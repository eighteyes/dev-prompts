# Dev Prompts

These prompts are for delivering an MVP plan and execution using Roo Code and Claude ( deepseek kinda works too, not as reliably ).

For use with Roo Code. Drop these `.clinerules*` files in your project root and they will apply the roles upon selection.

The base `.clinerules` file applies to ALL modes, so add your special instructions here. My focus is Python and JavaScript.

<https://github.com/RooVetGit/Roo-Code>

# Architect
>
> Note, the architect role doesn't permit file writing, so this 'archa' needs to be a custom role.

Moves through 7 modes, starting with a product focus, creating files along the way in `ai-docs`, finishing with a readme.

Validate the output here before continuing with coding, especially `plan.md`, as we will refer to that while coding.

# Code

Initially, ask:
> @./ai-docs/plan.md Review this plan for logical consistency

Kick off each session with:
> @./ai-docs/plan.md execute step n

At the end of each session, update the `ai-docs` with the current context with.
> update memory

Thanks to <https://github.com/nickbaumann98/cline_docs> for inspiration of the memory bank system.

# Duck
A simple one to use while running / debugging your application. Just send it your run command to kick it off so it doesn't have to waste tokens figuring it out.
