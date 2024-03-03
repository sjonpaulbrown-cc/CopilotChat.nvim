This is a high level overview of how to get started with contributing to `CopilotChat.nvim`.

Lets start with what you want to contribute to. This plugin started out with Python and `rplugin`. You can find the legacy Python code in `rplugin/python3/CopilotChat`. This may be removed from the main branch in the future, in which case you can look for a `legacy` branch.

<details>
<summary>

## Contributing to the legacy plugin

</summary>

Lets go by file names.

- `copilot_plugin.py` - This contains the command bindings between Neovim and the Python components. Look here if you want to add or modify a command at a high level. Look for @jellydn and @ziontee113 for info.
- `copilot.py` - This contains the core interactions with Copilot's API such as authentication and chat. Conversation history is also tracked here. @gptlang is responsible for this part.
- `handlers/` - This manages the Neovim buffer. The two main buffer handlers are `vsplit` and `in_place`. Token counting is also done here.
- `mypynvim/` - Magic by @ziontee113. Utilities for UI and other Neovim related things
- `prompts.py` - Self explanatory. Prompts are extracted from the VSCode extension by `mitmproxy`. Seek @gptlang.
- `typings.py` - Dataclasses for `Message` and `FileExtract`.
- `utilities.py` - Mostly request builders for JSON to be sent in `copilot.py`. Also manages authentication token cache.

</details>
