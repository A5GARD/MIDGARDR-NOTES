# FREYR

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Tailwind For VSCode

> [!NOTE] 
>
> This does not need react or tailwind installed in your vscode instance in order for it to work.

### Step 1: Trigger this features function
This will create a file in your root folder that contains the function to use in your webview, you may move this file to where ever you need / want it.
   
### Step 2: Clean Up Activity Bar
In your webview call this function in your html style section
   
### Step 3: You're Done!

Thankfully, I had already built the majority of the code base needed for this for something else, all that was needed was a quick change of the :root section to include vscode themed colors in place of what was already there.

The use case, or one of them rather, say your building a webview that will include something that you have already built else where. Unfortuantly, it was built using react and tailwind so typically you would have to go over it and readjust all the areas that use tailwind and convert it to the format that can be used within tailwind.

OR what if you would rather just use tailwind classnames instead of trying to learn an entire new styling format in order to build your webview. 

While the styling is long, yes, as the file sits at over 5000 lines of code. While this does include the 80-90% of what you would use with tailwind it is missing the last 10 or so %, for good reason. As that 10% would catapult the 5000 lines you see, to well over 50,000 lines of code. If you absolutely need everything that is needed that tailwind offers, there is a very fast... "cheat" in accomplishing and obtaining it. 

Place the entire css code into a react app that already has tailwind, in its tailwind.css file. Run your dev server so that the tailwind engine outputs everything contained within this file and everything else. Next go to your apps output folder, and within that folder is a css file that tailwind had built for the application. 

Before it can be used in your vscode webview, you will have to replace the :root section with the one that is provided from here.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Color Wheel

Using the color way more than I thought I ever would, I have started to annoyed with the fact that I have to leave VSCode to use it. So... were solving that problem.

There will be 2 versions made, the first being your typical color wheel, but more compacted and displaying the colors vertically. The same design thats on the components site because due to its compact styling, it very neatly fits ona single web page without scrolling.

The second version is ripping apart my color wheel picker, essentially its a different take on a color picker. For a lot of use cases, color pickers just suck. A while back I created a popover that contained the entire color wheel with some nice animations, and whenever you hovered over an of the colors it would display the name and the current color number you were hovering that when clicked on copies the color into the state.

Because it has to fit in a popover without looking stupid, this version is extremely compact, but actually looks... really nice, more than most full page colors wheels that I've seen anyways. Because of just how compact it is, it will fit really nicely in the sidebar with room to spare, for the following feature.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Color Picker

This... honestly has been more of an annoying thing to deal with in terms with finding... at the very minimum a decent picker. I don't like windows power toys color picker, because it doesnt have a zoomed in area. Having found one that I liked off of the microsoft store, it has the zoomed in area I want / need with a nice feature that I cant find anywhere else but everything else about it... fucking sucks, lol.

When it comes to color pickers, I apparently can't win since I've tried about 2 dozen for far.

Some of the functionality will piggy back off of the second color wheel, as this will be placed just above it. 

In addition to its zoomed in area, featured just below it will have a small box stating what current color value the picker is honed in on, in hex, hsl and oklch.

There will 100% be a short cut for this, and because I will use this... a lot, I will obsess over the click to click functionality and process that will happen with it. Currently the way it will work:

1. open picker via short cut or clicking the button in the sidebar
2. zoomed in viewing area will display, there will be a slider to control the actual zoom as well
3. the zoomed viewer, I don't knwo how to do this so we will see if I can accomplish this, but I would love for it take in the colors... in a pixalated format, which would make it so when your moving your cursor there is a slight snap from color to color... if that makes sense. Not to much where you want to throw your mouse against the wall, but just enough that when you go to click to capture the color, that slight button press that so gently your not even breathing to ensure you capture the right fucking color... doesnt bump your mouse enough with that mouse click... to instad capture the color right fucking beside it
4. once clicked it will paste your desried color format value into your clipboard
5. at the same time, this wont actually effect you in any way but these events will happen in sidebar as you continue to work, but there will be a previous 20 selected color swatches that move down one making room for the new color while the color pickers selected color will display the captured color along with displaying the available values for you to copy into your clipbard again if you need it, click on any of the previous 20 will essentially recapture that color and copy the value to your clipboard

If you were in a rush, or having to hurry for one reason or another, it will not impede you in any fashion from, opening the picker, capturing the color, pasting the color where its needed in your code, and letting you immediatly open the color picker again to capture the next color. As long as your desired color value is set up in the sidebar before you start, you should never have to revisit the sidebar unless your color dropped from your clipboard and you need to re-capture it.

The piggy backed funtionality includes:
- whenever a color is capture you can pre configure the settings on exactly how it will copy to your clipboard for example, working with hex colors there will be times it 10 times easier IF the color picker placed just the value, without the hash symbol into your clipboard so you can paste it into your code, that much more easily. While other times, where your not replacing another hex value with the one you want / need, then you would want the hash symbol to be included when it gets copied over into your clipboard. Hex is not the only color format with these... annoying formatting tendencies as it seems when it comes to color formats and their use around different apps or whatever, it really feels like... the person who started the project no longer works there and someone else had to pick up the project to finish it, but not know a single thing that was coded in previously and feels like the least cohesive system ever, Yes, I know it's across different products... but you can't sit there and tell me, the devs who picked up off where the previous finished... couldn't have continued on with atleast the slightest thought about ux.
- you will be able to also choose the format from a long list of color formats that will be used when copying it over into you clipboard
- there will be a short list under the color wheel feature that color but in different color formats as buttons so whenever it is clicked it copies a different value into your clipboard. For example if your working with converting a theme between 2 different tailwind versions, no matter what you choose as your desired format, when ever you need to quickly capture the opposing versions format, atleast you can do so without having to reconfigure the color picker for the other format, re capture the exact color, only to have to re configure back to the original color format you were working with

This is such a simple, and small tool... I really don't understand how there are so many pickers out there, that have one amazing thing about them... but then fall short on virtually everything else

... omg... the second the second version opened... it was love at first site... it fits so fucking perfectly...

sigh... after all that... perfectly get the eye dropper working, converting a react eye dropper to vanilla... making sure everytihng works... only to see it disappear as I mouse over vscodes edge due to the sandbox... your sandboxes have never stopped me before. Since then I've found several more bugs with escaping the sandbox and run commands as user on the machine entirely free of vscodes sandbox and node enviroments entirely, you guys should respond to your emails because if these events don't bother you as much as it seems, then I can finally code those features into the extension. And if your a user reading this, don't worry I won't be coding things like that into the extension, and just patiently wait till microsft responds because I really want those features. Such a roller coaster of emotions at times, lost all hope proding with different methods in order to get something to work for hours on end... finally ends up working so your over the moon... then it dawns on you, what actually took place in order to make it happen, then you loose all hope again, lol because microsoft doesn't want to call you back. One of the features is for the layout engine gaining the ability to toggle extensions on and off from a workspace context or layout context allowing you to have complete control over the performance and customizing your coding enviroment perfectly for the task at hand instead of just running everything, all the time. Where as if you tailer that work enviroment like that, users would no longer have performance issues, and would see huge gains in regards to that since vscode resembles more like an axe as it just tries to power through everything, in comparison to what it could be, a surgical razor sharp tool like a katana, that does exactly what it needs to do by going about what has to happen with percision. 


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> VSCODE & TAILWIND STYLING

- [Themes](#themes)
- [VSCode & Tailwind Theme Builder](#vscode--tailwind-theme-builder)
- [Blacked Out](#blacked-out)
- [Blued Out](#blued-out)
- [Window Differentiator](#window-differentiator)
- [Reset - Window Differentiator](#reset---window-differentiator)


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Themes

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

> [!NOTE]
>
> FEB 7, 2026: As I was waiting for some things to load I added... And for some reason I can't remember the total, and I'm not going back to count again... Lets just agree to agree that the new total count is between 50-55. Doesn't matter at this point really what the total is now because before adding these it was already a rediculous amount in comparison to the marketplace average... of 1 per extension. Noticed there were some gaps missing in comparison to whats available on the color wheel, and had some time to kill so I added a 80's miami theme as well. lol, its god awful but who knows, maybe someone out there may love it since its so loud. I can tell you one thing, it would def stop me in my tracks if I were walking by your station and saw that out of the corner of my eye and say, "what the f...", so if that's what your going for, than this is the theme for you.
>
> FEB 8, 2026: An update... to the previous update, lol. 
> There are now 140+ total themes to choose from. This total comes from 70 themes that all contian themed color tokens and semantic color tokens. Personally, I don't like the themed syntax highlighting but I know there are people out there that will go nuts for it, sitting there frantically clapping their hands together the first time they lay eyes on it. At the same time I know there are people, like myself, who do not want that. 
> 
> FEB 10, 2026: For each of the provided themes there is a "base" variant, that uses vscodes default dark syntax highlighting in place of the themed version because I was quite jealouse due to the themes turning out... way better than expected and not being able to use any of theme. The moment I tried coding with any one of theme since I tried multiple themes to find a syntax hightlight theme I could live with but trying each of them, I was like, "NOOPPEE". I'm pretty sure somewhere above I said this feature would get even more rediculous compared to the competing marketplace offerings, well I told ya so. Who knows there may be one out there, but the themes I've seen and installed... for some reason I've not once seen a theme that offered both a syntax theme and a default version of it without it. It's weird, as I continue to code I find a lot of features that I would consider to be the industry norm / default way of doing things, only to find out that even paid options don't even offer the same feature parity.
>
> FEB 11, 2026: As I was building my own theme completely from scratch I have noticed, I wasn't including as many items to each theme as I could have. This update... will take me a while since each theme will be almost tripling in size. Theres nothing wrong with the current themes, they're fucking great. It just bugs me knowing that, I could easily do better, albeit taking a while to complete. Not only will each theme look great given its base colors that are already set out in each theme, but every single theme will have the same level of depth with attention to detail.
>
> And I'll admit, I'm trying to cheat as much as I can by getting ai engines to help with this task but due to the size of the themes, they are becoming quite token heavy and can only complete a couple at a time, while I also manually edit them as well. Speaking of which, just burned through another quota and have to wait another 3 or so hours before receiving help again with this task, fuck I'm not even half way through, sigh that sucks, lol
>
> 



## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Blacked Out

Ultra-dark theme preset for VSCode with deep black backgrounds and optimized contrast.

**Access:** Settings Dropdown → Select option

**What It Does:**
- Applies ultra-dark theme configuration
- Sets theme for active workspace
- Optimized for reduced eye strain
- Perfect for dark environment coding

![Settings](https://raw.githubusercontent.com/8an3/midgardr-notes/main/config/settings.jpg)

---
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Blued Out

Dark blue theme preset combining deep blacks with subtle blue accents.

**Access:** Settings Dropdown → Select option

**What It Does:**
- Applies dark blue theme configuration
- Sets theme for active workspace
- Blue-tinted dark interface
- Alternative to pure black themes

![Settings](https://raw.githubusercontent.com/8an3/midgardr-notes/main/config/settings.jpg)

---

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Window Differentiator

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

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Reset - Window Differentiator

Restore default VSCode window colors and remove custom window differentiation.

**Access:** Settings Dropdown → Select option

**What It Does:**
- Removes custom window colors
- Restores default VSCode appearance
- Resets all window color assignments

![Settings](https://raw.githubusercontent.com/8an3/midgardr-notes/main/config/settings.jpg)


---

[🡄 Return](https://github.com/8an3/DevStack)