# BROKKR

> [!IMPORTANT]
>
> Please excuse the current state of the docs as this feature is currently undergoing an overhaul as it contains notes for the overhaul as well as documentation for the old version and the new version. New version documentation is indicated by the new icon that has been adopted into the docs, the red valknut. Despite the new version not yet available, this doc does contain documentation pertaining to the new version as it goes through its transformation. Some features that are meant for the newer version are currently available for you to use with manually editing your configs object. Such as the new theme variable, product icon theme, brokker viewer, file icon theme and more.

> [!NOTE]
> The new layout system is already underway, starting with focusing on the UI and how each level feels along with adjusting which level should control what exactly. No idea how I'll go about the back end of things yet, but we'll get there and figure it out. 
>
> Want to say this here in case you don't make it to the end, IF you haven't tried it yet... try this layout engine. I now have a config or more for every workspace... and it has been such a better experience than I first thought this feature would have as far as overall impact to the user experience within vscode. Even though an update is coming, who knows when it will done enough to use which is why I'm still suggesting, try this out seriously if I had to choose 5 features for someone to try out with this extension... this would be number 1 or number 2.
>
> In case you didn't read the notes below, some things that I did come across but still have to dive into further to see if they are viable paths to edit. A while back I tried adding a feature to the extension where it blocks... ALL toast notifications. Using insiders, they're plentiful and annoying and to make matters worse there seems to be a ton of devs that love recommending things that also pop up and ya... hit a dead end with it before, but it seems like this could be something that might get done.
> Don't read into this too much, but I did see some icons values... who knows, maybe even add custom icons to vscode?! That would be nice. And not just in the file tree.
> Even after finding that security threat in vscode and before even talking to microsoft I had decided NOT to move forward with it because of that... after all that, they never even responded, figures. Despite that I still don't want to use the workaround that I had found, primarily due to, exposing how its done and even though microsoft doesn't care I'd rather just keep that under wraps instead of advertising it to everyone. With saving that, I did see some values that might actually get the end result that I was going for... so, atleast the idea isn't completely dead yet, because weirdly this one feature excites me most currently. I don't know why, maybe it's because I had to deal with performance issues a lot, I was running a lot although I wasn't running a lot in vscode itself which was the main culprit but still.
> I don't know how but, I do really want some sort of stale data / garbage collector since going through those values... I saw A LOT of old data, that hasn't been used in years just sitting there. I'll try to calculate just how much storage that's actually taking up, because if it isn't enough to warrant going through the trouble, then theres no point.
> OH, almost forgot, once sauron is up and working I will be working on setting up the profile contexts up next in regards to layouts, and probably even for the rest of the extension. 

> [!NOTE]
> Levels 1, 2 and 3 will be getting more options to configure. Currently I have only coded in my own settings into Saurons tab, and it is astromically funny just how big of a difference there is between them. But after seeing it come together in the ui, it's going to be easy enough to know that no one should have any issue having the config they want as each part has descriptions and what not. 
>
> The new atlas layout system will come out in 2 versions, one after another. The first will be virtually how it is now but in ui form. Since there are a lot of moving parts I want to make sure the ui works before even moving on to the more complex settings that will be available in level 4, which means if you don't plan on using that level, you will be able to work with the new system rather quickly. With the new system being so simple the only documentation there will be is just an overview of each of the levels, and that's it really. as it's pretty self explanatory. At which point I will start working on the last tab, which might be over and done with quickly or... it will take some time with trying to figure out what everything does. A lot of that extra time will depend on new the systems being introduced to handle the new features, if any.

> [!NOTE]
> 
> finally took the time and went through every ui toggle and setting and grabbed all the necessary values with the exception of two values that I'm shocked I couldn't find... but I'll try blindly setting them to see if I can't find them since the files I'm now searching through do not have intellisense. 
>
> This means in addition to offering every setting available to certain levels, every level will atleast be getting a basic ui configuration manipulation section and I'm leaning towards offering the advance to all levels. Simply because the ui is so simple and makes for a really easy time of it.
>
> Ontop of that I think I beleive I have though of the perfect solution, when it comes to reliably tracking the state of the ui now that I've gained access to more values.
> 
> - It would be best if you started both of your settings files with a blank state, aside from the settings that are too advanced, obscure or any extensions specific settings, but be absolutely sure that no ui setting is currently in your workspace settings.json file. If you don't know what I mean by this, your in the clear and dont worry about it because whenever changes are made to the ui through the user interface, they are saved to the global file only.
> - thus making the next part more reliable, on start up it will not only take in any settings that are relevant that you may have set through this extensions settings, but also scan your current global settings file for each of the required values, IF there is no value among these sources a default will be used. The same default that would be used as if both your settings files were empty.
> - at which point using the already in place global context system in the extension, these values will be added so that they can be viewed, compared against and changed when needed as there will be more than one function with the ability to change them
> - whenever a layout is triggered, these values will be updated so as to know exactly what state everything is in when used else where but the global settings file will be used as a source of truth in certain circumstances to ensure the most up to date information is available prior to executing some functions. As the function sweeps through the list of functions that control every thing it will first check what the current state is, compare it against what you want and either skip it or trigger the function in order to get the desired end result
> - the new viewer, will also view and edit these values even going so far as re creating the custom layout menu that vscode has implemented into the system
>
> The only values I beleive I'm currently missing are primary and secondary sidebar boolean values, along with panel. I can toggle them, I just don't know what state they are in prior to toggling them so if your current ui is not what is expected of your configuration, then it does behalf with the opposite end result. Atleast these three ui items are... very easy to toggle back into view if that does happen.
>
> So currently, please try to use the viewer in order to make changes to the ui as your coding. The customize layout system is literlly exactly the same as vscodes. Because we can only track certain states ourselves without relying on vscode, this will be vital for a reliable state.

# Layout Configuration Guide

More of an overview of what to expect, than an actual guide since it's extremely straight forward, except maybe one part which I will go over.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Casual

- Layout name
- Icon - allowing you to set that layouts icon to be displayed in the sidebar
- Pre-configured theme dropdown - that will provide a selection of pre configured themes that I have registered with the extension
- UI Elements - this being one of the sections that was added on you can control: 
  - Primary sidebar
  - Secondary sidebar
  - Activity bar
  - Status bar
  - Panel Visibility
  - Panel alignment
  - Mode
- One auto run terminal command that executes once the workspace initializes
- file inputs so as to set a file for a 2 col editor group, you may only place one file in each of the 2 columns that are avaialable at this level
- checkbox to set the layout to deafult

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Intermediate

In addition to the above:
- Custom theme colors - instead of going with one of the many pre configured themes you may set your own color scheme. By shrinking down the amount of values needed to be placed in the custom section, this allows for you to create a nice cohesive theme across the entire UI with very little effort. Saving you tons of time in the process compared to the default process of completing this task. The following colors will be avaialbe for you to customize:
  - Background
  - Muted Background
  - Foreground
  - muted foreground
  - border
  - primary
  - primary foreground
- Instead of one file per col, you may select as many files as you wish and organize them per col

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Power User

In addition to the above:
- Plex vs Default Layout: Editor Grid
- Plex vs Default Layout: Terminal Grid

You may choose to stick with the default columns layout, but customizing the amount to whatever you wish it to be and allowing you to assign as many files to each.
If you prefer the linux `plex` style layout configuration, you may choose the amount of cols and rows to be used for both terminals and editor groups.

Just like you can with editors, you may choose to add as many config items to any terminal group you may wish, each item adds a new tab within that terminal group.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Sauron

In addition to the above:
This one has changed the most... weirdly, due to the overall length I have had to modify it by adding in a second sidebar to the right, and a search bar when dealing with settings values.
The sidebar contains the following: 
- Theme, as you can now edit every single color value via a color picker or input to paste in your value
- Auto run - you may place as many config items as you wish here, selectable via a drop down that scans your current config and populating the options with them
- Auto close - same as above but runs when you go to close the workspace, you may also override the execution of these commands by double clicking the windows close button
- Git 
  - has a value to place the desired branch you would like whenever you trigger that layout
  - onLoad - open and onClose values to place git related commands will work exactly autorun and onClose respectively
- Configuration settings - I have no hardcoded a single setting, opting out for the lazy mans version by dynamically generating this list via your vscode instance and populating the list with all the commands available to you at the time of creating or editing that current config
- .vscdb settings - this is where the `hidden` or whatever you want to call them, settings will be that we cannot modify anywhere else but here
- Editor grid - same as last group
- Terminal Grid - same as last group
- and this isn't all the items just yet, below you will find documentation on how to use the remaining items.

> [!NOTE] 
>
> For the next 3 following options whether they are set manually or using the newly created UI, whenever the ngin goes to set these values it will set them within your workspaces settings.json files instead of the global counterpart. These three values will be the only settings that will save in this fashion, which means you are free to set a default value for each of them to be used no matter what instance you are currently in. While at the same time, allowing for personal touches in each of the layouts configs.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Product Icons

This now grants the ability to change product icons, file icons and themes on a workspace context level. 

### Manually
Currently, you can do this manually as it is already coded into the ngin.

You can now set a registered product icon theme explicitly through the following setting:

```json
{
  "productIconTheme": "baldr-icons",
}
```

Placement is at the root level of the args object alongside customizeLayout and others.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> File Icons

### Manually
Currently, you can do this manually as it is already coded into the ngin.

You can now set a registered file icon theme explicitly through the following setting:

```json
{
  "fileIconTheme": "baldr-icons",
}
```

Placement is at the root level of the args object alongside customizeLayout and others.


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Themes

> [!NOTE] 
>
> Whether you opt in to choosing a registered theme or providing your own custom theme through workbench.colorCustomizations, these are now set in the workspace settings.json file. Where as previously everything was set at the global level, which allows for even further customization in terms of a globally set theme and themes set with a workspace context. 
> 
> This has been mentioned previously but will mention it again here incase you missed it, along with workbench.colorCustomizations the following values are only set at a workspace level, workbench.iconTheme ( registered file icon theme packs ), workbench.colorTheme ( registered theme packs ), workbench.productIconTheme ( registered product icon theme packs ). The only way this would necessitate a change is if these three values, or any value on its own, can only be set a global level.


### Manually
Currently, you can do this manually as it is already coded into the ngin.

You can now set a registered theme explicitly through the following setting:

```json
{
  "theme": "Deep-Void",
}
```

Placement is at the root level of the args object alongside customizeLayout and others.

### BROKKR
It may be up and running by the time you read this but once this is up and running you will be able to select one of the extensions registered themes via a dropdown menu, I will try to make it so that the dropdown menu contains ALL registered themes even ones you have registered or installed else where but currently I have no idea how to obtain that information. Currently the themes offered through this extension are as follows, but is not limited to:


> [!NOTE] 
>
> There is now a "base" counterpart version for each of the listed themes, these themes do not contain themed syntax highlighting. At the same time, I don't currently know if this will even work out but, each themes label in vscodes ui will contain which colors that theme was based off of when it was created.


- Acid-Trip // lime
- Another-Acid-Trip // Lime2
- Afterglow-Fade 
- Amazon-Jungle // Green
- Amethyst-Stone // Violet
- Aqua-Glacier // Cyan
- Black-Velvet-Luxe 
- Blueprint-Grid 
- C-Carbon-6 // blacked-out
- Cirrus-Float 
- Cobalt-Ice // Blue
- Concrete-slab // gray
- Crystal-Quartz // Rose
- Cyber-Industrial 
- Cyber-Pop 
- Dark-Crimson // Red
- Deep-Abyss // darkBlue
- Deep-Emerald // Emerald
- Deep-Ocean 
- Deep-Sea-Navigator 
- Deep-Teal // teal
- Deep-Void // blued-out
- Desert-Night 
- Espresso-High 
- Executive-Level 
- Fifth-Element-Aether // sky
- Forest-Tech 
- Frozen-Deep 
- Glacier-Blue 
- Graphite-Neutron-Moderator // slate
- Granite-Top // stone
- High-Alert-Crimson 
- Interstellar-Nebula // purple
- Loki // dark green
- Mainframe-Terminal 
- Meadow-Whisper 
- Metropolis-Sky-Scape 
- Midas-Touch // Yellow
- Middle-Field-Canvas // neutral
- Mineral-Forest 
- Modern-Retro 
- Monet-Impressionism 
- Nightshade-Venom // Indigo
- Obsidian-Wine 
- Oceanic-Gradient 
- Oceanic-Sunset 
- Office-Paper 
- Oracle-Vision 
- Pastel-Sorbet 
- Polymer-Flow 
- Retro-Arcade 
- Silk-Petal // Fuchsia
- Smoldering-Ember // Amber
- Solar-Flare // Orange
- Solstice-Heat 
- Sonic-Pulse 
- Sorbet-Swirl 
- Studio-Apartment 
- Synthwave-Neon // eighties
- Tactical-Ops 
- Terra-Verde 
- Ti-Titanium-22 // zinc
- True-Veridian // emerald
- Twilight-Bloom 
- Vanguard-Strike 
- Vintage-Heritage 
- Workplace-Chatter 
- Tree-Hugger 

The only reason I say is not limited too is because, the themes have been turning out better than I had hoped. Even the syntax highlighting looks... fucking great, albeit personally thats not for me but never the less they look phenomanal which makes me kinda jealous. To the point that, I have now included base variants for each of the themes which was a lot less of a headache than I originally thought and took way less time.

Anywho, whenever I have the time or whenever I need a break from regular coding I would like to continue going through the most popular pallete color combinations and use them to create more themes. Which is how a lot of the current themes were made. Following such a design decision ensures that whatever theme I do end up making I know that the majority of people would enjoy since the colors used are colors that have been voted most popular on the color pallete sites. 

I find this design philosophy makes each theme look phenomonal, despite a lot of the featuring colors I would have not at first chosen for a theme. But since the themes color pallete already jives with one another so much, they turned out to be great themes in compar

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

## Ignore All Notifications / Toasts ( WIP )
## Workspace Extensions Context ( WIP )
## Profile Context ( WIP )

<br /><br />


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> BROKKR Menu

While brokker viewer takes care of your current layout configs needs, brokkr menu takes care of others while allowing it to keep track of updating the current UI's state while at the same time offering a easier means to setting those values. 

For example setting the current theme through the menu bar, means traversing through 4 different levels of menus and submenus to finally present the quickpick that offers the selection of themes you have available to you.

The same will will be achieved through a single click in this menu.

While not only being a faster alternative, it also takes what is currently scattered throughout different menus, quickpicks, submenus and commands and consolidating it to a single source.

I do not know why Microsoft designed it this way that, whenever you want to change different elements of the UI that you have to go on a scavenger hunt and find them scattered throughout in a haphazard fashion. Themes being in thrown 4 levels deep in submenus, meanwhile a portion of manipulating the UI is in an entirely different menu, and then you have customize layout and the three panel toggles on the opposite end of the menu bar and lets not forget about the command pallete.

It's kind of a pain really, but its weird that no one even really attempts to bother solving as it seems all devs just live with it. As if collectively, everyone just shrugged and said, "it is the way it is".

This menu will grow over time as I find more to place within it, but it will serve the idea of a single source of all things UI. Currently it contains the following:

- Select a theme
- Select a file icon theme
- Select a product icon theme
- Toggle sidebar
  - toggle displayed tabs
- Toggle secondar sidebar
  - display labels
- toggle layout controls
- toggle navigation controls
- toggle share controls
- toggle command center
- toggle folding
- select folding controls configuration
- toggle fold imports by default
- toggle line numbers
- Toggle panel
- select panel position
- select panel alignment
- toggle panel show labels
- Toggle activity bar
- select activity bar position
- Toggle Status bar
- Toggle title bar style
- Select title bar style (native, custom)
- Toggle zen mode
- Toggle full screen
- toggle word wrap
- Toggle inline suggestions
- Toggle snippets suggestions
- Toggle quick suggestions
- Toggle tab completion
- Toggle format on paste
- Toggle format on type
- Toggle format on save
- Toggle auto save
- Select auto save delay
- Toggle timeline view
- Toggle outline view
- Toggle trim trailing whitespace
- Toggle insert final newline
- Toggle emmet
- Toggle code lens
- Toggle rulers
- Toggle parameter hints
- Toggle suggest widget
- Toggle hover
- select default external browser
- Move primary sidebar right
- Toggle editor tabs
- select tab bar configuration
- Select tab sizing (fit, shrink, fixed)
- Toggle indent guides
- Select indent guides style
- Toggle explorer compact folders
- Toggle explorer sort order
- Select explorer sort order type
- Toggle problems view
- Toggle output view
- Toggle debug console
- Toggle terminal tabs
- Toggle screencast mode
- Select workbench appearance (compact, default, comfortable)
- toggle minimap
  - select max column
  - toggle show region section headers
  - toggle show mark section headers
  - select auto hide configuration
  - select show slider configurations
  - select side
  - select size 
  - select render characters
- toggle breadcrumbs
- toggle sticky scroll
- Toggle smooth scrolling
- toggle terminal stick scroll
- toggle render whitespace
- toggle render control characters
- zoom in
- zoom out
- reset zoom level
- increase font size
- decrease font size
- reset font size to 12
- select font
- toggle font ligatures
- toggle font variations
- set editors actions position
- editor layout
  - split
    - split up
    - split down
    - split right
    - split left
  - split in group
  - move editor into new window
  - copy editor into new window
  - modify current editor group
    - single
    - two cols
    - three cols
    - two rows
    - three rows
    - grid 2x2
    - two rows right
    - two cols bottom
  - flip layout
- decorations
  - toggle git diff editor render gutter menu
  - toggle git decorations
  - toggle scroll beyond last line
  - toggle editor decorations colors
  - toggle editor highlight modified tabs
  - select scm diff decorations
  - select scm diff deorations gutter action
  - Toggle tab decorations
  - Toggle color decorators
  - Toggle explorer decorations
- git
  - Toggle git lens inline blame
  - Toggle git lens code lens
- Toggle terminal bell

This menu will NOT change your current config, think of it more as an expanded upon customize layout feature.

Did not see that coming... in terms of the total number of options that were going to be included. If this were anyone elses extension, this itself would be its own extension as a means to consolidate all UI features.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Current Config

While the new ngin is being created you can still use this feature while its under construction by following the configuration below:

```json
     {
          "label": "DevStack Default",
          "path": "",
          "type": "layout",
          "icon": "layout",
          "args": [
            {
              "default": true, // determines this config to be used as a default and loaded in whenever you open this workspace if placed in a workspace context config, if placed in a global config then this would be loaded in every single workspace you open and you may only have one default in each workspace, whether or not you include the object in your global or workspace folders
              "fileIconTheme": "baldr-icons", // this allows you to set a different file icon theme pack per config
              "productIconTheme": "baldr-icons", // the same goes for product icon theme packs as well
              "theme": "Deep-Void-Base", // instead of just relying on the workbench.colorCustomizations object to allow us to change the theme on a config by config basis, setting this value allows you to change the registered theme on a config by config basis
              // all items pertaining to custmoziing the layout, the values found within this object must be contained within this object since these values are tracked and are called upon from this object only
              "customizeLayout": {
                "window.menuBarVisibility": "classic",
                "window.commandCenter": true,
                "menubar.layoutControls": true,
                "editor.renderControlCharacters": false,
                "editor.renderWhitespace": "none",
                "editor.minimap.enabled": true,
                "breadcrumbs.enabled": false,
                "workbench.sideBar.location": "left",
                "workbench.statusBar.visible": true,
                "workbench.layoutControl.enabled": true,
                "workbench.secondarySideBar.showLabels": false,
                "workbench.navigationControl.enabled": true,
                "workbench.editor.showTabs": "multiple",
                "menubar.navigationControls": true,
                "menubar.share": true,
                "primarySidebar.display": true,
                "secondarySidebar.display": true,
                "panel.display": false,
                "panel.alignment": "center",
                "panel.view": "output",
                "modes.centeredLayout": false,
                "modes.fullScreen": false,
                "modes.zenMode": false,
                "window.zoomLevel": -2,
                "editor.glyphMargin": true,
                "editor.folding": true,
                "editor.lineNumbers": "relative",
                "editor.showFoldingControls": "always",
                "editor.minimap.maxColumn": 50,
                "editor.minimap.showRegionSectionHeaders": true,
                "editor.minimap.showMarkSectionHeaders": false,
                "editor.minimap.autohide": "mouseover",
                "editor.minimap.showSlider": "mouseover",
                "editor.minimap.side": "left",
                "editor.minimap.size": "fill",
                "editor.minimap.renderCharacters": false,
                "editor.wordWrap": "on",
                "editor.fontLigatures": true,
                "editor.fontVariations": true,
                "workbench.editor.pinnedTabsOnSeparateRow": true,
                "workbench.editor.alwaysShowEditorActions": true,
                "workbench.editor.enablePreviewFromQuickOpen": false,
                "workbench.editor.wrapTabs": true,
                "workbench.externalBrowser": "Opera",
                "workbench.remoteIndicator.showExtensionRecommendations": false,
                "workbench.commandPalette.history": 30,
                "window.restoreWindows": "one",
                "workbench.editor.autoLockGroups": true,
                "workbench.panel.showLabels": false,
                "editor.foldingImportsByDefault": false,
                "git.diffEditor.renderGutterMenu": false,
                "git.decorations.enabled": false,
                "editor.fontFamily": "JetBrains Mono",
                "editor.scrollBeyondLastLine": false,
                "terminal.integrated.fontSize": 12,
                "editor.fontSize": 12,
                "scm.diffDecorationsGutterAction": "none",
                "scm.diffDecorations": "none",
                "workbench.iconTheme": "baldr-icons",
                "workbench.activityBar.location": "default",
                "workbench.editor.decorations.colors": false,
                "window.newWindowDimensions": "inherit",
                "workbench.editor.highlightModifiedTabs": false,
                "markdown.preview.scrollPreviewWithEditor": false,
                "markdown.preview.scrollEditorWithPreview": false
              },
              // settings values pertaining to this extension, more or less a means of organization since there are so many, you may place anything in here other than what is found within the custmizeLayout object
              "devstack": {
                "ocrmnavigator.devstack.icons": true,
                "ocrmnavigator.devstack.snapshotNgin": true,
                "ocrmnavigator.devstack.ivaldi": true,
                "ocrmnavigator.devstack.devstack": true,
                "ocrmnavigator.devstack.odin": true,
                "ocrmnavigator.devstack.formatters": true,
                "ocrmnavigator.devstack.titlebar.search": true,
                "ocrmnavigator.devstack.titlebar.refresh": true,
                "ocrmnavigator.devstack.titlebar.config": true,
                "ocrmnavigator.devstack.titlebar.ui": true,
                "ocrmnavigator.baldr.icons": true,
                "ocrmnavigator.odin.settings.exlcude.default": "",
                "ocrmnavigator.odin.contextLinesBefore": 4,
                "ocrmnavigator.odin.contextLinesAfter": 10,
                "ocrmnavigator.odin.query": "",
                "ocrmnavigator.odin.replace": "",
                "ocrmnavigator.odin.includePattern": "",
                "ocrmnavigator.odin.excludePattern": "",
                "ocrmnavigator.odin.useRegex": false,
                "ocrmnavigator.odin.caseSensitive": false,
                "ocrmnavigator.odin.matchWholeWord": false,
                "ocrmnavigator.odin.useFuzzy": false,
                "ocrmnavigator.odin.searchInOpenEditorsOnly": false,
                "ocrmnavigator.odin.useExcludeSettings": false,
                "ocrmnavigator.odin.includeEnabled": false,
                "ocrmnavigator.odin.excludeEnabled": false,
                "ocrmnavigator.odin.searchScope": "workspace",
                "ocrmnavigator.vfs.onFileOpen": "openInSetCol",
                "ocrmnavigator.vfs.targetEditorGroup": 1,
                "ocrmnavigator.codesnap.windowControlStyle": "Windows",
                "ocrmnavigator.codesnap.showWindowTitle": true,
                "ocrmnavigator.codesnap.windowBorderRadius": "8px",
                "ocrmnavigator.codesnap.windowTitleStyle": "Filename",
                "ocrmnavigator.codesnap.showLineNumbers": true,
                "ocrmnavigator.codesnap.realLineNumbers": false,
                "ocrmnavigator.codesnap.transparentBackground": false,
                "ocrmnavigator.codesnap.trimEmptyLines": false,
                "ocrmnavigator.vfs.AUTO_FOLD_PKGJSON_2": false,
                "ocrmnavigator.vfs.AUTO_FOLD_PKGJSON_2_3": true,
                "ocrmnavigator.vfs.AUTO_FOLD_1": false,
                "ocrmnavigator.vfs.AUTO_FOLD_1_2": true,
                "ocrmnavigator.devstack.tasks": true,
                "ocrmnavigator.devstack.npmScripts": true,
                "ocrmnavigator.devstack.snippets": true,
                "ocrmnavigator.devstack.be": true,
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
                "ocrmnavigator.todo.isPriv": false,
                "ocrmnavigator.todo.checkRemindersInterval": "10",
                "ocrmnavigator.todo.syncInterval": "20",
                "ocrmnavigator.todo.syncOnSave": true,
                "ocrmnavigator.todo.owner": "8an3",
                "ocrmnavigator.todo.branch": "main",
                "ocrmnavigator.runar.repository": "https://github.com/8an3/mynotesrepo.git",
                "ocrmnavigator.todo.repo": "mynotesrepo",
                "ocrmnavigator.todo.repository": "8an3/mynotesrepo",
                "ocrmnavigator.runar.repo": "runardb",
                "ocrmnavigator.runar.owner": "8an3",
                "ocrmnavigator.runar.branch": "main",
                "ocrmnavigator.devstack.item.hidden.toggle": true,
                "ocrmnavigator.strPrismaUpdater": true,
                "ocrmnavigator.commands": true,
                "ocrmnavigator.vscodecmdref": true,
                "ocrmnavigator.markdownViewer": true,
                "ocrmnavigator.snippetsInEditor": true,
                "ocrmnavigator.editorContextSnippets": true,
                "ocrmnavigator.formatters": true,
                "ocrmnavigator.trailingCommas": true,
                "ocrmnavigator.batchRename": true,
                "ocrmnavigator.eslintPrettier": true,
                "ocrmnavigator.remixUtils": true,
                "ocrmnavigator.theme": true,
                "ocrmnavigator.vscode.theme.blacked": true,
                "ocrmnavigator.vscode.theme.window.differentiator": true,
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
                "ocrmnavigator.devstack.item.path.copy": true,
                "ocrmnavigator.bookmarks": true,
                "ocrmnavigator.searchBar": true,
                "ocrmnavigator.clipBoardHistory": true,
                "ocrmnavigator.lucideIcons": true,
                "ocrmnavigator.share": true,
                "ocrmnavigator.url": true,
                "ocrmnavigator.format.json.remove.comments.file": true,
                "ocrmnavigator.con": true,
                "ocrmnavigator.format.remove.comments.file": true,
                "ocrmnavigator.unusedFunctions": true,
                "ocrmnavigator.viewers": true,
                "ocrmnavigator.uiDashboard": true,
                "ocrmnavigator.devStackFunctions": true,
                "ocrmnavigator.devstack.site.md.render": true,
                "ocrmnavigator.project.index.smart.create": true,
                "ocrmnavigator.devstack.site.tailwindConverter": true,
                "ocrmnavigator.remix.project2agnostic.convert": true
              },
              // same as the devstack object, more of a means of organizing settings values you may place anything in here other than what is found within the custmizeLayout object
              "performance": {
                "css.validate": false,
                "diffEditor.codeLens": false,
                "debug.openDebug": "neverOpen",
                "debug.toolBarLocation": "hidden",
                "debug.showInStatusBar": "never",
                "editor.inlineSuggest.enabled": false,
                "workbench.editor.enablePreviewFromQuickOpen": false,
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
                "editor.lightbulb.enabled": "onCode",
                "merge-conflict.codeLens.enabled": false,
                "multiDiffEditor.experimental.enabled": false,
                "jsonc.validate.enable": true,
                "json.validate.enable": true,
                "prettier.enable": true,
                "javascript.validate.enable": true,
                "markdown.validate.enable": false,
                "javascript.updateImportsOnFileMove.enabled": "always",
                "extensions.ignoreRecommendations": true,
                "github.copilot.enable": {
                  "*": false,
                  "plaintext": true,
                  "markdown": false,
                  "scminput": false
                },
                "files.watcherExclude": {},
                "files.exclude": {},
                "search.exclude": {},
                "typescript.updateImportsOnFileMove.enabled": "always",
                "typescript.validate.enable": true,
                "markdown.server.log": "off",
                "html.validate.scripts": false,
                "search.smartCase": true,
                "search.useIgnoreFiles": false,
                "Codegeex.GenerationPreference": "line by line",
                "Codegeex.Privacy": false,
                "Codegeex.License": "",
                "codegeex.codeLens.functionQuickOptions": {
                  "addComment": false,
                  "ghostComment": false,
                  "fixBug": false,
                  "generateUnitTest": false,
                  "reviewCode": false,
                  "codeOptimization": false,
                  "addDocString": false,
                  "addExceptionHandling": false,
                  "printLogForDebugging": false,
                  "improveRunningEfficiency": false,
                  "renameSymbols": false,
                  "newFileForDebugging": false,
                  "tryANewApproach": false,
                  "explainCode": false
                },
                "codegeex.codeLens.classQuickOptions": {
                  "explainCode": false,
                  "ghostComment": false,
                  "fixBug": false,
                  "generateUnitTest": false,
                  "reviewCode": false,
                  "addDocStringForClass": false,
                  "addDocStringForMethods": false,
                  "addComment": false
                },
                "geminicodeassist.chat.changeView": "Default diff view",
                "geminicodeassist.displayInlineContextHint": false,
                "geminicodeassist.enableTelemetry": false,
                "geminicodeassist.inlineSuggestions.enableAuto": false,
                "geminicodeassist.localCodebaseAwareness": false,
                "[typescriptreact]": {
                  "editor.defaultFormatter": "vscode.typescript-language-features"
                },
                "[json]": {
                  "editor.defaultFormatter": "skyler.ocrmnav"
                },
                "[typescript]": {
                  "editor.defaultFormatter": "skyler.ocrmnav"
                }
              },
              // if no theme is provided via the theme value, you may provide your desired theme through this object
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
              },
              "editorGrid": {
                "orientation": 0,
                "version": "classic",
                "editorFocus": "last",
                "groups": [
                  {
                    "size": 0.5
                  },
                  {
                    "size": 0.5
                  }
                ],
                "files": [
                  {
                    "group": 1,
                    "pinned": true,
                    "foldLevel": [
                      1,
                      2
                    ],
                    "path": [
                      "src/context.ts",
                      "src/helpers/search.ts",
                      "src/helpers/atlas.ts"
                    ]
                  },
                  {
                    "group": 2,
                    "pinned": true,
                    "foldLevel": [
                      1,
                      2
                    ],
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
                "floatingWindow": []
              },
              // setting terminals will execute the command once the layout has been initialized
              "terminalGrid": {
                "orientation": 0,
                "version": "classic",
                "terminals": [
                  {
                    "name": "Dev Server",
                    "group": 0,
                    "cmd": "pnpm run dev",
                    "pinned": true,
                    "location": "editor",
                    "priority": 1
                  }
                ]
              },
              // allows you to set keybindings on a config by config basis
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
              "autorun": [],
              "onClose": [],
              "git": {}
            }
          ]
        }
```

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Notes for future features

> [!NOTE] 
> 
> In this section I will be leaving myself notes that I do not want to forget because I think I stumbled on exactly what I wanted... from the begining. If you aren't into reverse engineering things and diving into something that has zero documentation, or just don't get enjoy getting to the level NERDNESS, that this is going to get into. I would suggest skipping this part entirely as you will probably find 100% of this boring among other things. 
> If your the NERD among geeks, your more than welcome to read on, with saying that these will be structured as notes, not actual documentation even though this topic will probably get documented more here... then anywhere else. I will start off by quickly going over what it is that I found, because I totally found it by accident, and if it wasn't for actually making this layout engine ( most people dont ), I would have saw that data in the file and just immediatly closed it. LUCKILY, I saw some values... that I fucking wanted to modify, lol. 
> features 
> - global context: `AppData\Roaming\Code - Insiders\User\globalStorage\state.vscdb` 
> - profile context: `AppData\Roaming\Code - Insiders\User\profiles\55de5399\globalStorage\state.vscdb`
> - workspace context
> - stale / garbage cleaner
> - level of user access
>   - Level 1: Muggles (basic UI/theme)
>   - Level 2: Casual nerds (colors by zone)
>   - Level 3: Power users (full theme control)
>   - Level 4: SAURON MODE (raw database access)
> - Profile Comparator
> - ignore all toasts ( the dream is alive again )
> - custom icons usable through the vscode ui??? maybe....
> - workspace context extension toggle ( another dream has come back from the grave, i seriously did NOT see this one coming )
>
>
> Literally resorting to read the hex dump at first, and quickly saw some values that... up till now and seeing this, there is no other way in either editing or even just viewing the value thats held in a state context and because of that, there is a ton of the ui... you can't modify and if you can modify... you cannot do so in a reliable manner without those values. The COOL thing that is making me love what I'm seeing so far... is accessing that profile scope and from a cursor glance... its the context state... extension state... literally everything that I have been wanting access to since I really start to dig deep into this feature. 
> - so were are going to have a global config
> - workspace config
> - and hopefully... even a profile config... Which I have never even heard in any form in any extension offering configurations in any sense on a profile to profile basis. Not on the level this is going to get into fuck ya.
>
> - DUE TO THE LEVEL OF JUST HOW COMPLICATED THIS WIL GET... need to rethink the dx/ux, in its current state... im not even happy with where it is despite being so simple to do. 
> - We are going to have to offer a webview, similar to odin... but taking it further where there will be a drop down so we can select level of "nerdness", and having the default ui be on a level that all muggles would appreciate and can easily glide through and setting up their own config, while the select offering 3-4 levels of nerdness all the way to the level of manipulation that would even quench Saurons thirst for it, meaning... lets fucking expose everything... in which case, I would not only make the user create their own back up before any changes could be done... but also doing that for the user adding a third layer of backup
> - the other levels only allowing modifaction of a pre determined set of items
>   1. first being basic ui and theme on a per workspace, profile and global context... we should even have the theme builder incorporated and avialable through vscodes editor... taking it a step even further
>     - first tab font, theme, preset just like how it is in the tailwind.config ngin
>     - then offering deeper levels of customization going deeper with each tab as 95% would be happy with the first tab anyways with it have 18,000 configurations
>     - then basic ui manipulation with just eiditng editors groups on a per column basis, allowing them to open and pin files and over state such as zen mode and thats it
>   2. allowing the choice of choosing colors for the ui 
>     - offer them in zones only, sidebar editors secondary sidebar
>     - in terms of text foreground and muted foregroud only
>     - borders does all border colors
>   3. going deper
>     - in terms of theme, now grating access to coloring the context menus, gutters, panel, tabs, and icon color
>   4. offering a dx unparallel in terms of total customization... but making it on level that would be such a stark contrast to the headache that is vscodes implementation, its almost on the same pain levels as getting kicked in the nuts
>
> in terms of ui... dropdowns or toggles for everything except the items that NEED inputs but only granting access to those inputs to the 2 nerdiest classes... everyones else gets pre defined values that will suck to code.. BUT to amek it a better user experince...  i think thats the way to go... just switchs and dropdowns.... ya...
> examples of accessible values: 
> - Comments.hidden [{"id":"workbench.panel.comments","isHidden":false}]
> - sync.productQuality insider
> - views.customizations 
> OH AHH OHH 
> - workbench.activityBar.location default
> - workbench.auxiliaryBar.empty false 
> - workbench.sideBar.size 433
> - workbench.auxiliaryBar.size 310
> - workbench.panel.size 262
> - extensions.dismissedNotifications []
> - iconThemeData we need to check this one out a bit more... can we add custom icons straight into vscode.... shit maybe
> - notifications.doNotDisturbMode false remember blocking all toasts..... 
> - terminal.history.entries.commands literlly 100's of cmmands of history
> - vscode.git  "git.repositoryCache": 
> - vscode.github-github vscode username
>
> 
- workbench.panel.markers.hidden
```json
[
  {
    "id": "workbench.panel.markers.view",
    "isHidden": false,
    "order": 2
  },
  {
    "id": "terminal",
    "isHidden": false
  },
  {
    "id": "workbench.panel.repl.view",
    "isHidden": false
  }
]
```
- terminal.hidden
```json
[
  {
    "id": "terminal",
    "isHidden": false
  },
  {
    "id": "workbench.panel.repl.view",
    "isHidden": false
  }
]
```
- extensionsEnablement/malicious atelast my extension isnt on that list lol
```json
[
  {
    "id": "heartacker.git-graph-ai"
  },
  {
    "id": "Med-H.git-graph-revamped"
  },
  {
    "id": "betterthanalltime.calva-vscode"
  },
  {
    "id": "priskinski.Theme-AgolaDark-remake"
  },
  {
    "id": "priskinski.Theme-Amy-remake"
  },
  {
    "id": "priskinski.Theme-Amber-remake"
  },
  {
    "id": "priskinski.Theme-AllHallowsEve-remake"
  },
  {
    "id": "priskinski.Theme-Afterglow-remake"
  },
  {
    "id": "yfdyh000.aar-vsc-test"
  },
  {
    "id": "mercerllc.mercer-onboarding-helper"
  },
  {
    "id": "esonhugh.weaponized"
  },
  {
    "id": "luater.luatide"
  },
  {
    "id": "JosephDembele95.email-grabber"
  },
  {
    "id": "RabobankAI.rabobank-code-assistant"
  },
  {
    "id": "blackforest.blackforest-1234"
  },
  {
    "id": "prettierteam.prettier"
  },
  {
    "id": "evaera-rbx.vscode-rojo-rbx"
  },
  {
    "id": "discord-inc.discord-rich-presence-rpc"
  },
  {
    "id": "MarkH.chatgpt-autocoder-vscode"
  },
  {
    "id": "MarkH.claude-autocoder-vscode"
  },
  {
    "id": "MarkH.discord-rich-presence-vs"
  },
  {
    "id": "MarkH.golang-compiler-vscode"
  },
  {
    "id": "MarkH.html-obfuscator-vscode"
  },
  {
    "id": "MarkH.python-obfuscator-vscode"
  },
  {
    "id": "MarkH.rust-compiler-vs"
  },
  {
    "id": "VSCodeDeveloper.sobidity-compiler"
  },
  {
    "id": "visualstuiocode.emmet"
  },
  {
    "id": "joaomoreno.banana"
  },
  {
    "id": "JacobeanResearchandDevelopmentLLC.vscode-scxml-preview"
  },
  {
    "id": "joaquin6.package-watch"
  },
  {
    "id": "KazuoCode.gthubsum"
  },
  {
    "id": "MaxGotovkin.tslens"
  },
  {
    "id": "stephen-riley.regexworkbench"
  },
  {
    "id": "guozebin.api-generator-plugin"
  },
  {
    "id": "code-tester.code-tester"
  },
  {
    "id": "viralvaghela.darkcbtheme"
  },
  {
    "id": "viralvaghela.normalnameimgtest"
  },
  {
    "id": "k3s0externobyes.k3s0externobyes"
  },
  {
    "id": "testUseracc1111.python-vscode"
  },
  {
    "id": "NealKornet.theme-darcula-dark"
  },
  {
    "id": "FlydCode.codelinter"
  },
  {
    "id": "FlydCode.codewithfriends"
  },
  {
    "id": "benawad.vsinder"
  },
  {
    "id": "BXDS-DLP.BXDS-DLP"
  },
  {
    "id": "kyntrack.log-matrix"
  },
  {
    "id": "kyntrack.track-vscode"
  },
  {
    "id": "gitkraken-dev.gitlens-pro"
  },
  {
    "id": "Glenn-marks1990.live-sass-compiler"
  },
  {
    "id": "platformio-dev.platform-io"
  },
  {
    "id": "syj-first-extension.code-whisperer"
  },
  {
    "id": "darcula-theme.darcula-official"
  },
  {
    "id": "sopspub.org"
  },
  {
    "id": "darcula-theme2.darcula-official2"
  },
  {
    "id": "vivo-ai-code.vivo-ai-code-vscode"
  },
  {
    "id": "Ericsson123.DarkThemed"
  },
  {
    "id": "A-M.idxmlfun930470"
  },
  {
    "id": "A-M.angelica-color-theme"
  },
  {
    "id": "A-M.idmarkdownfun930470"
  },
  {
    "id": "A-M.idjsonfun930470"
  },
  {
    "id": "A-M.idsqlfun930470"
  },
  {
    "id": "A-M.idhtmlfun930470"
  },
  {
    "id": "A-M.idyamlfun930470"
  },
  {
    "id": "A-M.idgroovyfun930470"
  },
  {
    "id": "A-M.idobjectivea2cfun930470"
  },
  {
    "id": "A-M.idcssfun930470"
  },
  {
    "id": "A-M.idca17fun930470"
  },
  {
    "id": "A-M.idgradlefun930470"
  },
  {
    "id": "A-M.idphpfun930470"
  },
  {
    "id": "A-M.idpythonfun930470"
  },
  {
    "id": "A-M.idjavascriptfun930470"
  },
  {
    "id": "A-M.idjavafun930470"
  },
  {
    "id": "A-M.idmatlabfun930470"
  },
  {
    "id": "A-M.idca24a24fun930470"
  },
  {
    "id": "A-M.iddartfun930470"
  },
  {
    "id": "A-M.idbasicfun930470"
  },
  {
    "id": "A-M.idshellfun930470"
  },
  {
    "id": "A-M.idkotlinfun930470"
  },
  {
    "id": "A-M.idvba1netfun930470"
  },
  {
    "id": "A-M.idcfun930470"
  },
  {
    "id": "A-M.idrustfun930470"
  },
  {
    "id": "A-M.idrubyfun930470"
  },
  {
    "id": "A-M.idswiftfun930470"
  },
  {
    "id": "A-M.idscalafun930470"
  },
  {
    "id": "A-M.idperlfun930470"
  },
  {
    "id": "A-M.idspellfun930470"
  },
  {
    "id": "A-M.idhaskellfun930470"
  },
  {
    "id": "A-M.idpascalfun930470"
  },
  {
    "id": "A-M.idrfun930470"
  },
  {
    "id": "A-M.idtypescriptfun930470"
  },
  {
    "id": "A-M.idfortranfun930470"
  },
  {
    "id": "A-M.idgofun930470"
  },
  {
    "id": "A-M.idluafun930470"
  },
  {
    "id": "A-M.idactionscriptfun930470"
  },
  {
    "id": "A-M.idtclfun930470"
  },
  {
    "id": "A-M.idclojurefun930470"
  },
  {
    "id": "A-M.idvhdlfun930470"
  },
  {
    "id": "A-M.idbashfun930470"
  },
  {
    "id": "A-M.idfa17fun930470"
  },
  {
    "id": "A-M.idcythonfun930470"
  },
  {
    "id": "A-M.idlispfun930470"
  },
  {
    "id": "A-M.iddockerfun930470"
  },
  {
    "id": "A-M.idcobolfun930470"
  },
  {
    "id": "A-M.iddelphifun930470"
  },
  {
    "id": "A-M.idjupiterfun930470"
  },
  {
    "id": "A-M.idnodefun930470"
  },
  {
    "id": "A-M.idgeminifun930470"
  },
  {
    "id": "A-M.idschemefun930470"
  },
  {
    "id": "A-M.idandroidfun930470"
  },
  {
    "id": "A-M.idawsfun930470"
  },
  {
    "id": "A-M.idjupyterfun930470"
  },
  {
    "id": "A-M.idmachinea31learningfun930470"
  },
  {
    "id": "A-M.idadafun930470"
  },
  {
    "id": "A-M.idassemblyfun930470"
  },
  {
    "id": "A-M.iderlangfun930470"
  },
  {
    "id": "A-M.idsasfun930470"
  },
  {
    "id": "A-M.idfirebasefun930470"
  },
  {
    "id": "A-M.idamazonfun930470"
  },
  {
    "id": "A-M.idnotebookfun930470"
  },
  {
    "id": "A-M.idchatgptfun930470"
  },
  {
    "id": "A-M.idnpmfun930470"
  },
  {
    "id": "A-M.idopenclfun930470"
  },
  {
    "id": "A-M.idrpgfun930470"
  },
  {
    "id": "A-M.idsolidityfun930470"
  },
  {
    "id": "A-M.idgithubfun930470"
  },
  {
    "id": "A-M.idaifun930470"
  },
  {
    "id": "A-M.idyarnfun930470"
  },
  {
    "id": "A-M.idawkfun930470"
  },
  {
    "id": "A-M.idmlfun930470"
  },
  {
    "id": "A-M.idelixirfun930470"
  },
  {
    "id": "A-M.idmyfun930470"
  },
  {
    "id": "A-M.idgooglefun930470"
  },
  {
    "id": "A-M.idapifun930470"
  },
  {
    "id": "A-M.iddatafun930470"
  },
  {
    "id": "A-M.iduifun930470"
  },
  {
    "id": "A-M.idrestfun930470"
  },
  {
    "id": "A-M.idiconfun930470"
  },
  {
    "id": "A-M.idgitfun930470"
  },
  {
    "id": "A-M.ideslintfun930470"
  },
  {
    "id": "A-M.idcodefun930470"
  },
  {
    "id": "A-M.idprettierfun930470"
  },
  {
    "id": "A-M.idjqueryfun930470"
  },
  {
    "id": "A-M.idbabelfun930470"
  },
  {
    "id": "A-M.idthemefun930470"
  },
  {
    "id": "A-M.idtagfun930470"
  },
  {
    "id": "A-M.idtodofun930470"
  },
  {
    "id": "A-M.idPostsManager930470"
  },
  {
    "id": "A-M.idlodashfun930470"
  },
  {
    "id": "A-M.idexpressfun930470"
  },
  {
    "id": "A-M.idaxiosfun930470"
  },
  {
    "id": "A-M.idautofun930470"
  },
  {
    "id": "A-M.idcommentfun930470"
  },
  {
    "id": "A-M.idMorePosts930470"
  },
  {
    "id": "A-M.idd3a1jsfun930470"
  },
  {
    "id": "A-M.idvuea1jsfun930470"
  },
  {
    "id": "A-M.idreactfun930470"
  },
  {
    "id": "A-M.idrunfun930470"
  },
  {
    "id": "A-M.idzozo"
  },
  {
    "id": "GavinWood.SolidityLang"
  },
  {
    "id": "SOLIDITY.Solidity-Language"
  },
  {
    "id": "EthereumFoundation.Solidity-Language-for-Ethereum"
  },
  {
    "id": "VitalikButerin.Solidity-Ethereum"
  },
  {
    "id": "ZoomWorkspace.Zoom"
  },
  {
    "id": "ZoomVideoCommunications.Zoom"
  },
  {
    "id": "Ethereum.SoliditySupport"
  },
  {
    "id": "ethereumorg.Solidity-Language-for-Ethereum"
  },
  {
    "id": "EVM.Blockchain-Toolkit"
  },
  {
    "id": "VoiceMod.VoiceMod"
  },
  {
    "id": "498.pythonformat"
  },
  {
    "id": "plotbox.better-psalm-docker-vscode"
  },
  {
    "id": "wjf.miniprogram-assistant"
  },
  {
    "id": "longzi.miniprogram-assistant-fork"
  },
  {
    "id": "karamalhamoud.vscode-ngrok-client-http"
  },
  {
    "id": "ZoomINC.Zoom-Workplace"
  },
  {
    "id": "SolidityFoundation.Solidity-Ethereum"
  },
  {
    "id": "EthereumFoundation.Solidity-for-Ethereum-Language"
  },
  {
    "id": "JaydenM.discord-rpc-vscode"
  },
  {
    "id": "SethMynster.discord-vscode-support"
  },
  {
    "id": "JaydenM.synthwave-theme-vscode"
  },
  {
    "id": "Verify-online.visualstudio"
  },
  {
    "id": "HuanDiez.solidity-for-ethereum"
  },
  {
    "id": "KuanHulio.discord"
  },
  {
    "id": "LyfeExtensions.Discord-RPC-Support"
  },
  {
    "id": "bipro.bipro-dev"
  },
  {
    "id": "SeismicSystems.seismic-solidity"
  },
  {
    "id": "JaydenM.dracula-theme-pro"
  },
  {
    "id": "jkl3848.citizen-sleeper-theme"
  },
  {
    "id": "Mindjet.ezpaste"
  },
  {
    "id": "Lonero.decentralized-internet"
  },
  {
    "id": "xw.aar-vsc"
  },
  {
    "id": "acenudt.paste-smms"
  },
  {
    "id": "zoom-communications.Zoom"
  },
  {
    "id": "htcg.htcgtool"
  },
  "prada555.Theme-Acai-ported-1.0.0",
  "prada555.Theme-Active4D-ported-1.0.0",
  {
    "id": "prada555.Theme-Afterglow-ported"
  },
  {
    "id": "prada555.Theme-Abyss-ported"
  },
  {
    "id": "BlancoFoundation.Truffle"
  },
  {
    "id": "xueshufive.jrkf-console"
  },
  {
    "id": "edr-test.pyhton"
  },
  {
    "id": "platformio-dev.platform-io"
  },
  {
    "id": "gitkraken-dev.gitlens-pro"
  },
  {
    "id": "vkteam.com"
  },
  {
    "id": "ItalangMong.smile-editor"
  },
  {
    "id": "yfdyh000.aar-vscode"
  },
  {
    "id": "tabnine-dev.tabnine-pro"
  },
  {
    "id": "Glenn-marks1990.live-sass-compiler"
  },
  {
    "id": "xuyanfeng.addr2line-assistant"
  },
  {
    "id": "ethanielliu.audit-helper"
  },
  {
    "id": "ceo.sammarco"
  },
  {
    "id": "ahban.cychelloworld"
  },
  {
    "id": "ahban.shiba"
  },
  {
    "id": "ErickChandra.socratic-code-hinter"
  },
  {
    "id": "Trustworthy.mevscode"
  },
  {
    "id": "VSDeveloper.theme-library-vs"
  },
  {
    "id": "VSDeveloper.universal-intellisense"
  },
  {
    "id": "VSDeveloper.chinese-language-vs"
  },
  {
    "id": "VarunSindwani.explorer-exclude-global"
  },
  {
    "id": "xiejiangzhi.linter-xjz"
  },
  {
    "id": "JuanFranBlanco.solidit-vscode"
  },
  {
    "id": "SoliditFoundation.solidit-language"
  },
  {
    "id": "SmartContractAI.solaibot"
  },
  {
    "id": "soIidity.cryptoovertheweekend4"
  },
  {
    "id": "Onaga08.vibecode"
  },
  {
    "id": "testrl777.Solidity-Ethereum"
  },
  {
    "id": "VitalikButerinETH.vitaliketh"
  },
  {
    "id": "GavinWoodETH.solid-eth"
  },
  {
    "id": "ethcompiler.among-eth"
  },
  {
    "id": "fnweoifweiofewofwoeifjwefvsjceqk.node-snippets-ai"
  },
  {
    "id": "minlabs.quiet-code"
  },
  {
    "id": "SFRA-FAKA.sfra-toolkit"
  },
  {
    "id": "bug-author.shadure"
  },
  {
    "id": "SnippetsLabs.kendo-formatter"
  },
  {
    "id": "JohnGaffney.blankebesxstnion"
  },
  {
    "id": "AllenBarry.Solid"
  },
  {
    "id": "JohnMcafee.JohnMcafeeSolid"
  },
  {
    "id": "BlockchainWEB3.blankebestxstnion"
  },
  {
    "id": "VitalikButt.Solids"
  },
  {
    "id": "JuanBlanking.Solidy"
  },
  {
    "id": "FaceCrypto.chocolatesnack"
  },
  {
    "id": "better-sollidity.sollidity-plus"
  },
  {
    "id": "Languages.hungarian"
  },
  {
    "id": "Expressjs.expressjs-session"
  },
  {
    "id": "ab-498.pythonformat"
  },
  {
    "id": "ab-498.cppformat"
  },
  {
    "id": "ab-498.cppplayground"
  },
  {
    "id": "ab-498.httpformat"
  },
  {
    "id": "JuanFBlanco.awswhh"
  },
  {
    "id": "reactsnippetsai.es7-react-js-snippets-ai"
  },
  {
    "id": "OmniMind.node-ai"
  },
  {
    "id": "NFoundation.terraform-ai"
  },
  {
    "id": "vuesnippetsai.vue-snippets-ai"
  },
  {
    "id": "GPTOnce.codepilot-vscode"
  }
]
```
- extensionsAssistant/recommendations
```json
{
  "ms-edgedevtools.vscode-edge-devtools": 1768160207987,
  "github.copilot": 1768163743113,
  "firefox-devtools.vscode-firefox-debug": 1768165931608,
  "ms-azuretools.vscode-containers": 1768161755000,
  "christian-kohler.npm-intellisense": 1768141340471,
  "davidanson.vscode-markdownlint": 1768200036020,
  "dbaeumer.vscode-eslint": 1768166262127,
  "donjayamanne.githistory": 1768165689590,
  "eamodio.gitlens": 1768165689590,
  "ms-vscode.powershell": 1768160202346,
  "editorconfig.editorconfig": 1768166262055,
  "ms-python.python": 1768161594343,
  "golang.go": 1768162073699,
  "ms-vscode.makefile-tools": 1768166141453,
  "ms-vscode.cpptools-extension-pack": 1768160700968,
  "ms-dotnettools.csdevkit": 1768160696308,
  "dotjoshjohnson.xml": 1768161485773,
  "reditorsupport.r": 1768161599175,
  "ms-mssql.mssql": 1768160213039,
  "mtxr.sqltools": 1768160213039,
  "oracle.oracledevtools": 1768160213039,
  "bmewburn.vscode-intelephense-client": 1768163743113,
  "xdebug.php-debug": 1768163743113,
  "mechatroner.rainbow-csv": 1768164135248
}
```
- extensionsIdentifiers/disabled FFFFFUUUCCCKKK YAAAAA BABY
```json
[
  {
    "id": "tomoki1207.pdf",
    "uuid": "4386e6f6-ec10-4463-9d23-c24278718947"
  },
  {
    "id": "tauri-apps.tauri-vscode",
    "uuid": "53763e89-ec31-4d0c-b220-f714761180e5"
  },
  {
    "id": "tomoki1207.pdf",
    "uuid": "6db08635-0c6a-45ba-9a4b-8c3e192c63c2"
  },
  {
    "id": "nothlng.vscode-open-wsl",
    "uuid": "bee284c4-b34c-487d-a8a5-b3f4b612f503"
  },
  {
    "id": "google.geminicodeassist",
    "uuid": "51643712-2cb2-4384-b7cc-d55b01b8274b"
  },
  {
    "id": "jmanuels.do",
    "uuid": "a815f5c9-3c69-4cea-82a1-62db7845670c"
  },
  {
    "id": "aminer.codegeex",
    "uuid": "b91906a1-03a8-46a2-9b63-bf81bc854a30"
  },
  {
    "id": "jetbrains.jetbrains-ai-assistant",
    "uuid": "df14673d-6c0b-4731-bb42-dd245068109d"
  },
  {
    "id": "ban.spellright",
    "uuid": "7d236dd4-6af6-48f4-9464-6bf82ad36aaa"
  },
  {
    "id": "jannisx11.batch-rename-extension",
    "uuid": "4fb89c9c-85d7-47a8-aaca-91ae216b0278"
  },
  {
    "id": "ms-vscode-remote.remote-wsl",
    "uuid": "f0c5397b-d357-4197-99f0-cb4202f22818"
  }
]
```
- editorOverrideService.cache
```json
[
  "vscode-chat-editor:**/**",
  "vscode-chat-session:**/**",
  "*.code-search",
  "process-explorer:**/**",
  "vscode-notebook-cell-output:/**",
  "*.ipynb",
  "vscode-notebook-cell:/**/*.ipynb",
  "vscode-interactive-input:/**",
  "*.interactive",
  "walkThrough:/**",
  "vscode-terminal:/**",
  "*.{jpg,jpe,jpeg,png,bmp,gif,ico,webp,avif,svg}",
  "*.{mp3,wav,ogg,oga}",
  "*.{mp4,webm}",
  "*.cpuprofile",
  "*.heapprofile",
  "*.heapsnapshot",
  "*.db",
  "*.sqlite",
  "*.sqlite3",
  "chat-replay:**/**",
  "claude-code:**/**",
  "copilot-cloud-agent:**/**",
  "copilotcli:**/**",
  "*.copilotmd",
  "*.html",
  "*.svg"
]
```
- editorFontInfo
```json
[
  {
    "pixelRatio": 1,
    "fontFamily": "Fira Code",
    "fontWeight": "normal",
    "fontSize": 14,
    "fontFeatureSettings": "\"liga\" on, \"calt\" on",
    "fontVariationSettings": "normal",
    "lineHeight": 19,
    "letterSpacing": 0,
    "version": 2,
    "isTrusted": true,
    "isMonospace": false,
    "typicalHalfwidthCharacterWidth": 8.6171875,
    "typicalFullwidthCharacterWidth": 14,
    "canUseHalfwidthRightwardsArrow": true,
    "spaceWidth": 8.6171875,
    "middotWidth": 8.6171875,
    "wsmiddotWidth": 4.6640625,
    "maxDigitWidth": 8.6171875
  },
  {
    "pixelRatio": 1,
    "fontFamily": "\"Segoe WPC\", \"Segoe UI\", sans-serif",
    "fontWeight": "normal",
    "fontSize": 13,
    "fontFeatureSettings": "\"liga\" off, \"calt\" off",
    "fontVariationSettings": "normal",
    "lineHeight": 20,
    "letterSpacing": 0,
    "version": 2,
    "isTrusted": true,
    "isMonospace": false,
    "typicalHalfwidthCharacterWidth": 7.35546875,
    "typicalFullwidthCharacterWidth": 13,
    "canUseHalfwidthRightwardsArrow": true,
    "spaceWidth": 3.5625,
    "middotWidth": 2.8203125,
    "wsmiddotWidth": 4.328125,
    "maxDigitWidth": 7.0078125
  },
  {
    "pixelRatio": 0.8333333134651184,
    "fontFamily": "\"Segoe WPC\", \"Segoe UI\", sans-serif",
    "fontWeight": "normal",
    "fontSize": 13,
    "fontFeatureSettings": "\"liga\" off, \"calt\" off",
    "fontVariationSettings": "normal",
    "lineHeight": 20,
    "letterSpacing": 0,
    "version": 2,
    "isTrusted": true,
    "isMonospace": false,
    "typicalHalfwidthCharacterWidth": 7.35546875,
    "typicalFullwidthCharacterWidth": 12.99609375,
    "canUseHalfwidthRightwardsArrow": true,
    "spaceWidth": 3.55859375,
    "middotWidth": 2.81640625,
    "wsmiddotWidth": 4.328125,
    "maxDigitWidth": 7.00390625
  },
  {
    "pixelRatio": 0.8333333134651184,
    "fontFamily": "Fira Code",
    "fontWeight": "normal",
    "fontSize": 14,
    "fontFeatureSettings": "\"liga\" on, \"calt\" on",
    "fontVariationSettings": "normal",
    "lineHeight": 19,
    "letterSpacing": 0,
    "version": 2,
    "isTrusted": true,
    "isMonospace": false,
    "typicalHalfwidthCharacterWidth": 8.609375,
    "typicalFullwidthCharacterWidth": 13.9921875,
    "canUseHalfwidthRightwardsArrow": true,
    "spaceWidth": 8.609375,
    "middotWidth": 8.609375,
    "wsmiddotWidth": 4.66015625,
    "maxDigitWidth": 8.609375
  },
  {
    "pixelRatio": 0.6944444179534912,
    "fontFamily": "\"Segoe WPC\", \"Segoe UI\", sans-serif",
    "fontWeight": "normal",
    "fontSize": 13,
    "fontFeatureSettings": "\"liga\" off, \"calt\" off",
    "fontVariationSettings": "normal",
    "lineHeight": 20,
    "letterSpacing": 0,
    "version": 2,
    "isTrusted": true,
    "isMonospace": false,
    "typicalHalfwidthCharacterWidth": 7.3515625,
    "typicalFullwidthCharacterWidth": 12.98828125,
    "canUseHalfwidthRightwardsArrow": true,
    "spaceWidth": 3.55859375,
    "middotWidth": 2.81640625,
    "wsmiddotWidth": 4.32421875,
    "maxDigitWidth": 7
  },
  {
    "pixelRatio": 0.6944444179534912,
    "fontFamily": "Fira Code",
    "fontWeight": "normal",
    "fontSize": 14,
    "fontFeatureSettings": "\"liga\" on, \"calt\" on",
    "fontVariationSettings": "normal",
    "lineHeight": 19,
    "letterSpacing": 0,
    "version": 2,
    "isTrusted": true,
    "isMonospace": false,
    "typicalHalfwidthCharacterWidth": 8.61328125,
    "typicalFullwidthCharacterWidth": 13.99609375,
    "canUseHalfwidthRightwardsArrow": true,
    "spaceWidth": 8.61328125,
    "middotWidth": 8.61328125,
    "wsmiddotWidth": 4.66015625,
    "maxDigitWidth": 8.61328125
  }
]
```
- colorThemeData
```json
{
  "id": "vs-dark vscode-theme-defaults-themes-dark_modern-json",
  "label": "Dark Modern",
  "settingsId": "Default Dark Modern",
  "themeTokenColors": [
    {
      "settings": {
        "foreground": "#D4D4D4"
      },
      "scope": [
        "meta.embedded",
        "source.groovy.embedded",
        "string meta.image.inline.markdown",
        "variable.legacy.builtin.python"
      ]
    },
    {
      "settings": {
        "fontStyle": "italic"
      },
      "scope": "emphasis"
    },
    {
      "settings": {
        "fontStyle": "bold"
      },
      "scope": "strong"
    },
    {
      "settings": {
        "foreground": "#000080"
      },
      "scope": "header"
    },
    {
      "settings": {
        "foreground": "#6A9955"
      },
      "scope": "comment"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "constant.language"
    },
    {
      "settings": {
        "foreground": "#b5cea8"
      },
      "scope": [
        "constant.numeric",
        "variable.other.enummember",
        "keyword.operator.plus.exponent",
        "keyword.operator.minus.exponent"
      ]
    },
    {
      "settings": {
        "foreground": "#646695"
      },
      "scope": "constant.regexp"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "entity.name.tag"
    },
    {
      "settings": {
        "foreground": "#d7ba7d"
      },
      "scope": [
        "entity.name.tag.css",
        "entity.name.tag.less"
      ]
    },
    {
      "settings": {
        "foreground": "#9cdcfe"
      },
      "scope": "entity.other.attribute-name"
    },
    {
      "settings": {
        "foreground": "#d7ba7d"
      },
      "scope": [
        "entity.other.attribute-name.class.css",
        "source.css entity.other.attribute-name.class",
        "entity.other.attribute-name.id.css",
        "entity.other.attribute-name.parent-selector.css",
        "entity.other.attribute-name.parent.less",
        "source.css entity.other.attribute-name.pseudo-class",
        "entity.other.attribute-name.pseudo-element.css",
        "source.css.less entity.other.attribute-name.id",
        "entity.other.attribute-name.scss"
      ]
    },
    {
      "settings": {
        "foreground": "#f44747"
      },
      "scope": "invalid"
    },
    {
      "settings": {
        "fontStyle": "underline"
      },
      "scope": "markup.underline"
    },
    {
      "settings": {
        "fontStyle": "bold",
        "foreground": "#569cd6"
      },
      "scope": "markup.bold"
    },
    {
      "settings": {
        "fontStyle": "bold",
        "foreground": "#569cd6"
      },
      "scope": "markup.heading"
    },
    {
      "settings": {
        "fontStyle": "italic"
      },
      "scope": "markup.italic"
    },
    {
      "settings": {
        "fontStyle": "strikethrough"
      },
      "scope": "markup.strikethrough"
    },
    {
      "settings": {
        "foreground": "#b5cea8"
      },
      "scope": "markup.inserted"
    },
    {
      "settings": {
        "foreground": "#ce9178"
      },
      "scope": "markup.deleted"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "markup.changed"
    },
    {
      "settings": {
        "foreground": "#6A9955"
      },
      "scope": "punctuation.definition.quote.begin.markdown"
    },
    {
      "settings": {
        "foreground": "#6796e6"
      },
      "scope": "punctuation.definition.list.begin.markdown"
    },
    {
      "settings": {
        "foreground": "#ce9178"
      },
      "scope": "markup.inline.raw"
    },
    {
      "settings": {
        "foreground": "#808080"
      },
      "scope": "punctuation.definition.tag"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": [
        "meta.preprocessor",
        "entity.name.function.preprocessor"
      ]
    },
    {
      "settings": {
        "foreground": "#ce9178"
      },
      "scope": "meta.preprocessor.string"
    },
    {
      "settings": {
        "foreground": "#b5cea8"
      },
      "scope": "meta.preprocessor.numeric"
    },
    {
      "settings": {
        "foreground": "#9cdcfe"
      },
      "scope": "meta.structure.dictionary.key.python"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "meta.diff.header"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "storage"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "storage.type"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": [
        "storage.modifier",
        "keyword.operator.noexcept"
      ]
    },
    {
      "settings": {
        "foreground": "#ce9178"
      },
      "scope": [
        "string",
        "meta.embedded.assembly"
      ]
    },
    {
      "settings": {
        "foreground": "#ce9178"
      },
      "scope": "string.tag"
    },
    {
      "settings": {
        "foreground": "#ce9178"
      },
      "scope": "string.value"
    },
    {
      "settings": {
        "foreground": "#d16969"
      },
      "scope": "string.regexp"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": [
        "punctuation.definition.template-expression.begin",
        "punctuation.definition.template-expression.end",
        "punctuation.section.embedded"
      ]
    },
    {
      "settings": {
        "foreground": "#d4d4d4"
      },
      "scope": [
        "meta.template.expression"
      ]
    },
    {
      "settings": {
        "foreground": "#9cdcfe"
      },
      "scope": [
        "support.type.vendored.property-name",
        "support.type.property-name",
        "source.css variable",
        "source.coffee.embedded"
      ]
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "keyword"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "keyword.control"
    },
    {
      "settings": {
        "foreground": "#d4d4d4"
      },
      "scope": "keyword.operator"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": [
        "keyword.operator.new",
        "keyword.operator.expression",
        "keyword.operator.cast",
        "keyword.operator.sizeof",
        "keyword.operator.alignof",
        "keyword.operator.typeid",
        "keyword.operator.alignas",
        "keyword.operator.instanceof",
        "keyword.operator.logical.python",
        "keyword.operator.wordlike"
      ]
    },
    {
      "settings": {
        "foreground": "#b5cea8"
      },
      "scope": "keyword.other.unit"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": [
        "punctuation.section.embedded.begin.php",
        "punctuation.section.embedded.end.php"
      ]
    },
    {
      "settings": {
        "foreground": "#9cdcfe"
      },
      "scope": "support.function.git-rebase"
    },
    {
      "settings": {
        "foreground": "#b5cea8"
      },
      "scope": "constant.sha.git-rebase"
    },
    {
      "settings": {
        "foreground": "#d4d4d4"
      },
      "scope": [
        "storage.modifier.import.java",
        "variable.language.wildcard.java",
        "storage.modifier.package.java"
      ]
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": "variable.language"
    },
    {
      "settings": {
        "foreground": "#DCDCAA"
      },
      "scope": [
        "entity.name.function",
        "support.function",
        "support.constant.handlebars",
        "source.powershell variable.other.member",
        "entity.name.operator.custom-literal"
      ]
    },
    {
      "settings": {
        "foreground": "#4EC9B0"
      },
      "scope": [
        "support.class",
        "support.type",
        "entity.name.type",
        "entity.name.namespace",
        "entity.other.attribute",
        "entity.name.scope-resolution",
        "entity.name.class",
        "storage.type.numeric.go",
        "storage.type.byte.go",
        "storage.type.boolean.go",
        "storage.type.string.go",
        "storage.type.uintptr.go",
        "storage.type.error.go",
        "storage.type.rune.go",
        "storage.type.cs",
        "storage.type.generic.cs",
        "storage.type.modifier.cs",
        "storage.type.variable.cs",
        "storage.type.annotation.java",
        "storage.type.generic.java",
        "storage.type.java",
        "storage.type.object.array.java",
        "storage.type.primitive.array.java",
        "storage.type.primitive.java",
        "storage.type.token.java",
        "storage.type.groovy",
        "storage.type.annotation.groovy",
        "storage.type.parameters.groovy",
        "storage.type.generic.groovy",
        "storage.type.object.array.groovy",
        "storage.type.primitive.array.groovy",
        "storage.type.primitive.groovy"
      ]
    },
    {
      "settings": {
        "foreground": "#4EC9B0"
      },
      "scope": [
        "meta.type.cast.expr",
        "meta.type.new.expr",
        "support.constant.math",
        "support.constant.dom",
        "support.constant.json",
        "entity.other.inherited-class",
        "punctuation.separator.namespace.ruby"
      ]
    },
    {
      "settings": {
        "foreground": "#C586C0"
      },
      "scope": [
        "keyword.control",
        "source.cpp keyword.operator.new",
        "keyword.operator.delete",
        "keyword.other.using",
        "keyword.other.directive.using",
        "keyword.other.operator",
        "entity.name.operator"
      ]
    },
    {
      "settings": {
        "foreground": "#9CDCFE"
      },
      "scope": [
        "variable",
        "meta.definition.variable.name",
        "support.variable",
        "entity.name.variable",
        "constant.other.placeholder"
      ]
    },
    {
      "settings": {
        "foreground": "#4FC1FF"
      },
      "scope": [
        "variable.other.constant",
        "variable.other.enummember"
      ]
    },
    {
      "settings": {
        "foreground": "#9CDCFE"
      },
      "scope": [
        "meta.object-literal.key"
      ]
    },
    {
      "settings": {
        "foreground": "#CE9178"
      },
      "scope": [
        "support.constant.property-value",
        "support.constant.font-name",
        "support.constant.media-type",
        "support.constant.media",
        "constant.other.color.rgb-value",
        "constant.other.rgb-value",
        "support.constant.color"
      ]
    },
    {
      "settings": {
        "foreground": "#CE9178"
      },
      "scope": [
        "punctuation.definition.group.regexp",
        "punctuation.definition.group.assertion.regexp",
        "punctuation.definition.character-class.regexp",
        "punctuation.character.set.begin.regexp",
        "punctuation.character.set.end.regexp",
        "keyword.operator.negation.regexp",
        "support.other.parenthesis.regexp"
      ]
    },
    {
      "settings": {
        "foreground": "#d16969"
      },
      "scope": [
        "constant.character.character-class.regexp",
        "constant.other.character-class.set.regexp",
        "constant.other.character-class.regexp",
        "constant.character.set.regexp"
      ]
    },
    {
      "settings": {
        "foreground": "#DCDCAA"
      },
      "scope": [
        "keyword.operator.or.regexp",
        "keyword.control.anchor.regexp"
      ]
    },
    {
      "settings": {
        "foreground": "#d7ba7d"
      },
      "scope": "keyword.operator.quantifier.regexp"
    },
    {
      "settings": {
        "foreground": "#569cd6"
      },
      "scope": [
        "constant.character",
        "constant.other.option"
      ]
    },
    {
      "settings": {
        "foreground": "#d7ba7d"
      },
      "scope": "constant.character.escape"
    },
    {
      "settings": {
        "foreground": "#C8C8C8"
      },
      "scope": "entity.name.label"
    }
  ],
  "semanticTokenRules": [
    {
      "_selector": "newOperator",
      "_style": {
        "_foreground": "#d4d4d4",
        "_bold": null,
        "_underline": null,
        "_italic": null,
        "_strikethrough": null
      }
    },
    {
      "_selector": "stringLiteral",
      "_style": {
        "_foreground": "#ce9178",
        "_bold": null,
        "_underline": null,
        "_italic": null,
        "_strikethrough": null
      }
    },
    {
      "_selector": "customLiteral",
      "_style": {
        "_foreground": "#d4d4d4",
        "_bold": null,
        "_underline": null,
        "_italic": null,
        "_strikethrough": null
      }
    },
    {
      "_selector": "numberLiteral",
      "_style": {
        "_foreground": "#b5cea8",
        "_bold": null,
        "_underline": null,
        "_italic": null,
        "_strikethrough": null
      }
    },
    {
      "_selector": "newOperator",
      "_style": {
        "_foreground": "#c586c0",
        "_bold": null,
        "_underline": null,
        "_italic": null,
        "_strikethrough": null
      }
    },
    {
      "_selector": "stringLiteral",
      "_style": {
        "_foreground": "#ce9178",
        "_bold": null,
        "_underline": null,
        "_italic": null,
        "_strikethrough": null
      }
    },
    {
      "_selector": "customLiteral",
      "_style": {
        "_foreground": "#dcdcaa",
        "_bold": null,
        "_underline": null,
        "_italic": null,
        "_strikethrough": null
      }
    },
    {
      "_selector": "numberLiteral",
      "_style": {
        "_foreground": "#b5cea8",
        "_bold": null,
        "_underline": null,
        "_italic": null,
        "_strikethrough": null
      }
    }
  ],
  "extensionData": {
    "_extensionId": "vscode.theme-defaults",
    "_extensionIsBuiltin": true,
    "_extensionName": "theme-defaults",
    "_extensionPublisher": "vscode"
  },
  "themeSemanticHighlighting": true,
  "colorMap": {
    "checkbox.border": "#3c3c3c",
    "editor.background": "#1f1f1f",
    "editor.foreground": "#cccccc",
    "editor.inactiveSelectionBackground": "#3a3d41",
    "editorIndentGuide.background1": "#404040",
    "editorIndentGuide.activeBackground1": "#707070",
    "editor.selectionHighlightBackground": "#add6ff26",
    "list.dropBackground": "#383b3d",
    "activityBarBadge.background": "#0078d4",
    "sideBarTitle.foreground": "#cccccc",
    "input.placeholderForeground": "#989898",
    "menu.background": "#1f1f1f",
    "menu.foreground": "#cccccc",
    "menu.separatorBackground": "#454545",
    "menu.border": "#454545",
    "menu.selectionBackground": "#0078d4",
    "statusBarItem.remoteForeground": "#ffffff",
    "statusBarItem.remoteBackground": "#0078d4",
    "ports.iconRunningProcessForeground": "#369432",
    "sideBarSectionHeader.background": "#181818",
    "sideBarSectionHeader.border": "#2b2b2b",
    "tab.selectedBackground": "#222222",
    "tab.selectedForeground": "#ffffffa0",
    "tab.lastPinnedBorder": "#cccccc33",
    "list.activeSelectionIconForeground": "#ffffff",
    "terminal.inactiveSelectionBackground": "#3a3d41",
    "widget.border": "#313131",
    "actionBar.toggledBackground": "#383a49",
    "activityBar.activeBorder": "#0078d4",
    "activityBar.background": "#181818",
    "activityBar.border": "#2b2b2b",
    "activityBar.foreground": "#d7d7d7",
    "activityBar.inactiveForeground": "#868686",
    "activityBarBadge.foreground": "#ffffff",
    "badge.background": "#616161",
    "badge.foreground": "#f8f8f8",
    "button.background": "#0078d4",
    "button.border": "#ffffff12",
    "button.foreground": "#ffffff",
    "button.hoverBackground": "#026ec1",
    "button.secondaryBackground": "#313131",
    "button.secondaryForeground": "#cccccc",
    "button.secondaryHoverBackground": "#3c3c3c",
    "chat.slashCommandBackground": "#26477866",
    "chat.slashCommandForeground": "#85b6ff",
    "chat.editedFileForeground": "#e2c08d",
    "checkbox.background": "#313131",
    "debugToolBar.background": "#181818",
    "descriptionForeground": "#9d9d9d",
    "dropdown.background": "#313131",
    "dropdown.border": "#3c3c3c",
    "dropdown.foreground": "#cccccc",
    "dropdown.listBackground": "#1f1f1f",
    "editor.findMatchBackground": "#9e6a03",
    "editorGroup.border": "#ffffff17",
    "editorGroupHeader.tabsBackground": "#181818",
    "editorGroupHeader.tabsBorder": "#2b2b2b",
    "editorGutter.addedBackground": "#2ea043",
    "editorGutter.deletedBackground": "#f85149",
    "editorGutter.modifiedBackground": "#0078d4",
    "editorLineNumber.activeForeground": "#cccccc",
    "editorLineNumber.foreground": "#6e7681",
    "editorOverviewRuler.border": "#010409",
    "editorWidget.background": "#202020",
    "errorForeground": "#f85149",
    "focusBorder": "#0078d4",
    "foreground": "#cccccc",
    "icon.foreground": "#cccccc",
    "input.background": "#313131",
    "input.border": "#3c3c3c",
    "input.foreground": "#cccccc",
    "inputOption.activeBackground": "#2489db82",
    "inputOption.activeBorder": "#2488db",
    "keybindingLabel.foreground": "#cccccc",
    "notificationCenterHeader.background": "#1f1f1f",
    "notificationCenterHeader.foreground": "#cccccc",
    "notifications.background": "#1f1f1f",
    "notifications.border": "#2b2b2b",
    "notifications.foreground": "#cccccc",
    "panel.background": "#181818",
    "panel.border": "#2b2b2b",
    "panelInput.border": "#2b2b2b",
    "panelTitle.activeBorder": "#0078d4",
    "panelTitle.activeForeground": "#cccccc",
    "panelTitle.inactiveForeground": "#9d9d9d",
    "peekViewEditor.background": "#1f1f1f",
    "peekViewEditor.matchHighlightBackground": "#bb800966",
    "peekViewResult.background": "#1f1f1f",
    "peekViewResult.matchHighlightBackground": "#bb800966",
    "pickerGroup.border": "#3c3c3c",
    "progressBar.background": "#0078d4",
    "quickInput.background": "#222222",
    "quickInput.foreground": "#cccccc",
    "settings.dropdownBackground": "#313131",
    "settings.dropdownBorder": "#3c3c3c",
    "settings.headerForeground": "#ffffff",
    "settings.modifiedItemIndicator": "#bb800966",
    "sideBar.background": "#181818",
    "sideBar.border": "#2b2b2b",
    "sideBar.foreground": "#cccccc",
    "sideBarSectionHeader.foreground": "#cccccc",
    "statusBar.background": "#181818",
    "statusBar.border": "#2b2b2b",
    "statusBarItem.hoverBackground": "#f1f1f133",
    "statusBarItem.hoverForeground": "#ffffff",
    "statusBar.debuggingBackground": "#0078d4",
    "statusBar.debuggingForeground": "#ffffff",
    "statusBar.focusBorder": "#0078d4",
    "statusBar.foreground": "#cccccc",
    "statusBar.noFolderBackground": "#1f1f1f",
    "statusBarItem.focusBorder": "#0078d4",
    "statusBarItem.prominentBackground": "#6e768166",
    "tab.activeBackground": "#1f1f1f",
    "tab.activeBorder": "#1f1f1f",
    "tab.activeBorderTop": "#0078d4",
    "tab.activeForeground": "#ffffff",
    "tab.selectedBorderTop": "#6caddf",
    "tab.border": "#2b2b2b",
    "tab.hoverBackground": "#1f1f1f",
    "tab.inactiveBackground": "#181818",
    "tab.inactiveForeground": "#9d9d9d",
    "tab.unfocusedActiveBorder": "#1f1f1f",
    "tab.unfocusedActiveBorderTop": "#2b2b2b",
    "tab.unfocusedHoverBackground": "#1f1f1f",
    "terminal.foreground": "#cccccc",
    "terminal.tab.activeBorder": "#0078d4",
    "textBlockQuote.background": "#2b2b2b",
    "textBlockQuote.border": "#616161",
    "textCodeBlock.background": "#2b2b2b",
    "textLink.activeForeground": "#4daafc",
    "textLink.foreground": "#4daafc",
    "textPreformat.foreground": "#d0d0d0",
    "textPreformat.background": "#3c3c3c",
    "textSeparator.foreground": "#21262d",
    "titleBar.activeBackground": "#181818",
    "titleBar.activeForeground": "#cccccc",
    "titleBar.border": "#2b2b2b",
    "titleBar.inactiveBackground": "#1f1f1f",
    "titleBar.inactiveForeground": "#9d9d9d",
    "welcomePage.tileBackground": "#2b2b2b",
    "welcomePage.progress.foreground": "#0078d4"
  },
  "watch": false
}
```
- Codium.codium
```json
{
  "installation_fingerprint": "d45abdd22967a7e1247537c541bc1afe3fe627ae2272afba9d8c7758f6a8e403-Codium.codium-c:\\Users\\skyle\\.vscode-insiders\\extensions\\codium.codium-1.6.36-f:\\Microsoft VS Code Insiders\\resources\\app",
  "installation_fingerprint_uuid": "d8e4439a-46bd-5aca-b6e5-6606868408f0",
  "installation_id": "659a884d-1b38-404d-9d23-ad36834f4dc3",
  "distinct_id": "3hG3DgThtYRteK04DW9Xhn6uqJE2",
  "qodo_gen_installed_event_sent": true,
  "hasUpdatedModesWithAllCustomMcps": true,
  "hasUpdatedWorkflowsWithAllCustomMcps": true,
  "isAgenticModeViewed": true,
  "lastUserSelectedModel": "gpt-5-minimal",
  "customModel": "gpt-5-minimal",
  "disabledMcpServers": [
    "Web Search"
  ],
  "disabledMcpTools": {},
  "autoApprovedTools": { "Code Navigation": { "get_code_dependencies": true, "find_code_usages": true }, "File System": { "read_file": true, "write_to_file": true, "replace_in_file": true, "search_files": true, "get_file_info": true, "list_files": true }, "GIT": { "git_remote_url": true, "git_branches": true, "git_changes": true, "git_file_history": true } },
  "user_id": "75baef5c-0a54-40b4-b486-ce10ddd222ba"
}
``` 
- workbench.views.service.auxiliarybar.9e62d474-db52-4122-bf48-3b5b04b89013.state.hidden
```json
[
  { "id": "ocrmnavigatorNavigator", "isHidden": false, "order": 6 },
  { "id": "terminal", "isHidden": false },
  { "id": "workbench.explorer.openEditorsView", "isHidden": true },
  { "id": "workbench.explorer.fileView", "isHidden": false },
  { "id": "outline", "isHidden": true },
  { "id": "timeline", "isHidden": true },
  { "id": "npm", "isHidden": true }
]
```
- workbench.view.extension.ocrmnavigator.state.hidden
```json
[
  { "id": "ocrmnavigatorNavigator", "isHidden": false, "order": 0 },
  { "id": "terminal", "isHidden": false, "order": 2 },
  { "id": "str", "isHidden": false, "order": 1 }
]
```
- workbench.view.extension.DevStackToDo.state.hidden
```json
[
  { "id": "DevStackToDo", "isHidden": false },
  { "id": "DevStackNotes", "isHidden": false },
  { "id": "DevStackReminder", "isHidden": false },
  { "id": "DevStackPostItPad", "isHidden": false }
]
```
- workbench.view.debug.state.hidden
```json
[
  { "id": "workbench.debug.welcome", "isHidden": false },
  { "id": "workbench.debug.variablesView", "isHidden": false },
  { "id": "workbench.debug.watchExpressionsView", "isHidden": false },
  { "id": "workbench.debug.callStackView", "isHidden": false },
  { "id": "workbench.debug.loadedScriptsView", "isHidden": false },
  { "id": "workbench.debug.breakPointsView", "isHidden": false },
  { "id": "jsBrowserBreakpoints", "isHidden": false },
  { "id": "jsExcludedCallers", "isHidden": false },
  { "id": "jsDebugNetworkTree", "isHidden": false }
]
```
- workbench.statusbar.hidden
```json
[
  "status.workspaceTrust.1682032283885",
  "status.workspaceTrust.ba971d67e5c413165a91a5728298c1e3",
  "status.workspaceTrust.1682454481968",
  "status.workspaceTrust.1682454688834",
  "status.workspaceTrust.1682454909688",
  "status.workspaceTrust.a24655474f01d6293e3da3182f979dc3",
  "status.workspaceTrust.1682466294856",
  "status.workspaceTrust.448178e68c391b1f63ba607a00e64be2",
  "status.workspaceTrust.1682468523607",
  "status.workspaceTrust.3f270759c238d60ea779dcf4e6b19b4d",
  "status.workspaceTrust.e5f61873a3353c2194f85e8ae5270ea9",
  "status.workspaceTrust.1682841960041",
  "status.workspaceTrust.064c35463b84a42e90c191a7d349e56c",
  "status.workspaceTrust.1682849362212",
  "status.workspaceTrust.ac38b957f9a7f63fc58f1e419c319fd0",
  "status.workspaceTrust.1682852580327",
  "status.workspaceTrust.a5c10e2371354ef839623c5091e636ad",
  "status.workspaceTrust.1682855701354",
  "status.workspaceTrust.3baf0e831e8f4b8f8b463468a25e9a05",
  "status.workspaceTrust.1682863674548",
  "status.workspaceTrust.d4c590dd89c4c59228fd26028697693c",
  "status.workspaceTrust.df984d5d670255c8d71f29e974051e35",
  "status.workspaceTrust.03f5858fcff9f878fcb7051139b27853",
  "status.workspaceTrust.0278be27ea66f3395e22699c51c23a7f",
  "status.workspaceTrust.1682900177378",
  "status.workspaceTrust.dfa9e3c59f56f15d08ee68885aaaf621",
  "status.workspaceTrust.1682904537137",
  "status.workspaceTrust.4c25858f14be124c916eb9a3d1a1e73a",
  "status.workspaceTrust.1683052188554",
  "status.workspaceTrust.4f639903efe58eb851eeb5ecd3faf449",
  "status.workspaceTrust.1683065169615",
  "status.workspaceTrust.b9e5326982d7703008b1cbedfc71358c",
  "status.workspaceTrust.1683065629291",
  "status.workspaceTrust.1683155295797",
  "status.workspaceTrust.d15073b02ce54de8c2d956ee16e065e1",
  "status.workspaceTrust.76066ccf23b2d84d8a56b066fe785cf5",
  "status.workspaceTrust.1683165291237",
  "status.workspaceTrust.8ffceb481b648969ba2842de0850eb0f",
  "status.workspaceTrust.1683165695619",
  "status.workspaceTrust.8f4091efff1bc25a4819c107320a49f0",
  "status.workspaceTrust.1683622104678"
]
```
- workbench.panel.placeholderPanels
```json
[
  {
    "id": "workbench.panel.markers",
    "themeIcon": { "id": "markers-view-icon" },
    "name": "Problems",
    "isBuiltin": true,
    "views": [
      {},
      { "when": "debuggersAvailable" }
    ]
  },
  {
    "id": "workbench.panel.output",
    "themeIcon": { "id": "output-view-icon" },
    "name": "Output",
    "isBuiltin": true,
    "views": [
      {}
    ]
  },
  {
    "id": "workbench.panel.repl",
    "themeIcon": { "id": "debug-console-view-icon" },
    "name": "Debug Console",
    "isBuiltin": true,
    "views": []
  },
  {
    "id": "terminal",
    "themeIcon": { "id": "terminal-view-icon" },
    "name": "Terminal",
    "isBuiltin": true,
    "views": []
  },
  {
    "id": "workbench.panel.testResults",
    "themeIcon": { "id": "test-results-icon" },
    "name": "Test Results",
    "isBuiltin": true,
    "views": [
      { "when": "testing.hasAnyResults" }
    ]
  },
  {
    "id": "~remote.forwardedPortsContainer",
    "themeIcon": { "id": "ports-view-icon" },
    "name": "Ports",
    "isBuiltin": true,
    "views": []
  },
  { "id": "workbench.view.extension.continueConsole", "name": "Continue Console", "isBuiltin": false },
  { "id": "workbench.panel.comments", "name": "Comments", "isBuiltin": false },
  {
    "id": "workbench.views.service.panel.e93f6175-55af-4598-8176-c434529362f5",
    "name": "User View Container",
    "isBuiltin": true,
    "views": [
      { "when": "scm.providerCount && scm.providerCount != '0'" }
    ]
  },
  {
    "id": "refactorPreview",
    "themeIcon": { "id": "refactor-preview-view-icon" },
    "name": "Refactor Preview",
    "isBuiltin": true,
    "views": [
      { "when": "refactorPreview.enabled" }
    ]
  },
  { "id": "workbench.view.extension.vsc-todo-sidebar", "name": "VS Code Todo", "isBuiltin": false },
  { "id": "workbench.view.extension.markdown-todo", "name": "MarkDown To-Do", "isBuiltin": false }
]
```
- workbench.panel.pinnedPanels
```json
[
  { "id": "workbench.panel.markers", "pinned": true, "visible": true, "order": 0 },
  { "id": "workbench.panel.output", "pinned": true, "visible": true, "order": 1 },
  { "id": "workbench.panel.repl", "pinned": true, "visible": false, "order": 2 },
  { "id": "terminal", "pinned": true, "visible": false, "order": 3 },
  { "id": "workbench.panel.testResults", "pinned": true, "visible": false, "order": 3 },
  { "id": "~remote.forwardedPortsContainer", "pinned": false, "visible": true, "order": 5 },
  { "id": "workbench.view.extension.continueConsole", "pinned": true, "visible": false, "order": 6 },
  { "id": "workbench.panel.comments", "pinned": true, "visible": false, "order": 10 },
  { "id": "workbench.views.service.panel.e93f6175-55af-4598-8176-c434529362f5", "pinned": true, "visible": true },
  { "id": "refactorPreview", "pinned": true, "visible": false },
  { "id": "workbench.view.extension.vsc-todo-sidebar", "pinned": false, "visible": false, "order": 8 },
  { "id": "workbench.view.extension.markdown-todo", "pinned": true, "visible": false, "order": 9 }
]
```
- workbench.panel.chat.hidden
```json
[
  { "id": "workbench.panel.chat.view.copilot", "isHidden": false },
  { "id": "terminal", "isHidden": false }
]
```
- workbench.explorer.views.state.hidden
```json
[
  { "id": "outline", "isHidden": true, "order": 3 },
  { "id": "timeline", "isHidden": true, "order": 4 },
  { "id": "workbench.explorer.openEditorsView", "isHidden": true, "order": 2 },
  { "id": "workbench.explorer.emptyView", "isHidden": false },
  { "id": "npm", "isHidden": true, "order": 5 },
  { "id": "workbench.explorer.fileView", "isHidden": false, "order": 1 },
  { "id": "workbench.scm.repositories", "isHidden": false },
  { "id": "workbench.scm", "isHidden": false, "order": 0 },
  { "id": "liveshare.session", "isHidden": false },
  { "id": "liveshare.help", "isHidden": false },
  { "id": "liveshare.devtools", "isHidden": false },
  { "id": "liveshare.session.explorer", "isHidden": false },
  { "id": "azureActivityLog", "isHidden": false },
  { "id": "azureFocusView", "isHidden": false },
  { "id": "azureResourceGroups", "isHidden": false },
  { "id": "azureWorkspace", "isHidden": false },
  { "id": "ms-azuretools.helpAndFeedback", "isHidden": false },
  { "id": "dockerContainers", "isHidden": false },
  { "id": "dockerImages", "isHidden": false },
  { "id": "dockerRegistries", "isHidden": false },
  { "id": "dockerNetworks", "isHidden": false },
  { "id": "dockerVolumes", "isHidden": false },
  { "id": "vscode-docker.views.dockerContexts", "isHidden": false },
  { "id": "vscode-docker.views.help", "isHidden": false },
  { "id": "github-actions.current-branch", "isHidden": false },
  { "id": "github-actions.workflows", "isHidden": false },
  { "id": "github-actions.settings", "isHidden": false },
  { "id": "github-actions.empty-view", "isHidden": false },
  { "id": "buttons", "isHidden": false },
  { "id": "handy-commands.commandTree", "isHidden": false },
  { "id": "allSnipps", "isHidden": false },
  { "id": "terminalSnipps", "isHidden": false },
  { "id": "snippetTree", "isHidden": false },
  { "id": "connect", "isHidden": false },
  { "id": "suggestedSnippetsTree", "isHidden": false },
  { "id": "explainedSnippetsTree", "isHidden": false },
  { "id": "relatedSnippetsTree", "isHidden": false },
  { "id": "about", "isHidden": false },
  { "id": "piecesCopilot", "isHidden": false },
  { "id": "duplicatedCode", "isHidden": false },
  { "id": "snippetsExplorer", "isHidden": false },
  { "id": "wsSnippetsExplorer", "isHidden": false },
  { "id": "snippets.view", "isHidden": false }
]
```
- workbench.auxiliarybar.pinnedPanels
```json
 [
  {
    "id":"workbench.viewContainer.agentSessions",
    "pinned":true,
    "visible":false,
    "order":6
    },
    {
      "id":"workbench.panel.chatEditing",
    "pinned":false,
    "visible":false,
    "order":101
    },{
      "id":"workbench.view.extension.ocrmnavigator",
      "pinned":false,
      "visible":false,
      "order":11
      },{
        "id":"workbench.view.extension.geminiChat",
        "pinned":true,
        "visible":false,
        "order":9
        },{
          "id":"workbench.view.extension.jetbrains-ai",
          "pinned":true,
          "visible":false,
          "order":10
          },{
            "id":"workbench.views.service.auxiliarybar.bea28fd6-5262-4d04-8f7c-860259c3157c",
            "pinned":true,
            "visible":false
            },{
              "id":"workbench.views.service.sidebar.bbd2ef2d-f401-4fdb-9052-6d24abe4c360",
              "pinned":true,
              "visible":false
              },{
                "id":"workbench.panel.chat",
                "pinned":true,
                "visible":false,
                "order":1
                },{
                  "id":"workbench.views.service.sidebar.470e9ab5-bd81-4f91-bfa4-c3baddaa0af2",
                  "pinned":true,
                  "visible":false
                  }]

```
- workbench.activity.pinnedViewlets2 - this is some shit we want, but this is what im talking about.... something of these extesions i havent had in over a year
```json
[
  { "id": "workbench.view.search", "pinned": true, "visible": true, "order": 1 },
  { "id": "workbench.view.debug", "pinned": false, "visible": true, "order": 3 },
  { "id": "workbench.view.scm", "pinned": false, "visible": false, "order": 2 },
  { "id": "workbench.views.service.auxiliarybar.9e62d474-db52-4122-bf48-3b5b04b89013", "pinned": true, "visible": false },
  { "id": "workbench.view.explorer", "pinned": true, "visible": false, "order": 0 },
  { "id": "workbench.view.chat.sessions", "pinned": true, "visible": false, "order": 6 },
  { "id": "workbench.view.extension.devstacktodo", "pinned": true, "visible": false, "order": 12 },
  { "id": "workbench.view.extension.DevStackToDo", "pinned": true, "visible": false, "order": 10 },
  { "id": "workbench.view.extension.gistpad", "pinned": true, "visible": false, "order": 10 },
  { "id": "workbench.view.extension.prismaActivitybar", "pinned": false, "visible": false, "order": 10 },
  { "id": "workbench.view.extension.spellinguo", "pinned": true, "visible": false, "order": 11 },
  { "id": "workbench.view.extension.snippets-manager-sleek-snippetsView", "pinned": true, "visible": false, "order": 10 },
  { "id": "workbench.view.extension.dendron-view", "pinned": true, "visible": false, "order": 8 },
  { "id": "workbench.view.extensions", "pinned": true, "visible": true, "order": 4 },
  { "id": "workbench.view.remote", "pinned": false, "visible": true, "order": 4 },
  { "id": "workbench.view.extension.pieces-explorer-activity-bar", "pinned": true, "visible": false, "order": 8 },
  { "id": "workbench.view.extension.pieces-copilot", "pinned": true, "visible": false, "order": 9 },
  { "id": "workbench.view.extension.superusertaskrunner", "pinned": true, "visible": false, "order": 11 },
  { "id": "workbench.view.extension.md-notes-todo-explorer", "pinned": true, "visible": false, "order": 11 },
  { "id": "workbench.view.extension.snippetsmanager-snippetsView", "pinned": true, "visible": false, "order": 11 },
  { "id": "workbench.view.extension.continue", "pinned": true, "visible": false, "order": 9 },
  { "id": "workbench.view.extension.codegeex-sidebar", "pinned": true, "visible": false, "order": 8 }
]
```
- workbench.auxiliarybar.pinnedPanels
```json
[
  { "id": "workbench.viewContainer.agentSessions", "pinned": true, "visible": false, "order": 6 },
  { "id": "workbench.panel.chatEditing", "pinned": false, "visible": false, "order": 101 },
  { "id": "workbench.view.extension.ocrmnavigator", "pinned": false, "visible": false, "order": 11 },
  { "id": "workbench.view.extension.geminiChat", "pinned": true, "visible": false, "order": 9 },
  { "id": "workbench.view.extension.jetbrains-ai", "pinned": true, "visible": false, "order": 10 },
  { "id": "workbench.views.service.auxiliarybar.bea28fd6-5262-4d04-8f7c-860259c3157c", "pinned": true, "visible": false },
  { "id": "workbench.views.service.sidebar.bbd2ef2d-f401-4fdb-9052-6d24abe4c360", "pinned": true, "visible": false },
  { "id": "workbench.panel.chat", "pinned": true, "visible": false, "order": 1 },
  { "id": "workbench.views.service.sidebar.470e9ab5-bd81-4f91-bfa4-c3baddaa0af2", "pinned": true, "visible": false }
]
```
- workbench.auxiliarybar.placeholderPanels POPFFT
```json
[
  {
    "id": "workbench.viewContainer.agentSessions",
    "themeIcon": { "id": "chat-sessions-icon" },
    "name": "Agents",
    "isBuiltin": true,
    "views": [
      { "when": "!chatSetupDisabled && !chatSetupHidden && config.chat.agentSessionsViewLocation == 'single-view'" }
    ]
  },
  { "id": "workbench.panel.chatEditing", "name": "Copilot Edits", "isBuiltin": false },
  {
    "id": "workbench.view.extension.ocrmnavigator",
    "themeIcon": { "id": "code" },
    "name": "DevStack",
    "isBuiltin": false,
    "views": []
  },
  { "id": "workbench.view.extension.geminiChat", "name": "Gemini Code Assist", "isBuiltin": false },
  { "id": "workbench.view.extension.jetbrains-ai", "name": "JetBrains AI Assistant", "isBuiltin": false },
  { "id": "workbench.views.service.auxiliarybar.bea28fd6-5262-4d04-8f7c-860259c3157c", "name": "User View Container", "isBuiltin": false },
  {
    "id": "workbench.views.service.sidebar.bbd2ef2d-f401-4fdb-9052-6d24abe4c360",
    "iconUrl": { "$mid": 1, "path": "/c:/Users/skyle/.vscode-insiders/extensions/skyler.ocrmnav-4.0.78/code.svg", "scheme": "file" },
    "name": "DevStack",
    "isBuiltin": true,
    "views": [
      { "when": "workspaceFolderCount >= 1" }
    ]
  },
  {
    "id": "workbench.panel.chat",
    "themeIcon": { "id": "chat-sparkle" },
    "name": "Chat",
    "isBuiltin": true,
    "views": [
      { "when": "chatExtensionInvalid || chatPanelParticipantRegistered || !chatSetupDisabled && !chatSetupHidden" }
    ]
  },
  { "id": "workbench.views.service.sidebar.470e9ab5-bd81-4f91-bfa4-c3baddaa0af2", "name": "User View Container", "isBuiltin": false }
]
```
- simpply so much data that it makes me want to completley remove vscode... like nuking it off the system and reinstalling from scratch... like actually... and this is gonna take a while to reverse as... fucking nothing... is user friendly

```json 
{
  "viewContainerLocations":
{
  "workbench.views.service.panel.e93f6175-55af-4598-8176-c434529362f5":1,
  "workbench.views.service.sidebar.d705666c-a06a-43ae-b07e-7dd29acdd6ee":0,
  "workbench.view.extension.vsc-todo-sidebar":1,
  "workbench.view.extension.markdown-todo":1,
  "workbench.views.service.sidebar.a723bf58-66c7-4a12-85c6-26b9636555ce":0,
  "workbench.views.service.sidebar.c4b67703-45a0-4b09-bde9-039edc20262d":0,
  "workbench.views.service.sidebar.73412756-2c08-4084-bc57-031a78d54dd2":0,
  "workbench.views.service.sidebar.470e9ab5-bd81-4f91-bfa4-c3baddaa0af2":2,
  "workbench.view.extension.ocrmnavigator":2,
  "workbench.views.service.sidebar.3264ea6a-e0b9-4b2c-a0c7-4f09350e8fb0":0,
  "workbench.views.service.auxiliarybar.9e62d474-db52-4122-bf48-3b5b04b89013":0,
  "workbench.view.extension.geminiChat":2,
  "workbench.view.extension.jetbrains-ai":2,
  "workbench.views.service.auxiliarybar.bea28fd6-5262-4d04-8f7c-860259c3157c":2,
  "workbench.views.service.sidebar.bbd2ef2d-f401-4fdb-9052-6d24abe4c360":2
  },
"viewLocations":{
  "workbench.panel.repl.view":"workbench.panel.markers",
  "workbench.scm.repositories":"workbench.views.service.panel.e93f6175-55af-4598-8176-c434529362f5",
  "workbench.scm":"workbench.views.service.sidebar.d705666c-a06a-43ae-b07e-7dd29acdd6ee",
  "snippets-manager-sleek-snippetsView-WorkspaceSnippetsExplorerView":"workbench.view.explorer",
  "snippets-manager-sleek-snippetsView-ExtensionSnippetsExplorerView":"workbench.view.explorer",
  "cevsCore":"workbench.views.service.sidebar.a723bf58-66c7-4a12-85c6-26b9636555ce",
  "to-do-explorer":"workbench.views.service.sidebar.c4b67703-45a0-4b09-bde9-039edc20262d",
  "snippets-manager-sleek-snippetsView-UserSnippetsExplorerView":"workbench.views.service.sidebar.73412756-2c08-4084-bc57-031a78d54dd2",
  "opinionatedCrmNavigator":"workbench.views.service.sidebar.470e9ab5-bd81-4f91-bfa4-c3baddaa0af2",
  "workbench.view.search":"workbench.views.service.sidebar.3264ea6a-e0b9-4b2c-a0c7-4f09350e8fb0",
 } }
```
---

[🡄 Return](https://github.com/8an3/DevStack)





# 

