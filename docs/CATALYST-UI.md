# MIÐGARÐR SDK: Formerly known as CATALYST UI LIBRARY

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

## UPDATE

Adding a new line option 'Configure Import Call'. Configures your package.json and tsconfig.json files to allow the use of '#icons' and '#catalyst' in-place of the traditional '~/components/midgardr' and '@catalystsoftware/icons'

```javascript
import { Command, CommandGroup, CommandItem, CommandList, cn } from '#catalyst'
import { X } from '#icons'
```
Selecting the full installation will also configure your project for this use as well.

## Installation

### Quick Start

Install a single component:

```bash
bunx @a5gard/migardr-ui button
```

### Menu

```bash
bunx @a5gard/migardr-ui
```

Then select from the interactive menu:
- **Full Install** - Components + Libraries + Tailwind + PostCSS
- **Full Install with Ngin** - Includes 18,000 Tailwind config presets
- **Components + Libraries** - Install without config files
- **Configure Tailwind + PostCSS** - Setup only
- **Configure Tailwind + PostCSS w/ ngin** - Setup with preset that contains 18,000 configurations set with only 3 variables
- **Select Components** - Choose specific components
- **Create Config** - Creates config file that can be used in conjuction with the bunx command

## Premium Access

Unlock the full component library with a premium access key:


Premium features include:
- Access to all 2000+ components
- Advanced interactive components
- Specialized tools and utilities
- Priority updates

## Component Categories

### Primitives
Core UI components following modern design patterns:
- Button, Input, Select, Checkbox, Radio, Switch
- Dialog, Sheet, Popover, Tooltip
- Card, Badge, Avatar, Separator
- Accordion, Tabs, Collapsible
- And more...

### Forms
Advanced form components with validation:
- Input variants (masked, OTP, password)
- Date pickers and calendars
- File uploads and dropzone
- Toggle groups and button groups

### Data Display
Components for presenting data:
- Tables with sorting and filtering
- Charts and data visualizations
- Timeline and progress indicators
- Empty states and skeletons

### Navigation
Navigation and layout components:
- Menus and navigation bars
- Breadcrumbs and pagination
- Sidebars and dual sidebars
- Command palette

### Feedback
User feedback components:
- Alerts and notifications
- Toast messages
- Loading spinners
- Progress indicators

### Interactive
Advanced interactive elements:
- Drag and drop
- Resizable panels
- Image zoom and crop
- Code editors with syntax highlighting

### Utilities
Helper components and hooks:
- Custom hooks (useTimer, useCopyToClipboard, etc.)
- Auth utilities
- Server middleware
- Context management

## Package Managers

Catalyst UI automatically detects and uses your package manager:
- npm
- pnpm
- yarn

## Configuration

### Config File (Optional)

Create a `config.midgardr` file in your project root to customize installation behavior:

```bash
bunx @a5gard/migardr-ui
# Select: Create Config File
```

Or create it manually:

```jsonc
// catalyst.config.jsonc
{
    "theme": "blue",                      // presetting the theme
    "preset": "MODERN",                   // presetting the preset
    "font": "Geist",                      // presetting the font
    "all-components": false,              // auto-install all on `bunx @a5gard/migardr-ui`
    "install-tailwind": true,             // install Tailwind dependencies
    "configure-tailwind": true,           // create and paste .css file
    "configure-tailwind.config": true,    // true, "ngin", or false
    "install-postcss": true,              // install PostCSS dependencies
    "configure-postcss": true,            // create postcss.config.js
    "css": "app/routes/styles/tailwind.css",  // CSS file location
    "components": "app/"                  // components folder location
}
```

### Config Options Explained

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `theme` | string | `"blue"` | Default theme color |
| `preset` | string | `"MODERN"` | Default preset style |
| `font` | string | `"Geist"` | Default font family |
| `all-components` | boolean | `false` | Auto-install all components when running `bunx @a5gard/migardr-ui` |
| `install-tailwind` | boolean | `true` | Install Tailwind CSS and related dependencies |
| `configure-tailwind` | boolean | `true` | Create the tailwind.css file at specified location |
| `configure-tailwind.config` | boolean\|"ngin" | `true` | `true` for basic config, `"ngin"` for 18k presets, `false` for none |
| `install-postcss` | boolean | `true` | Install PostCSS dependencies |
| `configure-postcss` | boolean | `true` | Create postcss.config.js file |
| `css` | string | `"app/routes/styles/tailwind.css"` | Path and filename for tailwind.css |
| `components` | string | `"app/"` | Base directory for components folder |

### Auto-Install with Config

Once you have a config file with `"all-components": true`, simply run:

```bash
bunx @a5gard/migardr-ui
```

This will automatically:
1. Install all components to your specified components directory
2. Install required dependencies (if enabled)
3. Configure Tailwind CSS (if enabled)
4. Configure PostCSS (if enabled)
5. Create utils file

No menu selection needed!

### Tailwind Setup

Catalyst UI includes pre-configured Tailwind setups:

**Standard Configuration:**
```bash
bunx @a5gard/migardr-ui
# Select: Configure Tailwind + PostCSS
```

**Ngin Configuration** (18,000 presets):
```bash
bunx @a5gard/migardr-ui
# Select: Configure with Ngin
```

Or set in config:
```jsonc
{
    "configure-tailwind.config": "ngin"
}
```

### Utils File

All installations automatically create a `components/midgardr/utils/utils.ts` file with helper functions:
- `cn()` - Class name merger
- `focusInput` - Focus styles
- `focusRing` - Focus ring utilities
- `formatDate()` - Date formatting


## Requirements

- React 18+
- Tailwind CSS 3+
- Node.js 16+

### Utils File

All installations automatically create a `utils/utils.ts` file with helper functions:
- `cn()` - Class name merger
- `focusInput` - Focus styles
- `focusRing` - Focus ring utilities
- `formatDate()` - Date formatting

## Examples

### Installing a Button Component

```bash
bunx @a5gard/migardr-ui button
```

This will:
1. Create `/components/midgardr/primitives/button.tsx`
2. Install required dependencies (extracted from component imports)
3. Create `utils/utils.ts` if it doesn't exist

### Using the Button Component

```tsx
import { Button } from '~/components/midgardr';

export default function MyPage() {
  return (
    <Button 
      variant="default"
      size="lg"
      onClick={() => console.log('clicked')}
    >
      Click Me
    </Button>
  );
}
```

### Installing Multiple Components

```bash
bunx @a5gard/migardr-ui
# Select: Select Components
# Choose from the list
```

## Component Import Paths

All components use the centralized import path:

```tsx
import { Button, Card, Dialog } from '~/components/midgardr';
```

Or import directly from category folders:

```tsx
import { Button } from '~/components/midgardr/primitives';
import { useTimer } from '~/components/midgardr/hooks';
```

## Features

- **TypeScript First** - Full TypeScript support with type definitions
- **Accessible** - Built with accessibility in mind following WAI-ARIA standards
- **Customizable** - Highly customizable with Tailwind CSS
- **Tree-shakeable** - Import only what you need
- **Dark Mode** - Built-in dark mode support
- **Responsive** - Mobile-first responsive design
- **Zero Config** - Works out of the box with sensible defaults

## Dependencies

Components automatically install their required dependencies. Common dependencies include:
- `@radix-ui/react-*` - Primitive components
- `class-variance-authority` - Variant management
- `clsx` & `tailwind-merge` - Class name utilities
- `lucide-react` - Icons
- `framer-motion` - Animations (where applicable)

## File Structure

After installation, your project will have:

```
your-project/
├── components/
│   └── midgardr/
│       ├── primitives/
│       ├── forms/
│       ├── overlays/
│       ├── hooks/
│       ├── utils/
│       │   └── utils.ts
│       └── index.ts
└── (optional config files)
    ├── tailwind.config.js
    └── postcss.config.js
```

## Support

For issues, questions, or feature requests, please visit our documentation or contact support.

## License

MIT License - See LICENSE file for details


# Smart Prop Autocomplete

Pressing ctrl & spacebar while your cursor is inside the quotations of any props value will bring up an intellisense dropdown with the available prop values that can be assigned.

# Signature Help

# Hover Documentation

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





# Auto Import

To auto import the component right click the components name where ever it may be used within the editor, select `Add Import` in the editor context menu. 

# Go To Definition

Using cmd & ctrl & clicking the components name will bring up the source codes file in a, sheet style dropdown? I don't what what you call this really, any how, it allows you to view the source code file without navigating to it, while at the same time double clicking anywhere inside the "dropdown sheet" will navigate you to the source code file itself.

# Missing Import Warnings

Using the UI libraries inventory data, vscode will warn when not importing the component within any given file and should properly import from the correct location despite any other library installed that uses the same naming convention.

# In Editor Comp Autocomplete

Whenever you start to code a component `<`, pressing ctrl & spacebar will bring up the intellisense dropdown containing every single component currently available in the library, all 2500+.

> [!IMPORTANT]
> As far as you or I using the components library, I beleive the above mentioned features finally completes all the goals I set out in regards to the UI library and delivering the absolute best DX... possible.
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
The library hosts a number of tools for devs to use, the following list is up to date, at the time of writing and will feature more tools as time goes on.

- VSCode Cmd Reference ........ Built-in command library
- Markdown Cheat Sheet ........ Web-based reference
- IRIS: Color Converter ....... Multi-format conversion
- IRIS: Color Wheel ........... Visual color picker
- React/Tailwind Sandbox ...... Development playground
- Theme Builder ............... settings.json & tailwind.css generator
- Typography Tester ........... Font testing suite
- Layout Generator ............ UI layout tools
- X Tester .................... Cross-testing utilities
- Components Reel ............. Component showcase
- Tailwind Converter .......... v3 <-> v4, oklch, hsl, 
- Animation Builder ........... Visual editor
- Responsive Design Helper .... Breakpoint visualizer
- Code Carousel ............... Code display tool
- Sandbox ..................... Live react playground hosting libraries comps
- Icons ....................... Searchable, Rendered icons
- RÚNAR Editor ................ Formally catalyst-editor
- Regex Tester ................ Build and test regex string, cheatsheet included
- JSON Formatter & Validator .. Sanity check for json files
- API Response Mocker ......... Mock REST endpoints with custom JSON responses
- Lorem Ipsum Generator ....... Pick any length and copy to clipboard
- Cron Expression Builder ..... Visual builder for scheduling cron jobs
- UUID Hash Generator ......... Generate random hashes in a flash
- Code Diff Viewer ............ Differences become illuminated
- Flexbox Sandbox ............. Live preview sandbox featuring flexbox 
- Grid Sandbox ................ Live preview sandbox feature grid
- QR Code Generator ........... Images, text, urls 
- Responsive Preview .......... Test layouts across platforms and breakpoints
- Accessibility Checker ....... Scan for WCAG compliance and contrast issues
- Animation Builder ........... Live preview animation builder
- Chart Playground ............ Build charts, outputing react code to paste
- MD Badge Builder ............ Quickly build md badges, that render in real time
- Spinner Generator ........... Build as large of a spinner as you need
- Terminal Menu Generator ..... Best in class, no limitations terminal menu builder
- ENCODER_DECODER_LAB/
  - PNG to Base64
  - JPG to Base64
  - WEBP to Base64
  - PDF to Base64
  - Base64 to PNG
  - Base64 to JPG
  - Base64 to WEBP
  - Base64 to PDF
  - CSV to JSON
  - PNG to SVG
  - JPG to SVG
  - WEBP to SVG
  - MP4 to MP3

# SKALD
### Monaco Editor
If this were anyone elses extension, this would be it's own extension but in this extension it is classified under the tool suite. What first started out as a simple markdown editor, it has since evolved into a full blown monaco editor with 150+ custom features with each feature making it become more and more a full blown ide. 

I have used this so much more than I ever thought I would and because of this it continues to receive regular updates. The largest update to date, is just about to be pushed to the site and will host a list of features so large I cannot remember them all to list but here are some of the features that will be available.
- Feature Set .............. 150-200+ click-to-clipboard MD features
- Special Chars ............ HTML and MD style format character list
- PRE_MADE_ASSETS/
  - File Trees ........... Automated folder visualization
  - Progress Bars ........ Markdown progress indicators
  - ASCII Tables ......... Pre-formatted tables
  - Spinners ............. 17+ different loading spinners
  - Terminal Dashboards .. Terminal-style UI layouts
  - Code Block Previews .. Code styling previews
  - Terminal Menus ....... Visual terminal menu blocks
  - Terminal Logs ........ Logs with hierarchy visualization
  - Git Branch Viz ....... Branch style visualization
  - Status Indicators .... Terminal status boxes
  - Notification Boxes ... Terminal notification styling
  - Output Separators .... Command output dividers
  - Nested Data .......... Nested data structure visualization
  - Activity Timeline .... Sequential activity logs
  - Terminal Dashboards .. Pre-made dashboards
  - Box Drawing .......... Character-based box drawing
  - Various Spinners ..... 17 different spinners
  - Badges and Logos ..... Pre-made badges and icons
  - One night while creating a terminal menu... I kinda went overboard with this section, because of this, part of the sidebar... does need an overhaul, lol, just because the sheer amount of items there are now in this section I need to figure out the best way for users to interact with it, myself included. In the mean time, all of it is available and each "category" of items is nicely categorized the only issue being once clicking on a category it copies the entire category to the clipboard instead of a single item.
- Readme Generator ......... Feature-rich readme builder
- Readme Templates ......... Includes several pre-made templates to start from
- Remote Access ............ Connect remotely to workspace MD files
- Local Settings ........... Locally saved editor settings




# MIÐGARÐR UI

Overview


A comprehensive UI component library with 1808+ components spanning free and premium tiers. Currently features 193 free components alongside extensive development tools.

**Access:** Shortcut available through title pane

**Website:** [Catalyst Software](https://catalyst-software.vercel.app/asgard/midgardr)

##### Features

**Component Library:**
- Search and filter capabilities
- Component viewer with live preview
- React sandbox environment
- One-click library installation with Tailwind configuration
- Option to install components only (without full setup)

##### Built-in Tools

**Development Environment:**
- **Sandbox** - Live React/Tailwind development environment with accessible libraries inventory
  - ![Live Playground 1](https://raw.githubusercontent.com/8an3/midgardr-notes/blob/main/tools/live-playground1.png?raw=true)
  - ![Live Playground 2](https://raw.githubusercontent.com/8an3/midgardr-notes/blob/main/tools/live-playground.png?raw=true)

**Utility Tools:**
- Color Wheel
- MD Reference Sheet
- Icons Library
- VS Code Commands Reference
- Tailwind CSS v3 ↔ v4 Converter
- Tailwind and VS Code Theme Builder
- Code Formatters
- Catalyst Editor
- Encoder/Decoder

**Reusable Project Tools:**
All tools are designed to be integrated into your own projects for extended functionality.


### Insert Component via Editor Context Menu

Access the entire 1808+ component library directly from the editor context menu, inserting components at your cursor position.


**Access:** Right-click → Catalyst UI → Select component

![Context Menu](https://raw.githubusercontent.com/8an3/midgardr-notes/blob/main/ui/context-menu.png?raw=true)


### Insert Component via Quick Pick

Quick pick menu with search capabilities featuring a nested list of all available components for fast insertion at cursor


**Access:** Click UI button on status bar → Select component

![Quick Pick](https://raw.githubusercontent.com/8an3/midgardr-notes/blob/main/ui/quickpick.jpg)


### Installing Catalyst-UI Components

A comprehensive React component library with 100+ production-ready components for building modern web applications.

## Installation

### Quick Start

Install a single component:

```bash
bunx @a5gard/migardr-ui button
```

### Menu

```bash
bunx @a5gard/migardr-ui
```

Then select from the interactive menu:
- **Full Install** - Components + Libraries + Tailwind + PostCSS
- **Full Install with Ngin** - Includes 18,000 Tailwind config presets
- **Components + Libraries** - Install without config files
- **Configure Tailwind + PostCSS** - Setup only
- **Configure Tailwind + PostCSS w/ ngin** - Setup with preset that contains 18,000 configurations set with only 3 variables
- **Select Components** - Choose specific components
- **Create Config** - Creates config file that can be used in conjuction with the bunx command

## Premium Access

Unlock the full component library with a premium access key:


Premium features include:
- Access to all 2000+ components
- Advanced interactive components
- Specialized tools and utilities
- Priority updates

## Component Categories

### Primitives
Core UI components following modern design patterns:
- Button, Input, Select, Checkbox, Radio, Switch
- Dialog, Sheet, Popover, Tooltip
- Card, Badge, Avatar, Separator
- Accordion, Tabs, Collapsible
- And more...

### Forms
Advanced form components with validation:
- Input variants (masked, OTP, password)
- Date pickers and calendars
- File uploads and dropzone
- Toggle groups and button groups

### Data Display
Components for presenting data:
- Tables with sorting and filtering
- Charts and data visualizations
- Timeline and progress indicators
- Empty states and skeletons

### Navigation
Navigation and layout components:
- Menus and navigation bars
- Breadcrumbs and pagination
- Sidebars and dual sidebars
- Command palette

### Feedback
User feedback components:
- Alerts and notifications
- Toast messages
- Loading spinners
- Progress indicators

### Interactive
Advanced interactive elements:
- Drag and drop
- Resizable panels
- Image zoom and crop
- Code editors with syntax highlighting

### Utilities
Helper components and hooks:
- Custom hooks (useTimer, useCopyToClipboard, etc.)
- Auth utilities
- Server middleware
- Context management

## Package Managers

Catalyst UI automatically detects and uses your package manager:
- npm
- pnpm
- yarn

## Configuration

### Config File (Optional)

Create a `catalyst.config.jsonc` file in your project root to customize installation behavior:

```bash
bunx @a5gard/migardr-ui
# Select: Create Config File
```

Or create it manually:

```jsonc
// catalyst.config.jsonc
{
    "theme": "blue",                      // presetting the theme
    "preset": "MODERN",                   // presetting the preset
    "font": "Geist",                      // presetting the font
    "all-components": false,              // auto-install all on `bunx @a5gard/migardr-ui`
    "install-tailwind": true,             // install Tailwind dependencies
    "configure-tailwind": true,           // create and paste .css file
    "configure-tailwind.config": true,    // true, "ngin", or false
    "install-postcss": true,              // install PostCSS dependencies
    "configure-postcss": true,            // create postcss.config.js
    "css": "app/routes/styles/tailwind.css",  // CSS file location
    "components": "app/"                  // components folder location
}
```

### Config Options Explained

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `theme` | string | `"blue"` | Default theme color |
| `preset` | string | `"MODERN"` | Default preset style |
| `font` | string | `"Geist"` | Default font family |
| `all-components` | boolean | `false` | Auto-install all components when running `bunx @a5gard/migardr-ui` |
| `install-tailwind` | boolean | `true` | Install Tailwind CSS and related dependencies |
| `configure-tailwind` | boolean | `true` | Create the tailwind.css file at specified location |
| `configure-tailwind.config` | boolean\|"ngin" | `true` | `true` for basic config, `"ngin"` for 18k presets, `false` for none |
| `install-postcss` | boolean | `true` | Install PostCSS dependencies |
| `configure-postcss` | boolean | `true` | Create postcss.config.js file |
| `css` | string | `"app/routes/styles/tailwind.css"` | Path and filename for tailwind.css |
| `components` | string | `"app/"` | Base directory for components folder |

### Auto-Install with Config

Once you have a config file with `"all-components": true`, simply run:

```bash
bunx @a5gard/migardr-ui
```

This will automatically:
1. Install all components to your specified components directory
2. Install required dependencies (if enabled)
3. Configure Tailwind CSS (if enabled)
4. Configure PostCSS (if enabled)
5. Create utils file

No menu selection needed!

### Tailwind Setup

Catalyst UI includes pre-configured Tailwind setups:

**Standard Configuration:**
```bash
bunx @a5gard/migardr-ui
# Select: Configure Tailwind + PostCSS
```

**Ngin Configuration** (18,000 presets):
```bash
bunx @a5gard/migardr-ui
# Select: Configure with Ngin
```

Or set in config:
```jsonc
{
    "configure-tailwind.config": "ngin"
}
```

### Utils File

All installations automatically create a `components/midgardr/utils/utils.ts` file with helper functions:
- `cn()` - Class name merger
- `focusInput` - Focus styles
- `focusRing` - Focus ring utilities
- `formatDate()` - Date formatting


## Requirements

- React 18+
- Tailwind CSS 3+
- Node.js 16+

### Utils File

All installations automatically create a `utils/utils.ts` file with helper functions:
- `cn()` - Class name merger
- `focusInput` - Focus styles
- `focusRing` - Focus ring utilities
- `formatDate()` - Date formatting

## Examples

### Installing a Button Component

```bash
bunx @a5gard/migardr-ui button
```

This will:
1. Create `/components/midgardr/primitives/button.tsx`
2. Install required dependencies (extracted from component imports)
3. Create `utils/utils.ts` if it doesn't exist

### Using the Button Component

```tsx
import { Button } from '~/components/midgardr';

export default function MyPage() {
  return (
    <Button 
      variant="default"
      size="lg"
      onClick={() => console.log('clicked')}
    >
      Click Me
    </Button>
  );
}
```

### Installing Multiple Components

```bash
bunx @a5gard/migardr-ui
# Select: Select Components
# Choose from the list
```

## Component Import Paths

All components use the centralized import path:

```tsx
import { Button, Card, Dialog } from '~/components/midgardr';
```

Or import directly from category folders:

```tsx
import { Button } from '~/components/midgardr/primitives';
import { useTimer } from '~/components/midgardr/hooks';
```

## Features

- **TypeScript First** - Full TypeScript support with type definitions
- **Accessible** - Built with accessibility in mind following WAI-ARIA standards
- **Customizable** - Highly customizable with Tailwind CSS
- **Tree-shakeable** - Import only what you need
- **Dark Mode** - Built-in dark mode support
- **Responsive** - Mobile-first responsive design
- **Zero Config** - Works out of the box with sensible defaults

## Dependencies

Components automatically install their required dependencies. Common dependencies include:
- `@radix-ui/react-*` - Primitive components
- `class-variance-authority` - Variant management
- `clsx` & `tailwind-merge` - Class name utilities
- `lucide-react` - Icons
- `framer-motion` - Animations (where applicable)

## File Structure

After installation, your project will have:

```
your-project/
├── components/
│   └── midgardr/
│       ├── primitives/
│       ├── forms/
│       ├── overlays/
│       ├── hooks/
│       ├── utils/
│       │   └── utils.ts
│       └── index.ts
└── (optional config files)
    ├── tailwind.config.js
    └── postcss.config.js
```

> [!TIP]
>
> When your looking at code examples and see the import '#midgardr' being used in place of '~/components/midgardr/primitives/button', theres an option with the cli tool to configure your project to use it. 
>
> Every single comopnent in the library can be called with '#midgardr'. The same configuration also allows you to access the icons library via '#baldr' 