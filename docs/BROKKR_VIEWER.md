# BROKKR
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> BROKKR Viewer

> [!IMPORTANT]
>
> Brokkr ngin now tracks ALL UI states that are changed while using the ngin.
>
> If you would like a reliable user experience of changing layouts, use the newly created customize layout feature that you can find in the viewer in place of vscodes customize layout. It works and looks EXACTLY the same as vscodes implementation, the only difference being is that each change commited to the UI is tracked and will be used with customizing ui elements. This is due to the fact that some ui elements and their current state, cannot be accessed progmatically by extension authors.

> [!NOTE]
>
> Viewer has had some items added to it, making it so that it serves as a means to quickly edit your config on the fly. Whether that be adding files to specific groups or removing them, it now does a lot more than I had first thought this would do. Currently the only thing it doesn't do that I can remember is removing or editing values contained within the performance, ocrmnav, workspace and color customizations objects. Along side the new brokkr menu, this feature as a whole is... rounding out quite nicely despite having 0 plans when I first started the layout ngin. Not only does it solve a number of issues, but does so in cohesive well-rounded manner. With the addition of that menu, vscode... no longer feels like vscode anymore. But just thinking about that for a moment... it trully no longer feels like I'm using the same software. It will feel even more separated with the addition of the github wrapper that I'm working on, and when I'm done I plan on removing gits icon from the ui... so it will TRULY feel like a completely different app. At the same time I will be removing the search icon as well which will leave, folders, to do / notes, and devstack... jeeze.

Snapshot ngin may be changing, be replaced by in part or in its entirety or something else entirely but, even though a new ui is coming I still want be able to do what I want from this feature.
Basically, a quick pick that pulls up the current layout and provides quick details with ability to change certain things on the fly. Despite it being as great as it is, still in its original form, there were defiently times I wish I could just quickly add, edit or remove something, followed with either closing vscode because something came up or I wanted to reload vscode with that one file opening back up when the default layout initialized once vscode started up again. 

The quick pick will be present in the status bar and once opened the following options will be presented to you:
- default toggle, whenever clicked it toggles to the opposite value after confirming your selection
- catergoized list of files by group using a label to declare the group on the first line, clicking on any line item will ask you if you would like to remove that item 
- categorized list of terminals, same features as the previous
  - the only difference being that the first line of each group will be a 'add terminal command' option
- a read only menu for keybindings, opens a new quick pick stating your current keybindings with a back button to return to the previous menu
- a categorized list of autorun commands, will work exactly the same as terminal commands except when selecting the add option, where it will just provide a list of all your current configs items to choose from and
- a categorized list of on close, same as autorun
- an option to open a new menu for the git object, the new menu will contain the following menu items
  - branch, selecting this option will provide a input to insert a new value
  - onOpen, same as autorun
  - onClose, same as onClose

### Themes, product icon themes and file icon themes

Brokkr viewer now also serves as an easier means to setting your vscodes color theme, icon theme and product icon theme.

In the quick pick menu the first three options are devoted to each of them and will consist of opetions that are currently available to you that are registered in your current vscode instance. Which means, whatever theme you have registered previously via marketplace extenions will also be listed here among this extensions offerings as well.

Whenever an option has been selected it saves it to your workspaces settings.json file instead of your global, leaving whatever settings you have in place for the three intact.

### Customize Layout

As a means to track all UI state changes, I have re-created vscodes custmize layout quick pick. Each option works exactly like vscodes implementation with the exception of each option now updates the ngin's state that it tracks for each ui element. This one change allows for a much more reliable user experience when using toggles such as zen mode, full screen and so on. 
        
- global config - `const globalConfigPath = path.join(ctx.storagePath, 'global-navigator-config.json');`
- project id - `const projectId = await getOrCreateProjectId(ctx.workspaceRoot);`
- workspace config - `const workspaceConfigPath = path.join(projectConfigsDir, `${projectId}.json`);`

- example config item that features the layout type 
```json
        {
          "label": "DevStack Default",
          "path": "",
          "type": "layout",
          "icon": "layout-baldr",
          "args": [
            {
              "default": true,
              "editorGrid": {
                "orientation": 0,
                "version": "classic",
                "editorFocus": "last",
                "groups": [
                  { "size": 0.5 },
                  { "size": 0.5 }
                ],
                "files": [
                  {
                    "group": 1,
                    "pinned": true,
                    "foldLevel": [1,2],
                    "path": [
                      "src/context.ts",
                      "src/helpers/search.ts",
                      "src/helpers/atlas.ts"
                    ]
                  },
                  {
                    "group": 2,
                    "pinned": true,
                       "foldLevel": [1,2],
                    "path": [
                      "README.md",
                      "package.dev.jsonc",
                      "src/helpers/menus.ts",
                      "src/extension.ts",
                      "src/helpers/itemsActionsMenu.ts",
                      "src/helpers/master.ts",
                      "src/extension/navigatorView.ts",
                      "F:/DevStack/docs/BROKKR.md",
                      "C:/Users/skyle/AppData/Roaming/Code - Insiders/User/globalStorage/skyler.ocrmnav/project-configs/project-1744496862041-y866zpqtd9.json",
                      "C:/Users/skyle/AppData/Roaming/Code - Insiders/User/globalStorage/skyler.ocrmnav/global-navigator-config.json"
                    ]
                  }
                ],
                "floatingWindow" :[

                ]
              },
              "terminalGrid": {
                "orientation": 0,
                "version": "classic",
                "terminals": [  ]
              },
              "keybindings": {
                "ocrmnavigator.menu.devstack": "alt+d",
                "ocrmnavigator.odin.open": "alt+s",
                "ocrmnavigator.icons.menu": "alt+i",
                "ocrmnavigator.menu.catalystUi": "alt+u",
                "ocrmnavigator.menu.snippets": "alt+f",
                "ocrmnavigator.region.insert": "alt+r",
                "ocrmnavigator.endregion.insert": "alt+e",
                "ocrmnavigator.region.wrap": "alt+w",
                "ocrmnavigator.devstack.site.colorWheel": "alt+q",
                "ocrmnavigator.clipboardMgr.history.show": "alt+h",
                "ocrmnavigator.bookmarks.show": "alt+b",
                "ocrmnavigator.menu.github": "alt+g",
                "ocrmnavigator.project.pkg.open": "alt+p",
                "ocrmnavigator.project.readme.open": "alt+m"
              },
              "autorun": [
                   { "label": "BALDR - executing outside icons project", "path": "saveall, pnpmrungenerateBaldr, pnpmrunbuildBaldr, patchAndPublishToNPMBaldr, npmPublishWithTokenBaldr", "type": "chain" }
              ],
              "onClose": [
                   { "label": "BALDR - executing outside icons project", "path": "saveall, pnpmrungenerateBaldr, pnpmrunbuildBaldr, patchAndPublishToNPMBaldr, npmPublishWithTokenBaldr", "type": "chain" }
              ],
              "git": {
                 "branch": "dev",
                "onLoad": [
                  {
                    "label": "pnpm i & ini / push prisma & ini .env & run scaffolding",
                    "path": "echo 'git on load'",
                    "type": "powershellCommand"
                  }
                ],
                "onClose": [
                  {
                    "label": "pnpm i & ini / push prisma & ini .env & run scaffolding",
                    "path": "echo 'git on close'",
                    "type": "powershellCommand"
                  }
                ]
               },
              "customizeLayout": {
                "menubar.navigationControls": true,
                "menubar.share": true,
                "menubar.layoutControls": true,
                "menubar.customizeLayout": true,
                "secondarySidebar.view": "skyler.ocrmnav",
                "secondarySidebar.position": "right",
                "primarySidebar.display": true,
                "workbench.activityBar.visible": true,
                "secondarySidebar.display": true,
                "panel.display": false,
                "panel.alignment": "center",
                "panel.view": "output",
                "modes.centeredLayout": false,
                "modes.fullScreen": false,
                "modes.zenMode": false
              },
              "performance": {},
            }
          ]
        }
```
