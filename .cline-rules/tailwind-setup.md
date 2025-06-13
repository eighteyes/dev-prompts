# Tailwind CSS Setup Rule

## Overview
When setting up Tailwind CSS in a React project, manual configuration is often more reliable than using CLI commands, especially in environments where the Tailwind CLI might not be accessible or have permission issues.

## Technical Details
1. **Installation**: Always install the core dependencies first:
   ```
   npm install tailwindcss postcss autoprefixer
   ```

2. **Configuration Files**: Create these files manually instead of relying on CLI commands:
   - `tailwind.config.js`: Contains theme configuration, content paths, and plugins
   - `postcss.config.js`: Sets up the PostCSS plugins (tailwindcss and autoprefixer)

3. **CSS Integration**: Add the Tailwind directives to your main CSS file:
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

4. **Content Configuration**: Always specify all file paths that might contain Tailwind classes:
   ```js
   content: [
     "./src/**/*.{js,jsx,ts,tsx}",
     "./public/index.html"
   ],
   ```

## When to Apply
- When setting up a new project that requires Tailwind CSS
- When migrating an existing project to use Tailwind CSS
- When troubleshooting Tailwind CSS installation issues

## Context Clues
- If `npx tailwindcss init` commands fail with "command not found" errors
- When working in environments with restricted permissions
- When you need precise control over the Tailwind configuration

## Metadata
- Version: 1.0
- Created: 2025-03-11
- Author: Roo
- Tags: tailwind, css, setup, configuration