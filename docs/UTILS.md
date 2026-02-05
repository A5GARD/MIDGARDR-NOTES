# UTILS

> [!NOTE]
>
> My apologies, this file seems to be one of the few that didn't make the latest docs conversion.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **SVG To WOFF**

Just as its named its a svg to woff converter, converts your entire folder into and places the produced woff file within the same folder.

Be sure to remove all non svg files as it will error out if the folder contains anything but svgs.

Can be executed via the devstack menu, option labeled 'SVG to WOFF'


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **RATATOSKR**

Needs some work, as it is currently not in the state that I wish it to be, but it still works.

Accessible via the explorers context menu, just right click any folder and select ratatoskr. A new editor will open and allow you to make some edits and preview it via the preview tab.

Currently the only items that are working are the:
- use icons toggle
- wrapper type
- if you place any text in the import from text, clicking parse text to tree ( doesnt matter what text you use as it doesn't stick ), a editable tree will display to the right allowing you to edit individual line items. Click on any line item and the editable options will display below the tree itself.
- preview tab
- copy to clipboard

IMO, its jank as fuck right now because half the features don't work, but it still works and when I don't have more important things to do I will come back to this and make proper but might not be for a while, since it does do 95% of the jobs I use it forand to be honest, I use this waaaayy more than I ever thought I would as it is incredily handy when dealing with ai prompts. As giving ai's my exact file structure was not something I did do, due to how time consuming it is. But now that this is here... atleast once a day I'm using this feature.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Region Folding**

There are two ways you can use these features, first is the devstack menu, and navigating to the fold option. Which IMO, this takes to much time in comparison to the second. 

The second option is placing the command names in a config item so that is accessible viz the devstack explorer pane.

Currently, there are only toggles as I still can't figure out the other ways I would like folding to happen, but the toggle is nice as you quickly fold the specific section, once done toggle it back. Which leaves all your other folded sections exactly as they were. I've found it to be really handy in larger json file.

```json
{
    "label": "TOGGLE",
    "type": "folder",
    "expanded": true,
    "icon": "fold-down",
    "items": [
        { "label": "TGL #R 1", "path": "ocrmnavigator.vscode.region.1.toggle", "type": "command", "icon": "fold-down" },
        { "label": "TGL #R 2", "path": "ocrmnavigator.vscode.region.2.toggle", "type": "command", "icon": "fold-down" },
        { "label": "TGL #R 3", "path": "ocrmnavigator.vscode.region.3.toggle", "type": "command", "icon": "fold-down" },
        { "label": "TGL #R 4", "path": "ocrmnavigator.vscode.region.4.toggle", "type": "command", "icon": "fold-down" },
        { "label": "TGL #R 5", "path": "ocrmnavigator.vscode.region.5.toggle", "type": "command", "icon": "fold-down" },
        { "label": "TGL #R 6", "path": "ocrmnavigator.vscode.region.6.toggle", "type": "command", "icon": "fold-down" },
        { "label": "TGL #R 7", "path": "ocrmnavigator.vscode.region.7.toggle", "type": "command", "icon": "fold-down" }
    ]
},

```

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **File Nesting**

pfft... this seems to be like the other lost function. This extension is way too big, this was built and as I was working on it I started from scratch to start fresh and because I had a file nesting extesion in use... I forgot about finishing this. I might just pound this one out right now so its in the extension.

When I do get to this, it will place configurable settings within your global settings file with a default that covers, a lot. Really nice feature if you have a lot of files in your root folder, as it hides the majority of them and if you have weirdly named files, custom configurations, or files/configs that wouldn't really be used by many devs, you can quickly edit the settings to include those files.

There will be a option within the devstack menu that will activate this feature.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **env Context Swapper**

I've implemented multiple systems in the past, this seems to work the quickest and cleanest, as you only click once and it swaps everything for you.

I find whenever working with more than one .env variable I'm already placing 2 values in my .env anyways, but having to go manually cutting and pasting to swap out values. Obviously this being a lot quicker at it.

2 files are needed for this
- .env
- .dev.env

In order for it to tell what to swap where when it is triggered you must place the following values at the start of the .env key
- 'LOCAL_'
- 'REMOTE_'

Currently only usable via the devstack menu as I haven't found a way to trigger it via a config item in the devstack explorer pane. I might try again in the future but in its current form it works great.

Whenever you select remote or local, scans the .dev.env file for the relative desired values for example selecting local will swap out all the values that have a local entry in the .env file no matter how many you have to swap out.