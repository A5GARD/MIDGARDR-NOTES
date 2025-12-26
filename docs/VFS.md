#### Item Types

#### Files & Navigation

##### `file`
Quick access to frequently-used files with customizable labels and icons.
- Copy file paths from context menu
- Reveal files in explorer
- Set items as hidden
- Custom icon support via [VS Code icon library](https://code.visualstudio.com/api/references/icons-in-labels)

```json
{ "label": "prisma.schema", "path": "prisma/prisma.schema", "type": "file" }
```

##### `fileAtLine`
Open files at specific line numbers for immediate context.

```json
{ "label": "seed.ts", "path": "prisma/seed.ts:425", "type": "fileAtLine" }
```

**Path Format**: `relative/file/path:lineNumber`

##### `folder`
Organize items into collapsible groups.
- Set as global or workspace-specific
- Configure expanded/collapsed state on startup
- Hide folders when needed
- Add unlimited folders for either global or workspace
- UPDATE: can now create unlimited nested folders, where folders 2 deep would display

```json
{
  "label": "MAIN",
  "expanded": false,
  "type": "folder",
  "global": true,
  "hidden": false,
  "items": []
}
```

##### `url`
Access websites directly from the extensions pane.

```json
{ "label": "Google", "path": "https://www.google.com", "type": "url" }
```

#### Commands & Automation

##### `command`
Execute any VS Code command with a single click. Access 550+ built-in VS Code commands plus 450+ DevStack functions.

```json
{ "label": "SAVE ALL", "path": "workbench.action.files.saveAll", "type": "command" }
```

**Creating Commands:**
- **Custom Input**: Enter any command manually
- **VS Code Commands List**: Browse 550+ built-in commands with descriptions and categories
- **DevStack Commands List**: Access 450+ extension functions (400+ currently have AI-generated descriptions as work in progress)
- Auto-updating command picker that refreshes with each extension build

**Advanced Usage**: 
- Chain commands
- Sequential execution
- Access cheat sheet with 1050+ commands
- Set arguments for commands

```json
{ 
  "label": "Open Settings", 
  "type": "command", 
  "path": "workbench.action.openSettings", 
  "args": ["editor.fontSize"] 
}
```

##### `chain` - Sequential Execution
Execute commands one after another in your specified order. When creating items through the interface, the concurrent/sequential creation process enters a for loop allowing you to add as many custom or listed commands as needed.

```json
{ 
  "label": "Kill Terminals && Start DEV Server", 
  "path": "saveall, killterms, devApp", 
  "type": "chain" 
}
```

**Advanced Usage**: Mixed sequential/concurrent flows, conditional execution

**Preview**: [Video](https://youtu.be/ySp83VqxQ8s) | [Image](https://raw.githubusercontent.com/8an3/dev-notes/blob/main/vfs/SequentialExecution+.gif?raw=true)

##### `concurrent` - Parallel Execution
Run multiple commands simultaneously for maximum speed. Can run alongside sequential commands.

```json
{ 
  "label": "dev:all", 
  "path": "devApp, devCalc", 
  "type": "concurrent" 
}
```

**Concurrent Execution Features:**
- Two execution patterns:
  - **Sequential Execution**: Functions called with `await` for ordered execution
  - **Concurrent Execution**: `await` keyword omitted for parallel execution
- Commands pipe into a single terminal instance with:
  - Distinct color-coded output for each command
  - Interactive terminal for user input (e.g., canceling processes)
  - Terminal remains open as regular PowerShell after cancellation
- All other commands execute in separate environments with persistent terminal instances
- Failed command outputs remain available for review and debugging

**Advanced Usage**: Priority-based execution, resource management

**Enable**: Navigate to extension settings and toggle "Bleeding Edge" to `true`, or set `"ocrmnavigator.CONCURRENT": "bleeding-edge"` in settings

> [!TIP] `concurrent` && `chain` Optional creation process
> 
> The previous option to create an item with quickpick and inputs is available via the title pane dropdown and selecting `Add sequantial/concurrent/command chain via vscode` 
>
> There is now a new option if you select `Add item via Vscode` and select one of the three item types you wish to create.
> 
> INSTEAD of using quickpicks and inputs, this new process opens a jsonc file, in which you can, imo, much more easily create any of the three item types.
> Once started you will have a choice to add items of either:
> - using the new intellisense implementation, by `ctrl` + `space` within the path value of the parent object. 
>   - It scans your current vfs
>   - offers a dropdown displaying their labels. 
>   - once an option has been selected it wil add an object to the `chain` list that will be listed below the parent
> - the second option creates new objects within your config, you may copy the child object and paste it below to create a new object for your config
>   - any child item, whether you include it or not, will be given the value `hidden: true`
> Now you may use both systems, interchangeably in the case if you would like to add items exactly in the order you want them to execute in OR if you would like, add several options, not caring which order they are currently in. Once you have added all the items you wish, then cutting + pasting the objects in the execution order you would like them to happen
> All child items will execute in the order in which they are listed

##### `cmdChain`
Chain multiple VS Code or DevStack commands without building several config objects. Takes the value and executes each sequentially.

```json
{ "label": "Quick Setup", "path": "cmd1, cmd2, cmd3", "type": "cmdChain" }
```

> [!TIP] `cmdChain` Optional creation process
> 
> The same process will take place as `concurrent` && `chain`, the only difference is that whatever child items you add, WILL NOT be added to the config
>   - be sure you are only including `command` type items, because if you include any other item, the command will not work
> The intellisense options list has been replaced with dynamically acquiring vscodes currently available commands, to ensure the list is always update to date without my intervention
> There is a caveat with the auto generated commands list, the amount of available items it lists seems to be a lot less then the list that I can manually put together, by a lot. Because of this, if there is a command you wish to use but doesn't show up, don't worry, just paste it in and follow it with a command and space ie `, ` and move on to the next item
> I would rather include the entire list tbh, BUT whenever I can I create functions that take care of themselves due to the quantity of features available in this extension. If I were to have to manually groom this list constantly, I would never be able to get any other work done if every feature were like this. 
> There is however, a manually created list to view in the devstack quickpick menu `DevStack Cmds` and `VSCode Cmds` are both lists that dispaly commands that can be used with command chain. 
> VSCode cmds is a manually created list of vscode commands that were aquired via printing out every single available command that can be executed in my vscode instance. Then I took the time, to manually evaluate each item before deciding on whether to delete it or not. This process did not take long as I only have 2 other extensions active at any one time. Purely because I have not had the time to incorporate the functionality that I need from them into DevStack. The finished list came up to around 1830 options. Where as the dynamic list, comes up to 753, for me anyways
> The Devstack commands list IS dynmaically generated at the extensions build time to ensure that the list included is always up to date without my intervention
> The auto generated list does include, both vscode commands and commands avilable from this extension along with any other commands that are available to you within your OWN vscode instance. If you wanted to include commands from an extension you currently have installed, you may do so but be warned that whenever you go to use that `cmdChain` item it will only work if that extension is installed. Meaning if you configure that item at home, and then go to use it at work where you do not have that extension installed, it will not work.


#### Terminal Commands

##### `powershellCommand`
Execute commands in Windows PowerShell as if typed directly.

```json
{ "label": "CRM", "path": "code-insiders -n f:/DevStack", "type": "powershellCommand" }
```

**Advanced Usage**: WSL integration, environment variables, complex workflows

##### `debianCMD`
Run commands in Windows Debian WSL terminal environment. Execute programs with pre-programmed flags.

```json
{ 
  "label": "VLC w/ playlist", 
  "path": "cd /mnt/f/music && '/mnt/c/Program Files/VideoLAN/VLC/vlc.exe' playlist.xspf", 
  "type": "debianCMD" 
}
```

**Advanced Usage**: WSL integration, environment variables, complex workflows

**Note**: The ability to set arguments for powershell and bash commands is in development.


#### Utilities

##### `snippet`
Save snippets that copy to clipboard when clicked. Adds to the already included functionality of inline snippet insertion.

```json
{ "label": "Snippet Name", "path": "ocrmnavigator.code-snippets", "type": "snippet" }
```

##### `copyValue`
Place any predefined value into your clipboard.

```json
{ 
  "label": "Copy to clipboard", 
  "path": "Value to be copied into the clipboard", 
  "type": "copyValue" 
}
```

##### `settingsToggle`
Toggle VS Code settings between values. Defaults to toggle between true/false. If provided the args value, toggles through the array one by one.

```json
{ 
  "label": "ARCHIVER", 
  "path": "ocrmnavigator.ARCHIVER", 
  "type": "settingsToggle", 
  "args": ["custom", "vsce"],
  "icon": "settings" 
}
```

```json
{ 
  "label": "NPM Scripts", 
  "path": "ocrmnavigator.vfs.npmScripts", 
  "type": "settingsToggle", 
  "icon": "settings" 
}
```

##### `search`
Open search editors with predefined parameters. Opens in a new tab with context lines, case sensitive by default. Allows multiple search editors at once.

```json
{ 
  "label": "console.log(", 
  "path": "regex pattern to find console.log(", 
  "type": "search", 
  "icon": "search" 
}
```

##### `apiCall`
Execute HTTP API requests directly from the file tree.

**GET Request:**
```json
{
  "label": "Check API Status",
  "path": "https://api.example.com/status",
  "type": "apiCall",
  "icon": "cloud",
  "tooltipText": ""
}
```

**POST Request with Body:**
```json
{
  "label": "Deploy to Production",
  "path": "https://hooks.example.com/deploy",
  "type": "apiCall",
  "args": [
    { "method": "POST" },
    { "body": { "branch": "main", "environment": "production" } }
  ],
  "icon": "rocket"
}
```

When creating an api call from the title panes drop down menu a markdown doc will open that will help with the creation process as seen below:

```markdown
# API Call Configuration

# Required fields
label: ${label}
path: https://api.example.com/endpoint
type: ${itemType.value}

# Optional fields
icon: cloud
tooltipText: Description of this API call

# HTTP Configuration (optional)
args:
  - method: GET
  # For POST/PUT/PATCH requests with body:
  # - method: POST
  # - body:
  #     - key: value
  #     - another: value

# Headers (optional)
headers:
  - Content-Type: application/json
  # - Authorization: Bearer YOUR_TOKEN

# Instructions:
# - Fill in the required 'path' field with your API endpoint
# - Uncomment and modify optional sections as needed
# - Save this file to create the API call item
# - Close without saving to cancel
```


 ##### `layout`

[Layout Configuration Guide](./LAYOUT.md)

##### `label`

#### Auto-Generated Items

##### `tasks`
Automatically generated from `tasks.json` when workspace initializes.

##### `npmScripts`
Automatically generated from `package.json` when workspace initializes.

##### `settingsToggle`

- scans workspace settings.json and auto generates items within `SETTINGS` folder placing them in `workspace` so as to not overwrite any items you currently have within the settings folder. The auto generated items will only work for settings that use the values `false` | `true`

> [!TIP] `settingsToggle` Optional creation process
>
> If you have a settings key that requires a different value then `false` | `true`, then you may create a settings toggle
> When creating the new item, at the step of placing the required values you may place them in as such
> - `true, false`
> - `top, botton, left, right`
> And the function will take care of the formatting for you
> IF you do not know the values for the desired settings key at the time of creation, or would rather do other things than looking up vscodes settings.json values in microsofts amazingly kept together documentation, you may leave this value blank
> When leaving this value blank the function will dynamically aquire the required values for you and create the item in your config


##### `snippet`

- snippets are now auto generated items within the vfs explorer pane
- You may also edit the items within this folder, as these auto generated items will not actually take up any space within the config file itself, if any labels match any label from the auto generated list, those items will not be included
- allowing you to create you organization system for your snippet files
- snippet files adopted the global / workspace system, making them workspace context intelligent, enabling you to organize your snippets at a workspace level so you could have a different config for each project 


> [!NOTE] Moving Items
>
> Previously I relied on the web ui to provide a way to move items for users, but... I am trying to move away from that medium. It IS a lot easier to create functionality through that medium where the end-user will not only find it easy but painless. As far as moving items, I think I have thought of the best solution to provide through the vscode interface.
>
> Right clicking on any item and selecting `move` will bring up a quickpick, populated with your current configs items. 
> Wheenver you select an item from this list, it will place the item you are moving ABOVE that config item and save your edited config.
>
> By comparison, whenever you `cut` a line within vscodes editor, then place your cursor where you would like that line to end up. Pasting that item inserts it in the line above, just like the move item process. 
>
> It's not easy creating the `perfect` function when developing something, especially with an extension as complicated as this one. You have to know your end-user, their habits, what they do on a day to day basis, what they do while they work, what level of knowledge they may or may not possess and what experience level they may or may not be at, edge cases, not to mention forecasting what may or may not change within the code in the future, so on and so forth. Ontop of all that madness, vscodes interface and its limited available options to provide to end users when creating functionality. It becomes... a rather challenging problem to face. I KNOW I'm not the only one that's facing this issue, as 99% of the extensions on the marketplace have horrendous ui's and force the user to adopt to a stupid process, if not the entire ui atleast some parts of it. As I'm always challenging myself, I find these puzzles fun because you are not only looking to provide a technical solution but also a user solution and how they interact with what you built.
> Hopefully, the newly created `create` and `move` functions completely replace the need for the web ui as far as config items go, and will disable it for the meantime.



> [!TIP] Philosophy: Empowering Developers
> This extension takes an unconventional approach by exposing every internal function directly to you. While this is rare in VS Code extensions, the reasoning is simple: these functions were already built for personal use, and automating their availability helps colleagues and the broader community with minimal additional effort.
>
> Development work involves countless time-consuming repetitive tasks. Unlike some industries where these inefficiencies are unavoidable, software development offers a unique advantage—we can program solutions to our own problems. This extension aims to eliminate those time sinks and help you focus on what matters: building great software.
>
> Getting Started with Chains
> The `chain` type is the most powerful feature in DevStack. It allows you to combine multiple commands into a single workflow, dramatically reducing the steps required for common development tasks.
>
> Example 1: Git Workflow with Version Bump
> This chain automates the complete process of committing, pushing, and incrementing your package version:
> ```text
> type: chain
> path: gitAdd, gitCom, gitPush, bumpVers, gitPush, gitPushTags
> ```
> **Required Component Commands:**
> ```text
> type: powershellCommand
> hidden: true
> path: git add *
> 
> type: powershellCommand
> hidden: true
> path: git commit -m "pushing local data"
> 
> type: powershellCommand
> hidden: true
> path: git push
> 
> type: powershellCommand
> hidden: true
> path: pnpm version patch
> 
> type: powershellCommand
> hidden: true
> path: git push
> 
> type: powershellCommand
> hidden: true
> path: git push --tags
> ```
> Previously, this was run as a single inline command, which had edge cases that caused failures. Breaking it into modular components solved those reliability issues completely.
>
> Example 2: Using Extension Commands
> You can achieve the same result using the extension's built-in commands:
> ```text
> type: cmdChain
> path: ocrmnavigator.gitAdd, ocrmnavigator.gitCom, ocrmnavigator.gitPush, 
>       ocrmnavigator.bumpPatchVersion, ocrmnavigator.gitPush, 
>       ocrmnavigator.gitPushTags
> ```
> 
> The extension automatically detects your package manager (npm, pnpm, yarn) and adjusts commands accordingly.
> 
> ##### Example 3: VS Code Extension Development Workflow
> 
> This comprehensive chain handles the entire build-and-reload process for VS Code extension development:
> 
> ```text
> type: cmdChain
> path: ocrmnavigator.saveAll, ocrmnavigator.killAll, 
>       ocrmnavigator.formatPackageJson, ocrmnavigator.convertReadmeDevMd, 
>       ocrmnavigator.compileWithPackager, ocrmnavigator.installNow, 
>       ocrmnavigator.reloadWindow
> ```
> 
> **breakdoown:**
> 1. Saves all open editors
> 2. Terminates all terminal instances
> 3. Formats package.json files (supports dual package.json setup for automation)
> 4. Converts readme files for pre-processing
> 5. Compiles the extension using either:
>    - **vsce**: Creates local package and publishes to marketplace
>    - **Custom archiver**: Faster compilation with fewer restrictions (supports SVGs in readme, which vsce blocks)
> 6. Installs the extension locally
> 7. Reloads the current VS Code window
> 
> #### Real-World Impact
> 
> The automation possibilities are extensive. For example, my icon library workflow is fully automated—I simply drop an SVG file into a folder, click one button in the DevStack explorer, and walk away. The entire process runs automatically:
> 
> - Icon creation and optimization
> - README updates
> - Project compilation and building
> - Git commit and push to GitHub
> - Version bump
> - NPM publication
> 
> Since my projects are interconnected, I've even created a single button that executes this workflow across all three projects simultaneously.
> 
> Going forward, the extension will embrace a more modular architecture. Previously, functionality was built either entirely in config files or as monolithic standalone functions. The modular approach demonstrated above provides better reliability, maintainability, and reusability.





---

[🡄 Return](https://github.com/8an3/DevStack)










