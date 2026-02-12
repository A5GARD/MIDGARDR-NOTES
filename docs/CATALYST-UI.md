# MIÐGARÐR SDk

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Table of Contents**
 

## [MIÐGARÐR: Formerly known as CATALYST UI LIBRARY](#miðgarðr-formerly-known-as-midgardr-library)
- [Editor Context Insert](#editor-context-insert)
- [Quick Pick Insert](#quick-pick-insert)
- [Automated Installation](#automated-installation)
  - [UPDATE: Configure Import Call](#update-configure-import-call)
  - [Installation](#installation)
    - [Quick Start](#quick-start)
    - [Menu](#menu)
  - [Premium Access](#premium-access)
  - [Component Categories](#component-categories)
    - [Primitives](#primitives)
    - [Forms](#forms)
    - [Data Display](#data-display)
    - [Navigation](#navigation)
    - [Feedback](#feedback)
    - [Interactive](#interactive)
    - [Utilities](#utilities)
  - [Package Managers](#package-managers)
  - [Configuration](#configuration)
    - [Config File (Optional)](#config-file-optional)
    - [Config Options Explained](#config-options-explained)
    - [Auto-Install with Config](#auto-install-with-config)
    - [Tailwind Setup](#tailwind-setup)
    - [Utils File](#utils-file)
  - [Requirements](#requirements)
    - [Utils File](#utils-file-1)
  - [Examples](#examples)
    - [Installing a Button Component](#installing-a-button-component)
    - [Using the Button Component](#using-the-button-component)
    - [Installing Multiple Components](#installing-multiple-components)
  - [Component Import Paths](#component-import-paths)
  - [Features](#features)
  - [Dependencies](#dependencies)
  - [File Structure](#file-structure)
  - [Support](#support)
  - [License](#license)

## [VS Code Integration Features](#vs-code-integration-features)
- [Smart Prop Autocomplete](#smart-prop-autocomplete)
- [Signature Help](#signature-help)
- [Hover Documentation](#hover-documentation)
- [Auto Import](#auto-import)
- [Go To Definition](#go-to-definition)
- [Missing Import Warnings](#missing-import-warnings)
- [In Editor Comp Autocomplete](#in-editor-comp-autocomplete)
- [Developer Experience Achievements](#developer-experience-achievements)

## [Tool Suite](#tool-suite)
- [Development Tools](#development-tools)
  - [VSCode Cmd Reference](#vscode-cmd-reference)
  - [Markdown Cheat Sheet](#markdown-cheat-sheet)
  - [IRIS: Color Tools](#iris-color-tools)
    - [IRIS: Color Converter](#iris-color-converter)
    - [IRIS: Color Wheel](#iris-color-wheel)
  - [React/Tailwind Sandbox](#react-tailwind-sandbox)
  - [Theme Builder](#theme-builder)
  - [Typography Tester](#typography-tester)
  - [Layout Generator](#layout-generator)
  - [X Tester](#x-tester)
  - [Components Reel](#components-reel)
  - [Tailwind Converter](#tailwind-converter)
  - [Animation Builder](#animation-builder)
  - [Responsive Design Helper](#responsive-design-helper)
  - [Code Carousel](#code-carousel)
  - [Sandbox](#sandbox)
  - [Icons](#icons)
  - [RÚNAR Editor](#rúnar-editor)
  - [Regex Tester](#regex-tester)
  - [JSON Formatter & Validator](#json-formatter--validator)
  - [API Response Mocker](#api-response-mocker)
  - [Lorem Ipsum Generator](#lorem-ipsum-generator)
  - [Cron Expression Builder](#cron-expression-builder)
  - [UUID Hash Generator](#uuid-hash-generator)
  - [Code Diff Viewer](#code-diff-viewer)
  - [Flexbox Sandbox](#flexbox-sandbox)
  - [Grid Sandbox](#grid-sandbox)
  - [QR Code Generator](#qr-code-generator)
  - [Responsive Preview](#responsive-preview)
  - [Accessibility Checker](#accessibility-checker)
  - [Animation Builder](#animation-builder-1)
  - [Chart Playground](#chart-playground)
  - [MD Badge Builder](#md-badge-builder)
  - [Spinner Generator](#spinner-generator)
  - [Terminal Menu Generator](#terminal-menu-generator)
- [ENCODER_DECODER_LAB](#encoder_decoder-lab)
  - [Image to Base64](#image-to-base64)
    - [PNG to Base64](#png-to-base64)
    - [JPG to Base64](#jpg-to-base64)
    - [WEBP to Base64](#webp-to-base64)
    - [PDF to Base64](#pdf-to-base64)
  - [Base64 to Image](#base64-to-image)
    - [Base64 to PNG](#base64-to-png)
    - [Base64 to JPG](#base64-to-jpg)
    - [Base64 to WEBP](#base64-to-webp)
    - [Base64 to PDF](#base64-to-pdf)
  - [Data Conversion](#data-conversion)
    - [CSV to JSON](#csv-to-json)
    - [Image to SVG](#image-to-svg)
      - [PNG to SVG](#png-to-svg)
      - [JPG to SVG](#jpg-to-svg)
      - [WEBP to SVG](#webp-to-svg)
    - [Media Conversion](#media-conversion)
      - [MP4 to MP3](#mp4-to-mp3)

## [SKALD: Monaco Editor](#skald-monaco-editor)
- [Monaco Editor Overview](#monaco-editor-overview)
- [Feature Set](#feature-set)
- [Special Characters](#special-characters)
- [PRE_MADE_ASSETS](#pre_made_assets)
  - [File Trees](#file-trees)
  - [Progress Bars](#progress-bars)
  - [ASCII Tables](#ascii-tables)
  - [Spinners](#spinners)
  - [Terminal Dashboards](#terminal-dashboards)
  - [Code Block Previews](#code-block-previews)
  - [Terminal Menus](#terminal-menus)
  - [Terminal Logs](#terminal-logs)
  - [Git Branch Visualization](#git-branch-viz)
  - [Status Indicators](#status-indicators)
  - [Notification Boxes](#notification-boxes)
  - [Output Separators](#output-separators)
  - [Nested Data Visualization](#nested-data)
  - [Activity Timeline](#activity-timeline)
  - [Terminal Dashboards](#terminal-dashboards-1)
  - [Box Drawing](#box-drawing)
  - [Various Spinners](#various-spinners)
  - [Badges and Logos](#badges-and-logos)
- [Documentation Tools](#documentation-tools)
  - [Readme Generator](#readme-generator)
  - [Readme Templates](#readme-templates)
  - [Remote Access](#remote-access)
  - [Local Settings](#local-settings)

## [MIÐGARÐR UI](#miðgarðr-ui)
- [Overview](#overview)
- [Features](#features-1)
  - [Component Library](#component-library)
  - [Built-in Tools](#built-in-tools)
    - [Development Environment](#development-environment)
    - [Utility Tools](#utility-tools)
    - [Reusable Project Tools](#reusable-project-tools)
- [Component Insertion Methods](#component-insertion-methods)
  - [Editor Context Menu](#insert-component-via-editor-context-menu)
  - [Quick Pick Menu](#insert-component-via-quick-pick)
- [Installation Guide](#installing-midgardr-components)
  - [Installation Methods](#installation-1)
    - [Quick Start](#quick-start-1)
    - [Menu](#menu-1)
  - [Premium Access](#premium-access-1)
  - [Component Categories](#component-categories-1)
    - [Primitives](#primitives-1)
    - [Forms](#forms-1)
    - [Data Display](#data-display-1)
    - [Navigation](#navigation-1)
    - [Feedback](#feedback-1)
    - [Interactive](#interactive-1)
    - [Utilities](#utilities-1)
  - [Package Managers](#package-managers-1)
  - [Configuration](#configuration-1)
    - [Config File (Optional)](#config-file-optional-1)
    - [Config Options Explained](#config-options-explained-1)
    - [Auto-Install with Config](#auto-install-with-config-1)
    - [Tailwind Setup](#tailwind-setup-1)
    - [Utils File](#utils-file-2)
  - [Requirements](#requirements-1)
    - [Utils File](#utils-file-3)
  - [Examples](#examples-1)
    - [Installing a Button Component](#installing-a-button-component-1)
    - [Using the Button Component](#using-the-button-component-1)
    - [Installing Multiple Components](#installing-multiple-components-1)
  - [Component Import Paths](#component-import-paths-1)
  - [Features](#features-2)
  - [Dependencies](#dependencies-1)
  - [File Structure](#file-structure-1)

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Editor Context Insert**

Inserts selected component at cursor via the editor context menu. Menu options will be based upon current subscription status.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Quick Pick Insert**

Copies the selected component into your clipboard via the quick pick menu located in the status bar. Menu options will be based upon current subscription status.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Automated Installation**



## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Smart Prop Autocomplete**

Pressing ctrl & spacebar while your cursor is inside the quotations of any props value will bring up an intellisense dropdown with the available prop values that can be assigned.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Signature Help**

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Hover Documentation**

Whenever hovering over a components name a hovercard will appear with its relevant documentation, removing the need to ever visit the site. The card will contain the following:
- name
- cateogry
- import statement
- basic usage example
- usage example
- props
- link to the components url to quickly navigate straight to the page instead having to make us, open a browser, go to the landing page.... ya no
- if the component is a primitive or uses any primitive, links will be provided to radix ui's site
- dependencies
- features list 
- tags list

Personally, it really bothers me when a library uses a component to build off of... and not provide the apis to use the thing. To make matters WORSE, I've noticed libraries aren't even providing links... the components documentation page, lets just build something, ship it... and if the user needs something... fuck it they can figure it out right?

With so much on my plate, I too have forgotten to include it, but I won't just be including the links, personally that alone I think is absurd. I understand, devs are used to a shitty fucking user experience... and don't expect one because it's just that bad.

Instead each component that uses any one of the primitives, there will be a second props table added displaying all the props values for that primitive straight from the radix ui, or whoever the provider is. 

Thus truly ensuring that you do not need to minimize or open another window while coding as all the information, components and everything else you need, is already here.





## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Auto Import**

To auto import the component right click the components name where ever it may be used within the editor, select `Add Import` in the editor context menu. 

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Go To Definition**

Using cmd & ctrl & clicking the components name will bring up the source codes file in a, sheet style dropdown? I don't what what you call this really, any how, it allows you to view the source code file without navigating to it, while at the same time double clicking anywhere inside the "dropdown sheet" will navigate you to the source code file itself.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **In Editor Comp Autocomplete**

Whenever you start to code a component `<`, pressing ctrl & spacebar will bring up the intellisense dropdown containing every single component currently available in the library, all 2500+.

> [!IMPORTANT]
> As far as you or myself using the components library, I beleive the above mentioned features finally completes all the goals I set out in regards to the UI library and delivering the absolute best DX... possible.
>
> 1. Accessibility to any component without visiting the site - Acheived through the editor and quick pick menus that inserts the relevant usage example right into the editor
> 2. Shorten the length to mastery - Achieved but still on going, as this is more done so on the side of the actual components them selves. There are many faucets to this goal some examples include, removing as many required props as possible, where ever possible in the case of tabs you do not have to supply a default tab value, or values for any of the tabs themselves, providing default values... literally anywhere, and every where that I could which also saves you from remembering from what is required whenever using a component.
> 3. Providing the easiest to use components - Achieved, to be honest I replicated and expanded upon the build processs of components that shadcn used. As they were the first library I had ever used that whenever you used a component, it not only made sense but each component was easy to use.
> 4. Remove as much friction as possible to install the components - This by far is better than any other single compnents library, anywhere. Using the npm library there are several options on what to install or if a components name is provided then installtion of that one component. To top it off, whenever you select options like full installation, it literally does EVERYTHING:
>   - installs all components
>   - installs all required libraries
>   - checks to see if tailwind is already installed, if not installs it
>   - configures tailwind and goes so far as configuring everything else needed to run tailwind
>   - creates tailwind.css
>   - depending on the selection you get a basic tailwind.config.ts or an extremely feature rich version of it, grating access to over 18,000 configrations that you can change your projects font, theme and preset ( padding, margins, etc )
>   - whenever a component is installed, whether it is the full installation or just a single component, it creates a new index file in the relevant locations so as you get to use `~/components/midgardr` for literlly every single component no mattter the location
>   - just today I added, 'Configure Imports' which takes the previous item... a whole step further by configuring the tsconfig and package.json files so that all you have to do to import a component is `#catalyst` and if you use the icon library as well `#icons`. Now that I think of it, I've never ever... seen a dev or heard of one use this technique. I know as of late, a ton of devs are moving towards the @ in place of the tilde ( ~ ), to save typing the slash, but if your going to so far as to configuring your project so that you save typing a single character... why wouldn't you go the step further and do this? Since it saves you typing out a shit ton of characters... **shrugs**, anyways this feature is also trigger whenever you use full installation
>   - all in all, it provides a one clickesque solution for everything related to the library. I say one clickish, because it used to be such when it was implemented in the extension and only moved it to its own npm library to offer more variations for installation, but still it's just a single command. There isn't one other library that I know of that comes close to that... to my knowledge anyways. To this day, I beleive I have tried them all, that are react based anyways, as I will touch exactly why I tried them all in the next point.
> 5. Completely removing the need in having to 'need' more than one library - When trying to fulfill this goal, I was shocked at the current trend. The main larger libraries, it feels as if each one of them started with an idea that was either specialized or somewhat so and never really expanded upon once they reached that initial goal. Meanwhile, the lazy copy cats create an exact carbon copy of shadcn without adding anything of their own, or if they did or it was at first perceived that they did, it was one... maybe two items at most. Thus, each main library has massive holes in its offered inventory that leaves users... wanting / needing more. For example, the amount of hooks in this library, is unparallel to say the least, but there is only a single other library that can even be considered as coming close in terms of total hooks. While yes, the foundation of this libraries components used shadcn's but if you look at them today, you wouldn't be able to discern that fact. As each and every single one of them have been edited and expanded upon. Not to mention, a whole category, x, that no one else has, an entire animations category, a tool suite unlike any other I've ever seen, a ever growing blocks category in which I try to copy over any page that I code whenever I think of it, and to top it off unique reusable tools that if they aren't available yet they soon will be since they're on the to do list such as: 
>   - events calendar
>   - calendar
>   - automotive calculator
>   - messenger
>   - rich text editor - completely custom, unlike everyone else that wraps tiptap or some other library
>   - table - while the current iteration does wrap another library, it does however host features I have yet to see anywhere else in terms of ease of use and flexibility. Once I have the time... I do plan on creating my own table... but this I foresee taking... A LOT of time in doing it right
>   - and more... Currently, none of the others come to mind though
> There were several other goals but you get the point.
>
> Meanwhile, I was able to achieve something that I had NOT set out to do in regards to the X category. If you had asked me early on when I was first learning to code, do you think you would create a new method in creating react components? I would have not beleived you so much that, not only would I disregard it immediately but it would never cross my mind again to think about. Not only doing just that, but in a way that comes with all the benefits it does all the while at zero cost to the user when using it, didn't see that one coming. Today, I started to replace the main page of the theme builder and decided to use it as a... I wouldn't call it a proving grounds but a place to showcase the new category by giving each component a hover card with the code that was used to implement it. Besides saving a ton of space in terms of files ie, instead of having 100+ files devoted to different variants of inputs... it's just one. I noticed it also reduces a ton of code needed when actually implementing any one variation. So much so, that I will probably leave in the original section that I used, but edit so that each component comes with a hovercard with its implementation of code, so as you can see the difference.
>
> The other big plus I never saw coming, in terms of helping users ( despite still seeing devs still struggle with everything it solves ). Loki AI, as its now called, not only solves virtually every single issue you come across as a dev, and thats not an exageration, but have also cracked the limitation on being limited by an AI engines data training set. While The first point is already out and written about, the latter I'm still testing but the how to should be out soon. The weidest part about that is, getting these results uses methods that are already out there... just used differently.
>
> Knowing that all the goals have been completed... is satisfying. Especially given the fact that, this kinda sucked. Not so much from a coding perspective, but due to its size and with items to do such as providing hover card documentation for every single component... that sucks, but where ever I can and as much as I can I try to find ways to code it so that it takes care of itself. There have been so many days, where I thought I was going to be able to move on to something else only to find out after coming on... that no... there are things to be done with the ui library. Even now, there is still a massive update/change to severel large items that are held up in being pushed due to a couple of smaller other items, I just hope they don't need changes when I can finally test them in a prod enviroment.
>
> After typing this out, it had given me an idea by asking myself "Can we take it further?", it seems as though we can. Creating a new npm library called 'forge' it now acts as a cetralized CLI that grants access to all the libraries in one place along with, depending on the selected option, creating one command that install / updates the relevant libraries and packages. Creating a new remix run project, which will get replaced with a new creator soon, once the new project has been created it then installs icon and the ui library including installing, configuring all of tailwinds requirements and all the other smaller configuration goodies that come along with installing the library as well. I forgot to mention it even checks to see whether you have the vscode extension currently installed and at what version, prompting you to either update or installing it just like the other libraries. 
>
> Other than the create-remix2 replacement, I corrently do not see any other avenue in which it can be improved upon in terms of ux/dx. 

# Tool Suite
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Mathmatical Color Converter**

> [!NOTE]
>
> While I admit this being a bit more of an advanced tool, I promise that no matter what skill level you are currently at in terms of building themes or generating picture perfect UI color schemes, this will catapult your skill level far beyond what it should be. And I will go over this, as if you know nothing about colors... will barely even mention the proper terminology in order to explain everything.
> 
> Currently, I know enough about colors, color palletes, hues, shading and all other matters pertaining to colors, to know that... I fucking suck at making themes from scratch. At this knowledge level  I currently won't even waste my time trying because I know that there is an art to picking a color pallete that everyone will lov, but I did not attend art school although I am good at other things. 
>
> For example, math and science is every where and while art really... doesn't have anything to do those topics, maybe we can find some math in art. As I was staring at some one elses theme, I just kept asking myself, "How the fuck did they get that "input" color from that "background" color? Like what sliders or knobs do you need to use in order to achieve that end result?". Not even bothering with taking on that challenge, and attempting to achieve that same input color by playing with a bunch of color sliders. 
>
> Thankfully at this point I asked myself, "Is there a way to mathmatically calculate the difference between these two colors?" Again, thankfully when I took this question to an ai prompt... it didn't take long to convey what I wanted to get done.
>
> I'll be using a common libraries resource for this so as to make it a lot easier to provide the correct colors and a visual to go with the explanation if you need it. Go to [shadcn](https://ui.shadcn.com/)'s home page, to the right of the tabs there is a dropdown that allows you to select a theme, currently I'm on dark neutral.
>
> Click on the copy button beside the dropdown so you can open the color swatches that the theme is based off of, because when using a color picker with a live theme it's not always the most reliable  in extracting the exact color you want as it tends to change as you move the mouse around. To keep everyone on the same page, please use the background swatch found in the dialog that pops.
> 
> So using whatever color picker you have available to you, if you don't have one and are on windows pressing windows key + shift + c, will trigger a color picker if you have power toys installed ( a windows app ). If you don't have that installed ( or even if you do since this tool I'm about to go over is a lot better ), using microsfts store, download 'desktop color picker pro' its free and it features a cursor/picker with a zoomed in view so you can properly get the right color whenever you are trying to extract it from any ui. 
> 
> If you don't know what I'm talking about, install this tool and just going around your ui and look at different colored elements and you will see, for example blue text... isn't always exactly blue text, when you zoom in, it features different shades of blues, greens, whites, yellows and without that zoomed in view of what you are clicking on to extract the exact color you want... you could be sitting there for... 2, 4, sometimes even 10 minutes randomly click the same blue character... just to get the blue you see on the screen.
>
> With your color picker hover over background color swatch and you should get '#0A0A0A', and after checking the actual background it matches so this is perfect. Looking at the rest of the ui, you will notice that the inputs are not as dark, being slightly lighter in color, and active items even more so such as the radio group.
>
> While shadcn/vercel probably has a staff member or two who have art degrees, we're going to try to cheat our way to the top when it comes to creating picture perfect themes.
>
> Using your color picker hover over one of the inputs that does not change color... when you hover over it with the picker, and you should get a value of '#161616'
>
> Is there some possiblity of mathmatically determining how to achieve the same color difference between that background and input color, and then take any background color and find out what the correct color value should be used for its input? To expand on it even further, can we use that same formula/function and just slightly change the knob ( values ) in order to also determine what our active radio group colors should be? Well... apparently there is.
>
> I won't dive into the actual math, but now that you get the idea behind this in what this tool sets out to achieve, I can go over the converter.

The converter will contain 4 parts, parts 1 and 2 will work along side one another and parts 3 and 4 will work on their own.

The first section, will take in that background color in the first input and also take in that input color in the second input. When these two values are populated there will be a result that pops up that gives you the exact number you need in order to complete the next step.

Working on whatever theme you are, taking whatever color you need to start with, place it within the first input. The tool should already have the value derived from the previous step so it will automatically produce a color value that is mathmatically the same difference between itself and the color you just provided, as it is for the first two colors you provided. 

Now you aren't limited to just background and input colors, as you can use the same formula on a number of things in order to find the perfect color to use in combination with the first color. And since the first step, calculates what the actual difference is between the two, it doesn't matter how much of a difference there is.

The third section will contain an input and to the right of it you will be able to adjust the rgb value up or down to dynamically to achieve the same result that would be produced above, but allowing you to visually see a mathmatically correct color across its sliding values in comparison to sliding the color knob on a 16 different colored background.

The fourth section, while similar to the previous, uses a different formula that you can change the value of the given percentage in order to slide up and down that color range.

Depending on where, exactly the color is from in terms of the spectrum the mulitpler method gets messy with low color values, which is why I decided to include both of them.

Hopefully, I explained this in a way that anyone from any skill level can understand, even if you never created your own theme before. Personally, I wish I had a tool like this when I started playing around with themes. The hours I spent staring at other peoples themes just wondering how exactly they got the colors they did that were based off of the backgrounds and such and going so far as attempting to play with the hues and such to attempt in getting the same result... omg. This literlly takes a task that, without that degree, would take hours in order to properly get the perfect color to use and cutting it down to seconds. And yes, I know those art majors probably have some stupidly expensive art software where it does exactly the above for them too.

Personally, I will be taking these exact formulas and pumping them into my theme builder, which will enable me to... with very little inputs, create the perfect theme every time. This will be achieved by supplying a hex value and the mulipler value into a function, in order for it to calculate it on its own by setting the values once and letting it do the rest.

```jsx
export function getInputColorByOffset(hex: string, multi = 10) {
  // Remove # if present
  const cleanHex = hex.replace('#', '');
  
  // Parse RGB values
  const r = parseInt(cleanHex.substring(0, 2), 16);
  const g = parseInt(cleanHex.substring(2, 4), 16);
  const b = parseInt(cleanHex.substring(4, 6), 16);
  
  // Add "multi" to each channel, clamp to 255
  const newR = Math.min(r + Number(multi), 255);
  const newG = Math.min(g + Number(multi), 255);
  const newB = Math.min(b + Number(multi), 255);
  
  // Convert back to hex
  return '#' + 
    newR.toString(16).padStart(2, '0') +
    newG.toString(16).padStart(2, '0') +
    newB.toString(16).padStart(2, '0');
}

export function getInputColorByMultiplier(hex: string, multi = 1.83){
  // Remove # if present
  const cleanHex = hex.replace('#', '');
  
  // Parse RGB values
  const r = parseInt(cleanHex.substring(0, 2), 16);
  const g = parseInt(cleanHex.substring(2, 4), 16);
  const b = parseInt(cleanHex.substring(4, 6), 16);
  
  // Multiply by "multi", round, clamp to 255
  const newR = Math.min(Math.round(r * Number(multi)), 255);
  const newG = Math.min(Math.round(g * Number(multi)), 255);
  const newB = Math.min(Math.round(b * Number(multi)), 255);
  
  // Convert back to hex
  return '#' + 
    newR.toString(16).padStart(2, '0') +
    newG.toString(16).padStart(2, '0') +
    newB.toString(16).padStart(2, '0');
}
```

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **VSCode & Tailwind Theme Builder**

Obviously I enjoy looking at a nice user interface, who doesn't? The real question is, who wants to build themes the way microsoft intended with vscode? Fucking nobody... My god, this is a prime example on how to not include a feature. Especially a feature that so many people would want to use at varying skill levels.

This being such a complicated task to complete it took me ages, just to work up the confidence to start editing that object in the settings.json file... let me re-phrase that, it took me ages just to learn on how to find out what values are needed to be modified in order to create a theme in the first place, unbelievable.

Seriously, the system that vscode created to edit the theme is simply, just garbage, but we have to endure it because... that's how you edit the theme. After creating... about the third theme I stopped creating them all together. Once I got good enough at coding, I created a tailwind theme builder that maps the same tailwind theme to all the elements found in vscodes UI. Making it so that creating a vscode theme, no longer sucks.

Now the theme builder is currently at it's umphteen revision, it does quite a lot more while solving some critical UX problems... that nobody even seems to be attempting to solve. 

Like color pickers? I know you, myself and every other dev has just lived with these things, but fuck do they suck when building a theme. Taking an exercise that, lets be honest, takes a while all on its own but then whenever you want to manually customize a color and use that color picker, your adding a unknown multiplier thats based on how perfect you want the theme to look and then again, multipling the time by the amount of custom colors you want to customize. Who wants to build themes like that? Again, fucking nobody. So along side every single color picker, just in case that one person out there that wants it, there is a new style of color picker that, tbh I've never seen created anywhere else in any context. Simply named, the color wheel picker. Instead of making you dial in each color with 6 different knobs, it just provides every option available on the color wheel. Whenever you hover over a color, a tooptip displays with the colors name and number value. It works so much better, here on out I will be droping the color picker all together and use the color wheel picker in its place, except for uses cases like this theme builder.

![Z](https://raw.githubusercontent.com/8an3/midgardr-notes/main/freyr/colorwheelpicker.png)

### Live Previews

The theme builder hosts a number of live previews so you can see exactly what your building as you build it, consisting of but not limited to:
- a webpage that features a host of components to ensure you know exactly the theme your building for your tailwind.css file
- a recreated vscode user interface that achieves the same as above
- lastly a specialized vscode interface that hosts a number of different files to view that you can change from switch tab to tab, just like you do in vscode. Each file features a different language so that you can preview token colors and semantic token colors that change how the syntax highlighting looks as you build on the fly. This is another feature, I have yet to see elsewhere

### Color Output Formats

Due to working in so many enviroments it obviously outputs in more formats than the current tailwind version, such as:
- tailwind v4
- tailwind v3
- settings.json ( so you can paste it straight into your file )
- while the last one doesn't exactly have a name per say, but it outputs the exact object you need in order to create your very own vscode theme extension. Actually... as it includes all the colors needed, all the values that are required, the token colors you have chosen along side the semantic token colors as well

### Intelligent Color Mapping

This one took a while to get right but when it was perfected... it really made the exercise of creating a vscode theme a breeze.

Whenever you select a preset theme configuration, or whenever you select a color to use in your tailwind theme it automatically applies the same colors to your vscode theme, token colors and semantic token colors. 

In the time it takes to create a tailwind theme, you now have two other output options that you can choose from for setting that same theme in vscode.

Not only does it provide the perfect vscode theme to quickly paste into your project, it also provides THEMED token colors its semantic counterpart. Thus taking a task that was usually only being done, by seasoned devs and opening it up to virtually... any skill level. Not to mention, drastically cutting down the required time in creating themes 100 fold.

MEANWHILE, the theme builder still lets you custmize each vscode color option whenever you go to individually custmize it. So if you hate the color of the border that used in your tailwind theme, no problem change it.

### Closing Notes

Obviously, I do not stick to industry norms when it comes to things and since I already have a vscode UI, why not squeeze more out of it. Ontop of visually see what colors do what and where, I've also added options to change several elements in the ui itself as well. For example, toggling breadcrumbs, minimap, and a long list of other UI manipulation features that are found in vscode.

The theme builder is up and does all the points listed above. Just don't mind the tailwind section as I use it to build more complicated than normal components by putting them through there paces over several examples. So if you see some components that are kind of messed up thats why but I hope the awesomeness of the theme builder as a whole makes you overlook that.

---

 


# SKALD
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Monaco Editor**

If this were anyone elses extension, this would be it's own extension but in this extension it is classified under the tool suite. What first started out as a simple markdown editor, it has since evolved into a full blown monaco editor with 150+ custom features with each feature making it become more and more a full blown ide. 

I have used this so much more than I ever thought I would and because of this it continues to receive regular updates. The largest update to date, is just about to be pushed to the site and will host a list of features so large I cannot remember them all to list but here are some of the features that will be available.


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **MIÐGARÐR SDK**
