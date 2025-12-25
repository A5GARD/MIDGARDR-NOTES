# Layout Configuration Guide

The Workspace Layout Engine is designed for developers who switch contexts frequently—moving from heavy feature development to a focused debugging session or a minimal writing environment. It automates the tedious process of rearranging your editor every time you start a task.

This guide explains how to configure custom workspace layouts using the DevStack layout system. Each layout defines how VS Code appears when activated, including UI elements, editor tabs, terminals, and color themes.

> [!NOTE]
> The Workspace Layout Engine, a sophisticated orchestrator that allows you to define and switch between entire development environments with a single click. It doesn't just change a theme; it reconfigures the entire VS Code UI, opens your project files in specific grid positions, and prepares your terminal environment.
>
> At this time the issues have been resolved but the new item type still needs to tested thoroughly, but initial tests are perfect so far as I don't see a single item wrong even with the ridiculously long config I'm testing with. As my UI just loaded perfectly, with a config item of 516 lines long.

Despite being the most configurable workspace context layout engines, it was made with new and experienced devs in mind. If your new to dev and still want to use it, don't be intimated by it as it is extremely easy to set up a `simple` but still power layout. As for the more experienced devs, obviously if my config is 516 lines long without even trying, it can get a lot longer which grants you access to a lot more granular level of control of your vscode instance.

## Configuration Approachs

#### The quick and dirty method
Technically speaking... you can literally dump all the values you want / need to control within the `settings.workspace` object. As this object was created as a `dumping` ground for any and all vscode settings values. If all you want to use this for is a theme and very basic layout control, the only item you will need to configure is settings, by placing your values in either theme and workspace or both.

#### For ALOT more granular control

Smart Layout Capabilities
- Automated Workspace Reset: Optionally clears the deck by closing all open editors and killing active terminals to ensure a clean slate.
- Deep UI Configuration: Controls the visibility and position of the Activity Bar, Sidebars, Panel, and Status Bar via workspace-level settings.json automation.
- Performance Profiles: Automatically toggles high-overhead features like Inlay Hints, CodeLens, and Git Decorations to optimize performance based on your current task.
- Dynamic Editor Grids:
  - Define custom grid orientations (Horizontal/Vertical).
  - Specify group sizes (e.g., 20% sidebar group, 80% main group).
  - Auto-Open & Pin: Define sets of files to open in specific grid columns, with optional pinning for essential documentation or TODO lists.
- Terminal Automation: Spawns multiple terminals (in the Panel or Editor area) and automatically executes startup commands like npm run dev or log tailing.

Built-in Layout Presets

- Minimal -	Distraction-free writing -Hides Status Bar, Activity Bar, and Tabs. Disables Minimap.
- Focus -	Deep work / Logic -	Hidden Activity Bar, single-tab mode, centered editor layout.
- Full - Standard Development -	Enables Breadcrumbs, Sticky Scroll, and all UI navigation elements.
- Debug -	Troubleshooting -	Optimized for the debug console and secondary sidebars.

To control everything a 4 tier system has been implemented
1. Context/State commands - Runtime UI state (focus, visibility)
2. `customizeLayout` commands - Layout-specific UI state
3. `.vscode/settings.json` file - Workspace-specific overrides
4. VS Code Configuration API (`config.update()`) - Base settings

Not only allowing for a much cleaner looking config but also an easier time in the overall configuration process. You can think of each value within the appearance object as an organized version of its vscodes settings.jsons items, ie `editor.minimap.autohide` is simply `autoHide` within the minimap object

## Root object
- **label**
  - to be displayed as its label within the vfs
- **path** 
  - if you are only looking to create a single terminal instance and auto run that command, you may place the command within the path key
- **type**
  - `layout`
- **icon**
  - you may place any vscode icon value here to be shown in the vfs
  
## args

## Appearance Settings

### Quick Input
- **`quickInputPosition`**
  - Controls the position of quick input dialogs (command palette, etc.)
  - **Values**: `true` (shows in default position) | `false` (hides)

### Menu Bar
- **`view`**
  - Controls the menu bar visibility style
  - **Values**: `"classic"` (always visible) | `"toggle"` (hide, show on Alt) | `"hidden"` (always hidden) | `"compact"` (compact form)

- **`commandCenter`**
  - Shows/hides the command center
  - **Values**: `true` | `false`

- **`navigationControls`**
  - Controls navigation buttons (back/forward)
  - **Values**: `true` | `false`

- **`share`**
  - Controls the share button visibility
  - **Values**: `true` | `false`

- **`layoutControls`**
  - Shows/hides layout controls
  - **Values**: `true` | `false`

- **`customizeLayout`**
  - Enables layout customization options
  - **Values**: `true` | `false`

- **`togglePrimarySidebar`**
  - Shows/hides the primary sidebar toggle button
  - **Values**: `true` | `false`

- **`toggleSecondarySidebar`**
  - Shows/hides the secondary sidebar toggle button
  - **Values**: `true` | `false`

- **`togglePanel`**
  - Shows/hides the panel toggle button
  - **Values**: `true` | `false`

### Activity Bar
- **`display`**
  - Shows/hides the activity bar
  - **Values**: `true` | `false`

- **`position`**
  - Controls activity bar position
  - **Values**: `"default"` (left side) | `"right"` | `"hidden"`

### Primary Sidebar
- **`display`**
  - Shows/hides the primary sidebar
  - **Values**: `true` | `false`

- **`position`**
  - Controls primary sidebar position
  - **Values**: `"left"` | `"right"`

- **`view`**
  - Sets the default view shown in primary sidebar
  - **Values**: `"Explorer"` | `"Search"` | `"Source Control"` | `"Run and Debug"` | `"Extensions"`

- **`showLabels`**
  - Shows/hides labels in sidebar
  - **Values**: `true` | `false`

### Secondary Sidebar
- **`display`**
  - Shows/hides the secondary sidebar
  - **Values**: `true` | `false`

- **`view`**
  - Sets the view shown in secondary sidebar
  - **Values**: Extension view ID (e.g., `"skyler.ocrmnav"` for your custom navigator)

- **`showLabels`**
  - Shows/hides labels in secondary sidebar
  - **Values**: `true` | `false`

### Panel
- **`display`**
  - Shows/hides the panel
  - **Values**: `true` | `false`

- **`position`**
  - Controls panel position
  - **Values**: `"bottom"` | `"right"` | `"left"`

- **`alignment`**
  - Controls panel alignment when split
  - **Values**: `"center"` | `"left"` | `"right"`

- **`view`**
  - Sets the default view shown in panel
  - **Values**: `"output"` | `"terminal"` | `"problems"` | `"debug console"`

- **`maximized`**
  - Opens panel maximized
  - **Values**: `true` | `false`

### Modes
- **`fullScreen`**
  - Enables full screen mode
  - **Values**: `true` | `false`

- **`zenMode`**
  - Enables Zen mode (distraction-free)
  - **Values**: `true` | `false`

- **`centered`**
  - Enables centered layout mode
  - **Values**: `true` | `false`

### Status Bar
- **`visible`**
  - Shows/hides the status bar
  - **Values**: `true` | `false`

- **`hoverDebug`**
  - Shows debug info on hover in status bar
  - **Values**: `true` | `false`

### Minimap
- **`minimap`**
  - Enable/disable minimap
  - **Values**: `true` | `false`

- **`autohide`**
  - Controls when minimap auto-hides
  - **Values**: `"mouseover"` | `"never"` | `"always"`

- **`showMarkSectionHeaders`**
  - Show mark section headers in minimap
  - **Values**: `true` | `false`

- **`showRegionSectionHeaders`**
  - Show region section headers in minimap
  - **Values**: `true` | `false`

- **`showSlider`**
  - Show minimap slider
  - **Values**: `"mouseover"` | `"always"` | `"never"`

- **`side`**
  - Controls minimap side
  - **Values**: `"left"` | `"right"`

- **`size`**
  - Controls minimap size
  - **Values**: `"fill"` | `"proportional"` | `"fit"`

- **`renderCharacters`**
  - Render characters in minimap (vs blocks)
  - **Values**: `true` | `false`

- **`maxColumn`**
  - Maximum column width for minimap
  - **Values**: Number (e.g., `"50"`) | `"auto"`

### Terminal
- **`location`**
  - Default terminal location
  - **Values**: `"editor"` (opens in editor area) | `"panel"` (opens in panel)

- **`fontSize`**
  - Terminal font size
  - **Values**: Number (e.g., `12`)

### Editor
- **`zoomLevel`**
  - Controls editor zoom level
  - **Values**: Number (e.g., `-1` = zoom out, `0` = normal, `1` = zoom in)

- **`fontSize`**
  - Editor font size
  - **Values**: Number (e.g., `11`)

- **`breadcrumbs`**
  - Enable/disable breadcrumbs
  - **Values**: `true` | `false`

- **`tabBar`**
  - Controls tab bar style
  - **Values**: `"multiple"` | `"single"` | `"none"`

- **`editorsActionPosition`**
  - Position of editor action buttons
  - **Values**: `"tab"` (in tabs) | `"titleBar"` (in title bar)

- **`wordWrap`**
  - Enable word wrapping
  - **Values**: `true` | `false`

- **`fontFamily`**
  - Editor font family
  - **Values**: Font name (e.g., `"JetBrains Mono"`)

- **`fontLigatures`**
  - Enable font ligatures
  - **Values**: `true` | `false`

- **`foldingImportsByDefault`**
  - Fold imports by default
  - **Values**: `true` | `false`

- **`accessibilitySupport`**
  - Accessibility support level
  - **Values**: `"off"` | `"on"` | `"auto"`

- **`showFoldingControls`**
  - When to show folding controls
  - **Values**: `"always"` | `"mouseover"`

- **`showTabs`**
  - How tabs are shown
  - **Values**: `"multiple"` (multiple tabs) | `"single"` (single tab) | `"none"`

- **`alwaysShowEditorActions`**
  - Always show editor action buttons
  - **Values**: `true` | `false`

- **`enablePreviewFromQuickOpen`**
  - Enable preview from quick open
  - **Values**: `true` | `false`

- **`focusRecentEditorAfterClose`**
  - Focus recent editor after closing current
  - **Values**: `true` | `false`

- **`pinnedTabsOnSeparateRow`**
  - Show pinned tabs on separate row
  - **Values**: `true` | `false`

- **`wrapTabs`**
  - Wrap tabs when they overflow
  - **Values**: `true` | `false`

- **`limit.enabled`**
  - Enable editor limit (max width)
  - **Values**: `true` | `false`

- **`lineNumbers`**
  - Line number display style
  - **Values**: `"relative"` | `"on"` | `"off"` | `"interval"`

- **`scrollBeyondLastLine`**
  - Allow scrolling beyond last line
  - **Values**: `true` | `false`

- **`updateImportsOnPaste.enabled`**
  - Update imports when pasting code
  - **Values**: `true` | `false`

- **`restoreViewState`**
  - Restore editor view state on reopen
  - **Values**: `true` | `false`

- **`renderWhitespace`**
  - How to render whitespace
  - **Values**: `"none"` | `"boundary"` | `"selection"` | `"all"`

- **`renderControlCharacters`**
  - Render control characters
  - **Values**: `true` | `false`

- **`folding`**
  - Enable code folding
  - **Values**: `true` | `false`

- **`glyphMargin`**
  - Enable glyph margin (for breakpoints, etc.)
  - **Values**: `true` | `false`

#### Sticky Scroll
- **`enabled`**
  - Enable sticky scroll
  - **Values**: `true` | `false`

- **`maxLineCount`**
  - Maximum lines in sticky scroll
  - **Values**: Number (e.g., `5`)

### Editor Grid
- **`orientation`**
  - Grid orientation
  - **Values**: `0` (horizontal) | `1` (vertical)

- **`groups`**
  - Defines editor groups with sizes
  - **Values**: Array of objects with `size` property (0-1)

- **`files`**
  - Files to open in specific groups
  - **Values**: Array of objects with `path`, `group`, `pinned` properties

## Editor Grid Settings

### `orientation`
- **What it does**: Controls the orientation of editor groups (how they're split)
- **Values**: 
  - `0` = Horizontal split (editor groups side by side)
  - `1` = Vertical split (editor groups stacked vertically)

### `groups`
- **What it does**: Defines the editor groups and their relative sizes
- **Structure**: Array of objects with `size` property
- **Values**: 
  - Each `size` is a decimal between 0 and 1 representing percentage of available space
  - Example: `[{"size": 0.2}, {"size": 0.45}, {"size": 0.45}]` creates three groups taking 20%, 45%, and 45% of space

### `files`
- **What it does**: Specifies which files to open in which editor groups
- **Structure**: Array of objects with these properties:
  - `path`: String or array of strings - file paths to open
  - `group`: Number - which group to open files in (1-indexed: 1 = first group)
  - `pinned`: Boolean - whether to pin the tab (prevent replacement)
- **Values**: Custom file paths and group assignments

## Performance Settings

### Editor Features
- **`editor.inlineSuggest.enabled`**
  - **What it does**: Enables inline suggestions (GitHub Copilot, etc.)
  - **Values**: `true` | `false`

- **`editor.inlayHints.enabled`**
  - **What it does**: Shows type hints and parameter names inline in code
  - **Values**: `"off"` | `"on"` | `"onUnlessPressed"`

- **`editor.parameterHints.enabled`**
  - **What it does**: Shows parameter hints when typing function calls
  - **Values**: `true` | `false`

- **`editor.suggestOnTriggerCharacters`**
  - **What it does**: Shows suggestions automatically on trigger characters (like `.`, `::`)
  - **Values**: `true` | `false`

- **`editor.acceptSuggestionOnEnter`**
  - **What it does**: Controls Enter key behavior for accepting suggestions
  - **Values**: `"off"` | `"on"` | `"smart"`

- **`editor.acceptSuggestionOnCommitCharacter`**
  - **What it does**: Accepts suggestions when typing commit characters
  - **Values**: `true` | `false`

- **`editor.wordBasedSuggestions`**
  - **What it does**: Enables word-based code suggestions
  - **Values**: `"off"` | `"matchingDocuments"` | `"matchingDocumentsMore"` | `"allDocuments"`

### Formatting
- **`editor.formatOnType`**
  - **What it does**: Automatically formats code as you type
  - **Values**: `true` | `false`

- **`editor.formatOnPaste`**
  - **What it does**: Automatically formats pasted code
  - **Values**: `true` | `false`

- **`editor.formatOnSave`**
  - **What it does**: Automatically formats files when saved
  - **Values**: `true` | `false`

### Highlighting & Decorations
- **`editor.semanticHighlighting.enabled`**
  - **What it does**: Enables semantic colorization (more accurate than syntax highlighting)
  - **Values**: `true` | `false` | `"configuredByTheme"`

- **`editor.occurrencesHighlight`**
  - **What it does**: Highlights other occurrences of selected text
  - **Values**: `"off"` | `"singleFile"` | `"multiFile"`

- **`editor.selectionHighlight`**
  - **What it does**: Highlights other matches of current selection
  - **Values**: `true` | `false`

- **`editor.codeLens`**
  - **What it does**: Shows CodeLens (references, implementations count above code)
  - **Values**: `true` | `false`

### Git Integration
- **`git.decorations.enabled`**
  - **What it does**: Enables Git decorations in editor and explorer
  - **Values**: `true` | `false`

- **`git.diffDecorations`**
  - **What it does**: Shows Git diff decorations
  - **Values**: `"none"` | `"gutter"` | `"overview"` | `"all"`

- **`git.diffDecorationsGutterAction`**
  - **What it does**: Action when clicking diff decorations in gutter
  - **Values**: `"none"` | `"diff"` | `"peek"`

- **`git.diffEditor.renderGutterMenu`**
  - **What it does**: Shows menu in diff editor gutter
  - **Values**: `true` | `false`

- **`git.mergeEditor.codeLens.enabled`**
  - **What it does**: Shows CodeLens in merge editor
  - **Values**: `true` | `false`

### Search
- **`search.smartCase`**
  - **What it does**: Enables smart case search (case-insensitive unless uppercase used)
  - **Values**: `true` | `false`

- **`search.useIgnoreFiles`**
  - **What it does**: Respects .gitignore and other ignore files in search
  - **Values**: `true` | `false`

- **`search.exclude`**
  - **What it does**: Patterns to exclude from search results
  - **Values**: Object with glob patterns (e.g., `{"**/node_modules": true}`)

### File Management
- **`files.watcherExclude`**
  - **What it does**: Files/folders to exclude from file watching
  - **Values**: Object with glob patterns

- **`files.exclude`**
  - **What it does**: Files/folders to hide from file explorer
  - **Values**: Object with glob patterns

- **`files.maxMemoryForLargeFilesMB`**
  - **What it does**: Maximum memory allocated for large files
  - **Values**: Number (e.g., `4096` = 4GB)

### Extensions
- **`extensions.ignoreRecommendations`**
  - **What it does**: Ignores extension recommendations
  - **Values**: `true` | `false`

- **`extensions.showRecommendationsOnlyOnDemand`**
  - **What it does**: Only shows extension recommendations when requested
  - **Values**: `true` | `false`

### Workbench
- **`workbench.editor.enablePreview`**
  - **What it does**: Opens files in preview mode (single click replaces tab)
  - **Values**: `true` | `false`

### CSS
- **`css.validate`**
  - **What it does**: Validates CSS syntax and shows errors
  - **Values**: `true` | `false`

## Terminals Configuration

### Terminal Objects
- **Structure**: Array of terminal configuration objects
- **Properties**:
  - `name`: String - Display name for terminal
  - `cmd`: String - Command to run in terminal
  - `location`: String - Where terminal opens (`"editor"` or `"panel"`)
  - `cwd`: String - Working directory for command (empty = current workspace)
- **Values**: Custom terminal configurations for different purposes

## Settings & Workspace Configuration

### Workspace Settings
- **General VS Code Settings**: Controls various VS Code behaviors
- **Extension Settings**: Configuration for installed extensions
- **Language-specific Settings**: Settings for different file types

> [!TIP]
> Workspace
> This is your vscode settings.json dumping ground that will change the settings found within the workspace settings.json file. Allowing you to create a profile system and change its settings based on the layout config of your choosing. I have never even heard of another extension implementing such a system, but I have to say this has been a nice touch to the layout engine. 


### Theme Customizations (`workbench.colorCustomizations`)
- **What it does**: Overrides theme colors with custom values
- **Structure**: Object mapping VS Color Theme keys to color values
- **Common color keys**:
  - `background`: Main background color
  - `foreground`: Main text color
  - `editor.background`: Editor background
  - `editor.foreground`: Editor text color
  - `sideBar.background`: Sidebar background
  - `statusBar.background`: Status bar background
  - `terminal.ansi*`: Terminal color scheme (Black, Red, Green, Yellow, Blue, Magenta, Cyan, White)
- **Values**: Hex color codes or CSS color names



## Example Config

```json
   {
          "$schema": "./schemas/layout-config-schema.json",
          "label": "DevStack Default",
          "path": "",
          "type": "layout",
          "icon": "editor-layout",
          "args": [
            {
              "default": true,
              "appearance": {
                "quickInputPosition": true,
                "menuBar": {
                  "view": "classic",
                  "commandCenter": true,
                  "navigationControls": true,
                  "share": true,
                  "layoutControls": true,
                  "customizeLayout": true,
                  "togglePrimarySidebar": true,
                  "toggleSecondarySidebar": true,
                  "togglePanel": true
                },
                "activityBar": {
                  "display": true,
                  "position": "default"
                },
                "primarySidebar": {
                  "display": true,
                  "position": "left",
                  "view": "Explorer",
                  "showLabels": true
                },
                "secondarySidebar": {
                  "display": true,
                  "view": "skyler.ocrmnav",
                  "showLabels": false
                },
                "panel": {
                  "display": false,
                  "position": "bottom",
                  "alignment": "center",
                  "view": "output",
                  "maximized": true
                },
                "modes": {
                  "fullScreen": false,
                  "zenMode": false,
                  "centered": true
                },
                "statusBar": {
                  "visible": true,
                  "hoverDebug": true
                },
                "minimap": {
                  "minimap": true,
                  "autohide": "mouseover",
                  "showMarkSectionHeaders": false,
                  "showRegionSectionHeaders": true,
                  "showSlider": "mouseover",
                  "side": "left",
                  "NEWBELOW": false,
                  "size": "fill",
                  "renderCharacters": false,
                  "maxColumn": "50"
                },
                "terminal": {
                  "location": "editor",
                  "fontSize": 12
                },
                "editor": {
                  "zoomLevel": -1,
                  "fontSize": 11,
                  "breadcrumbs": false,
                  "tabBar": "multiple",
                  "editorsActionPosition": "tab",
                  "wordWrap": true,
                  "fontFamily": "JetBrains Mono",
                  "fontLigatures": true,
                  "foldingImportsByDefault": false,
                  "accessibilitySupport": "off",
                  "showFoldingControls": "always",
                  "showTabs": "multiple",
                  "alwaysShowEditorActions": true,
                  "enablePreviewFromQuickOpen": false,
                  "focusRecentEditorAfterClose": false,
                  "pinnedTabsOnSeparateRow": true,
                  "wrapTabs": true,
                  "limit.enabled": true,
                  "lineNumbers": "relative",
                  "scrollBeyondLastLine": false,
                  "updateImportsOnPaste.enabled": false,
                  "restoreViewState": true,
                  "renderWhitespace": "none",
                  "renderControlCharacters": true,
                  "folding": true,
                  "glyphMargin": true,
                  "stickyScroll": {
                    "enabled": true,
                    "maxLineCount": 5
                  }
                }
              },
              "editorGrid": {
                "orientation": 0,
                "groups": [
                  {
                    "size": 0.2
                  },
                  {
                    "size": 0.45
                  },
                  {
                    "size": 0.45
                  }
                ],
                "files": [
                  {
                    "path": ".vscode/ntrsync/10516_DevStack_todo.md",
                    "group": 1,
                    "pinned": true
                  },
                  {
                    "path": [
                      "src/extension.ts",
                      "src/helpers/master.ts",
                      "src/helpers/menus.ts",
                      "src/helpers/workspace.ts",
                      "src/extension/navigatorView.ts",
                      "src/helpers/itemsActionsMenu.ts",
                      "src/helpers/modular-commands.ts"
                    ],
                    "group": 2
                  },
                  {
                    "group": 3,
                    "pinned": true,
                    "path": [
                      "README.dev.md",
                      "package.dev.jsonc",
                    ]
                  }
                ]
              },
              "performance": {
                "editor.inlineSuggest.enabled": false,
                "editor.inlayHints.enabled": "off",
                "editor.parameterHints.enabled": false,
                "editor.suggestOnTriggerCharacters": false,
                "editor.acceptSuggestionOnEnter": "off",
                "editor.acceptSuggestionOnCommitCharacter": false,
                "editor.wordBasedSuggestions": "off",
                "editor.formatOnType": false,
                "editor.formatOnPaste": false,
                "editor.formatOnSave": false,
                "editor.semanticHighlighting.enabled": true,
                "editor.occurrencesHighlight": "off",
                "editor.selectionHighlight": true,
                "editor.codeLens": false,
                "git.decorations.enabled": false,
                "git.diffDecorations": "none",
                "git.diffDecorationsGutterAction": "none",
                "git.diffEditor.renderGutterMenu": false,
                "search.smartCase": true,
                "search.useIgnoreFiles": false,
                "search.exclude": {},
                "files.watcherExclude": {},
                "files.exclude": {},
                "files.maxMemoryForLargeFilesMB": 4096,
                "extensions.ignoreRecommendations": true,
                "extensions.showRecommendationsOnlyOnDemand": true,
                "git.mergeEditor.codeLens.enabled": false,
                "workbench.editor.enablePreview": false,
                "css.validate": true
              },
              "terminals": [
                {
                  "name": "Server",
                  "cmd": "npm run dev",
                  "location": "editor",
                  "cwd": ""
                },
                {
                  "name": "Logs",
                  "cmd": "tail -f dev.log",
                  "location": "panel",
                  "cwd": ""
                }
              ],
              "settings": {
                "workspace": {
                  "editor.minimap.renderCharacters": false,
                  "editor.minimap.maxColumn": "50",
                  "editor.minimap.size": "fill",
                  "ocrmnavigator.AUTO_FOLD_PKG": true,
                  "ocrmnavigator.BE_QP": true,
                  "ocrmnavigator.vscodeVersion": "Code - Insiders",
                  "ocrmnavigator.AUTORUN_DIR": "src",
                  "ocrmnavigator.UPDATE_PROMPT_OBJECTS": false,
                  "ocrmnavigator.AUTORUN_SCRIPTS": true,
                  "ocrmnavigator.CONVERT_README_DEV_MD": false,
                  "ocrmnavigator.PRO7": false,
                  "ocrmnavigator.CONCURRENT": "bleeding-edge",
                  "ocrmnavigator.ARCHIVER": "custom",
                  "ocrmnavigator.DELETE_OLD_VSIX": true,
                  "ocrmnavigator.AUTO_INSTALL_VSIX": true,
                  "ocrmnavigator.OPEN_PUB_DASH": true,
                  "ocrmnavigator.RELOAD_INSTANCE": true,
                  "ocrmnavigator.codesnap.windowControlStyle": "Windows",
                  "ocrmnavigator.codesnap.showWindowTitle": true,
                  "ocrmnavigator.codesnap.windowBorderRadius": "8px",
                  "ocrmnavigator.codesnap.windowTitleStyle": "Filename",
                  "ocrmnavigator.codesnap.showLineNumbers": true,
                  "ocrmnavigator.codesnap.realLineNumbers": false,
                  "ocrmnavigator.codesnap.transparentBackground": false,
                  "ocrmnavigator.codesnap.trimEmptyLines": false,
                  "ocrmnavigator.todo.branch": "main",
                  "ocrmnavigator.todo.checkRemindersInterval": "10",
                  "ocrmnavigator.todo.syncInterval": "20",
                  "ocrmnavigator.todo.syncOnSave": true,
                  "ocrmnavigator.todo.owner": "8an3",
                  "ocrmnavigator.todo.repository": "8an3/mynotesrepo",
                  "ocrmnavigator.todo.isPriv": false,
                  "ocrmnavigator.toggleHiddenItems": true,
                  "ocrmnavigator.strPrismaUpdater": true,
                  "ocrmnavigator.commands": true,
                  "ocrmnavigator.vscodecmdref": true,
                  "ocrmnavigator.markdownViewer": true,
                  "ocrmnavigator.snippets": true,
                  "ocrmnavigator.snippetsInEditor": true,
                  "ocrmnavigator.editorContextSnippets": true,
                  "ocrmnavigator.formatters": true,
                  "ocrmnavigator.trailingCommas": true,
                  "ocrmnavigator.batchRename": true,
                  "ocrmnavigator.eslintPrettier": true,
                  "ocrmnavigator.remixUtils": true,
                  "ocrmnavigator.theme": true,
                  "ocrmnavigator.blackedOut": true,
                  "ocrmnavigator.windowDifferentiator": true,
                  "ocrmnavigator.shadCNComponents": true,
                  "ocrmnavigator.repoMgr": true,
                  "ocrmnavigator.openGithub": true,
                  "ocrmnavigator.githubFunctions": true,
                  "ocrmnavigator.prismaFunctions": true,
                  "ocrmnavigator.remixComponents": true,
                  "ocrmnavigator.clickToSchema": true,
                  "ocrmnavigator.crudResolvers": true,
                  "ocrmnavigator.fileNesting": true,
                  "ocrmnavigator.revealExplorer": true,
                  "ocrmnavigator.copyPath": true,
                  "ocrmnavigator.bookmarks": true,
                  "ocrmnavigator.searchBar": true,
                  "ocrmnavigator.clipBoardHistory": true,
                  "ocrmnavigator.colorWheel": true,
                  "ocrmnavigator.lucideIcons": true,
                  "ocrmnavigator.share": true,
                  "ocrmnavigator.url": true,
                  "ocrmnavigator.jsonComments": true,
                  "ocrmnavigator.con": true,
                  "ocrmnavigator.removeAllComments": true,
                  "ocrmnavigator.unusedFunctions": true,
                  "ocrmnavigator.viewers": true,
                  "ocrmnavigator.uiDashboard": true,
                  "ocrmnavigator.devStackFunctions": true,
                  "ocrmnavigator.openLeftOffNote": true,
                  "ocrmnavigator.renderMd": true,
                  "ocrmnavigator.createFolderSmartIndex": true,
                  "ocrmnavigator.tailwindConverter": true,
                  "ocrmnavigator.convertToAgnostic": true,
                  "ocrmnavigator.concurrent": true,
                  "ocrmnavigator.autoSequencer": true,
                  "window.restoreWindows": "one",
                  "window.openFilesInNewWindow": "default",
                  "workbench.editorAssociations": {
                    "*.html": "default",
                    "*.svg": "default"
                  },
                  "workbench.editor.autoLockGroups": {
                    "default": false,
                    "mainThreadWebview-simpleBrowser.view": false,
                    "mainThreadWebview-browserPreview": false
                  },
                  "files.defaultLanguage": "TypeScript",
                  "terminal.integrated.profiles.windows": {
                    "PowerShell": {
                      "source": "PowerShell",
                      "icon": "terminal-powershell"
                    },
                    "Command Prompt": {
                      "path": [
                        "${env:windir}\\Sysnative\\cmd.exe",
                        "${env:windir}\\System32\\cmd.exe"
                      ],
                      "args": [],
                      "icon": "terminal-cmd"
                    },
                    "Git Bash": {
                      "source": "Git Bash"
                    },
                    "Debian (WSL)": {
                      "path": "C:\\Windows\\System32\\wsl.exe",
                      "args": [
                        "-d",
                        "Debian"
                      ],
                      "icon": "terminal-debian"
                    }
                  },
                  "[markdown]": {
                    "editor.quickSuggestions": {
                      "comments": false,
                      "strings": false,
                      "other": false
                    },
                    "workbench.quickOpen.preserveInput": true,
                    "workbench.editor.languageDetection": false,
                    "editor.defaultFormatter": "yzhang.markdown-all-in-one",
                    "editor.suggest.snippetsPreventQuickSuggestions": true,
                    "editor.acceptSuggestionOnEnter": "off",
                    "editor.suggest.showStatusBar": true,
                    "editor.hover.enabled": "on",
                    "editor.renderWhitespace": "none",
                    "editor.renderControlCharacters": false,
                    "editor.renderLineHighlight": "line",
                    "editor.matchBrackets": "always",
                    "editor.glyphMargin": true,
                    "editor.folding": true,
                    "editor.gotoLocation.multipleDefinitions": "gotoAndPeek",
                    "editor.gotoLocation.multipleTypeDefinitions": "gotoAndPeek",
                    "editor.gotoLocation.multipleDeclarations": "gotoAndPeek",
                    "editor.gotoLocation.multipleImplementations": "gotoAndPeek",
                    "editor.gotoLocation.multipleReferences": "gotoAndPeek",
                    "editor.links": true,
                    "editor.occurrencesHighlight": "off",
                    "editor.selectionHighlight": true,
                    "editor.semanticHighlighting.enabled": true,
                    "editor.showFoldingControls": "always",
                    "editor.suggest.insertMode": "replace",
                    "editor.suggest.filterGraceful": false,
                    "editor.suggest.shareSuggestSelections": false,
                    "editor.suggest.showClasses": false,
                    "editor.suggest.showColors": false,
                    "editor.suggest.showConstants": false,
                    "editor.suggest.showConstructors": false,
                    "editor.suggest.showCustomcolors": false,
                    "editor.suggest.showDeprecated": false,
                    "editor.suggest.showEnumMembers": false,
                    "editor.suggest.showEnums": false,
                    "editor.suggest.showEvents": false,
                    "editor.suggest.showFields": false,
                    "editor.suggest.showFiles": false,
                    "editor.suggest.showFolders": false,
                    "editor.suggest.showFunctions": false,
                    "editor.suggest.showInterfaces": false,
                    "editor.suggest.showIssues": false,
                    "editor.suggest.showKeywords": false,
                    "editor.suggest.showMethods": false,
                    "editor.suggest.showModules": false,
                    "editor.suggest.showOperators": false,
                    "editor.suggest.showProperties": false,
                    "editor.suggest.showReferences": false,
                    "editor.suggest.showSnippets": false,
                    "editor.suggest.showStructs": false,
                    "editor.suggest.showTypeParameters": false,
                    "editor.suggest.showUnits": false,
                    "editor.suggest.showUsers": false,
                    "editor.suggest.showValues": false,
                    "editor.suggest.showVariables": false,
                    "editor.suggest.showWords": false,
                    "editor.wordBasedSuggestions": "off",
                    "editor.wordBasedSuggestionsMode": "allDocuments",
                    "editor.suggestSelection": "recentlyUsed",
                    "diffEditor.wordWrap": "inherit"
                  },
                  "files.associations": {
                    ".env*": "dotenv"
                  },
                  "files.exclude": {},
                  "editor.defaultFormatter": "vscode.typescript-language-features",
                  "[typescriptreact]": {
                    "editor.defaultFormatter": "vscode.typescript-language-features"
                  },
                  "[javascriptreact]": {
                    "editor.defaultFormatter": "vscode.typescript-language-features"
                  },
                  "[typescript]": {
                    "editor.defaultFormatter": "vscode.typescript-language-features"
                  },
                  "[javascript]": {
                    "editor.defaultFormatter": "vscode.typescript-language-features"
                  },
                  "[json]": {
                    "editor.defaultFormatter": "vscode.json-language-features"
                  },
                  "[jsonc]": {
                    "editor.validate": false
                  },
                  "[css]": {
                    "editor.defaultFormatter": "vscode.css-language-features"
                  },
                  "[html]": {
                    "editor.defaultFormatter": "vscode.html-language-features"
                  },
                  "[snippets]": {
                    "editor.defaultFormatter": "vscode.json-language-features"
                  }
                },
                "workbench.colorCustomizations": {
                  "background": "#020817",
                  "menubar.background": "#020817",
                  "menubar.menu": "#020817",
                  "activityBar.background": "#020817",
                  "terminal.background": "#020817",
                  "titleBar.inactiveBackground": "#020817",
                  "titleBar.activeBackground": "#020817",
                  "panel.background": "#020817",
                  "terminalCommandDecoration.defaultBackground": "#020817",
                  "sideBar.background": "#020817",
                  "sideBarSectionHeader.background": "#1E293B",
                  "editor.background": "#020817",
                  "editorGroup.emptyBackground": "#020817",
                  "statusBar.background": "#020817",
                  "editorGroupHeader.tabsBackground": "#020817",
                  "activityBar.border": "#020817",
                  "menu.border": "#1E293B",
                  "menu.separatorBackground": "#1E293B",
                  "sideBar.border": "#1E293B",
                  "tree.tableColumnsBorder": "#1E293B",
                  "tab.border": "#1E293B",
                  "statusBar.border": "#1E293B",
                  "panel.border": "#1E293B",
                  "menu.foreground": "#94A3B8",
                  "foreground": "#94A3B8",
                  "menubar.foreground": "#94A3B8",
                  "activityBar.foreground": "#F8FAFC",
                  "sideBarSectionHeader.foreground": "#F8FAFC",
                  "explorer.folderItem.foreground": "#1E293B",
                  "panelTitle.activeForeground": "#F8FAFC",
                  "list.focusForeground": "#F8FAFC",
                  "sideBar.foreground": "#94A3B8",
                  "statusBar.foreground": "#94A3B8",
                  "editor.foreground": "#F8FAFC",
                  "activityBar.inactiveForeground": "#94A3B8",
                  "explorer.fileItem.foreground": "#94A3B8",
                  "input.background": "#1E293B",
                  "dropdown.background": "#1E293B",
                  "button.background": "#3B82F6",
                  "button.hoverBackground": "#3B82F6",
                  "input.foreground": "#F8FAFC",
                  "button.foreground": "#0F172A",
                  "menubar.selectionBackground": "#1E293B",
                  "menu.selectionBackground": "#1E293B",
                  "menubar.selectionForeground": "#F8FAFC",
                  "menu.selectionForeground": "#F8FAFC",
                  "list.activeSelectionBackground": "#1E293B",
                  "list.activeSelectionForeground": "#F8FAFC",
                  "input.border": "#1E293B",
                  "inputOption.activeBorder": "#1D4ED8",
                  "focusBorder": "#1D4ED8",
                  "errorForeground": "#7F1D1D",
                  "editor.lineHighlightBackground": "#1E293B",
                  "editor.selectionBackground": "#1E293B",
                  "editorCursor.foreground": "#F8FAFC",
                  "editorIndentGuide.background1": "#1E293B",
                  "editorWhitespace.foreground": "#1E293B",
                  "list.focusBackground": "#1E293B",
                  "list.hoverBackground": "#1E293B",
                  "list.highlightForeground": "#3B82F6",
                  "explorer.fileItem.hoverForeground": "#F8FAFC",
                  "explorer.folderItem.hoverForeground": "#F8FAFC",
                  "tree.indentGuidesStroke": "#1E293B",
                  "tab.activeBackground": "#020817",
                  "tab.activeForeground": "#F8FAFC",
                  "tab.inactiveBackground": "#020817",
                  "tab.inactiveForeground": "#94A3B8",
                  "tab.activeBorder": "#020817",
                  "gitDecoration.deletedResourceForeground": "#7F1D1D",
                  "gitDecoration.conflictingResourceForeground": "#3B82F6",
                  "terminal.ansiBlack": "#020817",
                  "terminal.ansiBlue": "#3B82F6",
                  "terminal.ansiCyan": "#29c3a0",
                  "terminal.ansiGreen": "#29c3a0",
                  "terminal.ansiMagenta": "#3B82F6",
                  "terminal.ansiRed": "#7F1D1D",
                  "terminal.ansiWhite": "#F8FAFC",
                  "terminal.ansiYellow": "#d29922",
                  "scrollbarSlider.hoverBackground": "#3B82F6",
                  "scrollbarSlider.activeBackground": "#3B82F6",
                  "scrollbarSlider.background": "#3B82F620",
                  "activityBarBadge.background": "#3B82F6",
                  "activityBarBadge.foreground": "#F8FAFC",
                  "explorer.folderItem.selectedIconForeground": "#3B82F6",
                  "explorer.fileItem.conflictForeground": "#7F1D1D",
                  "explorer.fileItem.errorForeground": "#7F1D1D",
                  "explorer.fileItem.warningForeground": "#d29922",
                  "explorer.folderItem.iconForeground": "#F8FAFC",
                  "explorer.fileItem.selectedIconForeground": "#F8FAFC",
                  "explorer.fileItem.modifiedForeground": "#29c3a0",
                  "list.dropBackground": "#02081740",
                  "list.filterMatchBackground": "#02081720",
                  "list.inactiveSelectionBackground": "#1E293B40",
                  "list.hoverForeground": "#F8FAFC",
                  "statusBarItem.hoverBackground": "#1E293B",
                  "gitDecoration.submoduleResourceForeground": "#F8FAFC"
                }
              }
            }
          ]
        }
```

> [!TIP]
> Troubleshooting
> If there is a setting that you want to use but do not see it among the options under appearance, I still got you covered. You can place anything you need in the settings.workspace object and will be included when updating the configuration.
> If a setting isn't applying:
> 1. Check the setting name matches VS Code's exact setting key
> 2. Try placing it in `settings.workspace` instead
> 3. Restart VS Code after applying the layout
> 4. Check the VS Code output panel for errors
> 5. Verify the setting type (boolean, string, number, object)

> [!TIP]
> Additional Resources
> - [VS Code Settings Reference](https://code.visualstudio.com/docs/getstarted/settings)
> - [VS Code API Documentation](https://code.visualstudio.com/api)
> - [Workspace Configuration](https://code.visualstudio.com/docs/editor/workspaces)

> [!TIP]
> Theme
> To quickly create this section you can use the theme builder that can be found on the web ui.
> Once your theme has been built just copy over the settings into the config


