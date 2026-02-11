# FREYR

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **VSCODE & TAILWIND STYLING**

- [Themes](#themes)
- [VSCode & Tailwind Theme Builder](#vscode--tailwind-theme-builder)
- [Blacked Out](#blacked-out)
- [Blued Out](#blued-out)
- [Window Differentiator](#window-differentiator)
- [Reset - Window Differentiator](#reset---window-differentiator)


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Themes**

Didn't realize it was this many, but 38 comprehensive dark themes have been registered and can be activated via the file context menu under themes found within the preferences submenu.

Currently there are no light themes registered, but I may add 38 light counter parts in the future as I'm unsure if they are even worth the time considering that devs typcically favour the dark flavour. 

However, each of the themes includes token colors. After creating them all I had found out there are also tokens for semantic highlighting and others... Well that's annoying. I fucking hate when resources talk about a subject but leave large portions of data out. 

No matter, each theme will cover the following sections as I now have to go back through all 40 of them to include them:

* languages: js, jsx, ts, tsx, python, html, css, json but where applicable file extensions were left out so as to cover all file types instead
* semantic highlighting rules 
* specfic token types to emphasize function variables, keywords, etc

The new count being 40 due to adding two more of my personal themes. These themes are a lot different in my opinion than the typical theme found in among the marketplace listings and convey a lot more "professional" looking UI than your typical "professional" theme due to the fact that all random over overstated colors that are typcaily sprinkled around virtually every single theme, have been removed or left out. 

For example blued-out features a dark blue theme throughout with borders consisting of a blue tinted grey. The text colors also go against the norms, where all text in the ui aside from the text found in the editors is muted-foreground, while the editors receive the foreground counter-part. Thus the end result, is a theme in which it has very little distractions in terms of different parts of the ui always trying to grab your attention. If this theming style appeals to you I highly suggest adding the following values to your global settings files:

- "git.diffEditor.renderGutterMenu": false,
- "git.decorations.enabled": false,
- "scm.diffDecorationsGutterAction": "none",
- "scm.diffDecorations": "none"

These settings remove all the dabs of color ( or I would label it as unicorn puke ) that github places in among the different parts of the ui including tabs, explorer pane, gutter, etc. 

The end result is a nice user interface that gives off the least amount of light while not sacrificing anything where it is important. If you suffer from headaches, eye pain, or get exhausted whenever you use a computer for long periods of times, than this theme, along with blacked-out, are two you should most definitely try out. Personally, I never suffered from the mentioned issues but I had noticed I was able to work a lot longer then I could typically, hours and hours longer. After using the two themes for over a year, I've noticed I'm now getting effected by those issues, since these themes have such an understateted tone to them ( or overall light exposure being blasted at you via your monitor ) in comparison to the average user interface. To the point that I can no longer use the average work station anymore. So, if they have made me accustemed to receiving less light exposure, then they will most definitely help you with those issues as well.

If you want to take it a step farther and you use minimaps like myself, than I would also suggest trying this minimap configuration:

- "editor.minimap.maxColumn": 50,
- "editor.minimap.showRegionSectionHeaders": true,
- "editor.minimap.showMarkSectionHeaders": false,
- "editor.minimap.autohide": "mouseover",
- "editor.minimap.showSlider": "mouseover",
- "editor.minimap.side": "left",
- "editor.minimap.size": "fill",
- "editor.minimap.renderCharacters": false,

The end result places the mini map on the left side with a smaller width than what is set by default with the rendered minimap text hidden from view unless hovered over. Whenever the minimap is not in use, the editor just has a slightly fatter gutter that now acts as a quick way to navigate files due to the fill value making it less of a scrolling type feature and more like a function that quickly lets you navigate the file in its entirety. I'll admit, if you do not already use the minimap on the left side, it will take some time getting used to but when you think about it you will see the benefits make it worth it for the following reasons: 

- your cursor is typically placed more to the left of the editor than the right, making it less of a journey to reach the minimap 
- whenever you have multiple editors up, for example using one file for reference ( the right editor ) while coding in another ( the left editor ). Makes it so that the coding editors scroll bar and the references minimap are literally right beside eachother and with ease can navigate the two files by using both
- there are more but I'd rather not convey more of the anal-retentive nerd image I seem to paint myself with

Blacked-out was made with the same design ideas as blued-out.

> [!UPDATE]
>
> As I was waiting for some things to load I added... And for some reason I can't remember the total, and I'm not going back to count again... Lets just agree to agree that the new total count is between 50-55. Doesn't matter at this point really what the total is now because before adding these it was already a rediculous amount in comparison to the marketplace average... of 1 per extension. Noticed there were some gaps missing in comparison to whats available on the color wheel, and had some time to kill so I added a 80's miami theme as well. lol, its god awful but who knows, maybe someone out there may love it since its so loud. I can tell you one thing, it would def stop me in my tracks if I were walking by your station and saw that out of the corner of my eye and say, "what the f...", so if that's what your going for, than this is the theme for you.


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **VSCode & Tailwind Theme Builder**

Create custom themes for both VSCode and Tailwind with live preview and multiple export formats.

**Access:** Web GUI

**Features:**
- Visual theme configurator with live preview
- Export to Tailwind v4 CSS format
- Export to Tailwind v3 CSS format
- Export to VSCode settings file format
- Real-time color customization
- Complete theme control

![Theme Builder](https://raw.githubusercontent.com/8an3/midgardr-notes/main/config/theme.jpg)

---

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Blacked Out**

Ultra-dark theme preset for VSCode with deep black backgrounds and optimized contrast.

**Access:** Settings Dropdown → Select option

**What It Does:**
- Applies ultra-dark theme configuration
- Sets theme for active workspace
- Optimized for reduced eye strain
- Perfect for dark environment coding

![Settings](https://raw.githubusercontent.com/8an3/midgardr-notes/main/config/settings.jpg)

---
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Blued Out**

Dark blue theme preset combining deep blacks with subtle blue accents.

**Access:** Settings Dropdown → Select option

**What It Does:**
- Applies dark blue theme configuration
- Sets theme for active workspace
- Blue-tinted dark interface
- Alternative to pure black themes

![Settings](https://raw.githubusercontent.com/8an3/midgardr-notes/main/config/settings.jpg)

---

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Window Differentiator**

Color-code multiple VSCode windows to easily distinguish between different projects.

**Access:** Settings Dropdown → Select option

**Features:**
- Assign unique colors to each VSCode window
- 20+ color variants available
- Different color applied each time triggered
- Perfect for managing multiple projects
- Quick visual identification

![Settings](https://raw.githubusercontent.com/8an3/midgardr-notes/main/config/settings.jpg)

---

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Reset - Window Differentiator**

Restore default VSCode window colors and remove custom window differentiation.

**Access:** Settings Dropdown → Select option

**What It Does:**
- Removes custom window colors
- Restores default VSCode appearance
- Resets all window color assignments

![Settings](https://raw.githubusercontent.com/8an3/midgardr-notes/main/config/settings.jpg)


---

[🡄 Return](https://github.com/8an3/DevStack)