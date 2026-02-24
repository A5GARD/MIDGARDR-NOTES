# @a5gard/asgard

The one cli to rule them all.

> [!NOTE]
>
> To keep this libraries size to a minimum, the icons and ui components libraries are kept seperate and this libraries use of them acts as a pass through. If you prefer your more than welcome to use those libraries on their own.

## Installing

```sh
npm install -g @a5gard/asgard
```

## Usage

To display the main menu / help screen

```sh
asgard menu
```

Otherwise you can use the commands that are designed for each feature

> [!IMPORTANT]
> Currently in alpha, if you have never used my projects before so as to not waste time I conduct testing as I code, once an issue crosses my path it gets fixed immediatly. Your more than welcome to use this, but if you come across an issue before I do, this is why

# TOC

- [GitHub](#github)
  - [Installing](#installing)
  - [create-project](#create-project)
  - [delete-project](#delete-project)
  - [load-project](#load-project)
  - [save-project](#save-project)
  - [upload-project](#upload-project)
  - [upload-project+](#upload-project+)
  - [upload-project++](#upload-project++)
  - [upload-project+++](#upload-project+++)
  - [add-source](#add-source)
  - [delete-source](#delete-source)
  - [download-source](#download-source)
  - [set-source](#set-source)
  - [sync-source](#sync-source)
  - [create-timeline](#create-timeline)
  - [combine-timelines](#combine-timelines)
  - [delete-timeline](#delete-timeline)
  - [replace-timeline](#replace-timeline)
  - [switch-timeline](#switch-timeline)
  - [view-timeline](#view-timeline)
  - [restore-version](#restore-version)
  - [delete-version](#delete-version)
  - [view-versions](#view-versions)
  - [download-file](#download-file)
  - [download-folder](#download-folder)
- [BALDR](#baldr)
- [BIFRÖST](#bifrost)
- [BIFRÖST PLUGIN](#bifrost-plugin)
- [MIÐGARÐR](#midgardr)
- [THOR](#thor)

# GitHub 

Simply put, replaces githubs naming convention with names that hold meaning to them, in addition to, each github command sequence has been replace with a single command, ie: In order to create a project, not only is it 5 or 6 commands long but it even takes 2 seperate clis in order to accomplish, meanwhile 'asgard create-project' not only does the same thing but more.

## Overview

This library is for you if one of the following is true:
1. finds github too complicated
2. hates memorizing or having to look up commands whenever you go to use git/github
3. can't remember the exact commands or flags needed to run git commands
4. no longer wants to use git but doesn't want to actually use another platform for whatever reason
5. new to development
6. tired of git/github
7. would like a resource that handles more than just github
8. and the list goes on...

While this resource works with more than just github as I have merged my other libraries in with this one, instead of have 9 resources which is dumb...

This resource is for anyone who has to continue using github but doesn't actually want to use it, or if your new to development. 

If your new to development, I urge you to use this library as it will save you from many headaches and time wasting excercises of dealing with github. It's a great platform and a great idea, they just really missed the mark when it comes to implementation and user experience. This is due to the fact that their naming conventions hold no meaning behind them for new people coming into the industry and the required commands to do anything you need to do... simply put, make no sense unless you either created the platform yourself or were one of the unlucky devs, like me, who had to bash their head against the wall in order to learn the platform.

For experienced devs, simply put, this will not only save you time but also save you from having to continue memorizing everything which will decrease the cognitive load of whenever you have to deal with github, which we use every day.

Either way as you can tell from the toc, the naming convention set forth by github has been replaced with a naming convention that not only makes sense but will actually hold meaning to you whether this is your first day or 10th year.

If this is your 10th year, the following breakdown will provide the conversions on the naming convention:
- project - is your local repo so anything project is referenced its refering to the local representation of your remote repo
- source - refers to remote, as it is the source of your project
- timeline - is your branch, timeline was chosen because whether you are new or not timeline immediatly tells someone that it can be temparay, can be deleted or can become the final project 
- version - replacing tags, this name immediatly conveys a versioning system where as tags... simply does not

To help with chaotic nature that is github and remove the fear of pushing or pulling of any one thing, a system has been put in place to ease and remove these burdens. If your new and have never used github, just skip this part as you do not need to know about this since the fear I'm talking about only plagues people who have used github.

The system that has been put in place is a custom sync sequence that happens before a lot of commands are actually executed, thus removing the pop up prompts like rejected push and other similar prompts telling you that your push or sync has failed. For example, whenever you use upload-project, aka git add *, git commit.. and so on, before running the actual push commands it will first pull/fetch/rebase, merge it with your local, and finally push the local to your repo. This ensures that before any action is taken, whatever branch your currently on, is always up to date so as you will never experience a conflit in refs or heads. If your skeptical about never to experience this again, I don't blame you but to ease this concern in one of my other projects I have an extension that contains a notes and to do app. Simple in nature I know but it uses github as a source of truth, which to be honest I have never seen another dev do before. The notes and to do files are accessible in every single workspace and I can have 4 workspaces open and use the extension in each of them whether or not their are dirty or clean notes in any number of them. This was made 9-10 months ago and not once have I ever had a rejected push. This project will receive the same treatment.

The reason I can ensure this, is because I too will be using this resource and do you think that I... want to deal with this crap day in and day out? No... lol, I do not. But before you ask, yes I'm making this entirely for myself and making public so I can access it everywhere. The only reason for the docs is because... I tend to build larger than normal resources, so large that at times I need to refer to my own documentation in order to remember how to use it, seriously. My vscode extension contains 175+ worth of extensions features and functionality. Currently I have 9 npm libraries, and right before creating this github wrapper I was looking at it and said to myself, "this is stupid, why am I creating so many?" and those libraries will be merged with this one. In addition to that, any other idea or need that comes up will also be added to this library. The only reason why I make the docs so descriptive as I don't need this much information in order to remember how to use it is because even in my last career I always went out of my way to help my colleagues and since I'm already making the documentation I might as well make it right so that anyone else can use it too.

The only libraries I plan on keeping up are the ones that have seen a lot of use considering, I have never told anyone about any of them, otherwise they will be removed once they have been merged



> [!NOTE] 
> Flags are not required and when left out it will prompt for the required information


## create-project

### With no arguments

```sh
asgard new-project
**```
****
If you use the above command a series of prompts will be provided inquiring:
1. project name
2. which package manager you would like to use
3. license you would like to use
4. confirmation to pre install icons library
5. confirmation to pre install components library

Silently it will:
- create the new project folder
- cd into the project folder
- create readme.md
- create license.md
- create package.json
- create .env and .dev.env
- create .gitignore
- initialize github project
- create github repo
- push project to the new repo
- creates asgard.config with the provided values to be used later**

Proving just how much easier life will become when using this resource, as this now perfectly sets you up to dive into whatever project you were planning on creating.

### With arguments

```sh
asgard new-project project-name
```

replacing project-name with whatever you would like to call your project, doing this skips the prompt process with a set of defaults:
- icons: false
- ui components: false
- license: MIT
- branch: main
- package manger: pnpm

This command will follow the same processs as the previous.

### With config

```sh
asgard new-project
```

You may provide your own config with whatever values you would like by first creating the projects folder and then creating the config file 'config.asgard' and running the above command.

### Fallbacks

If you have never used github before or using it for the first time on this station there are a few command that will ensure that you have the required values in order to run everything and if you don't currently have them it will start off by asking you to provide username/owner, email and github token. This will trigger before running the following commands:

- create-project
- download-file
- download-folder
- download-source


## delete-project

New: Removes saved temporary work that you previously set aside. Think of it like deleting a bookmark of your work in progress.

Exp: Removes a stash entry

```sh
asgard delete-project
```

## load-project

New: Brings back work you temporarily set aside. Imagine you put some papers in a drawer to work on something else - this takes those papers back out and puts them on your desk.

Exp: Restores and removes a stash entry (pop operation)

```sh
asgard load-project
```

## save-project

New: Packages up all your current changes, labels them with a note, and sends them to GitHub. It's like saving your video game progress to the cloud.

Exp: Stages all changes, commits with message, and pushes to remote

```sh
asgard save-project
asgard save-project -m "added login page"
```

## upload-project

New: Makes sure your local work matches what's on GitHub, then sends your changes up. Prevents conflicts by always checking first.

Exp: Syncs local with remote then pushes

```sh
asgard upload-project
```

## upload-project+

New: Sends your changes to GitHub and automatically updates your project's version number by one tiny step (like going from 1.0.5 to 1.0.6). Use this for small bug fixes.

Exp: Sync, bump patch version, commit, tag, push with tags

```sh
asgard upload-project+
```

## upload-project++

New: Sends your changes to GitHub and updates your version number for a new feature (like going from 1.2.0 to 1.3.0). Use this when you add something new but don't break existing features.

Exp: Sync, bump minor version, commit, tag, push with tags

```sh
asgard upload-project++
```

## upload-project+++

New: Sends your changes to GitHub and updates your version number for major changes (like going from 2.0.0 to 3.0.0). Use this when you make big changes that might break things for people using your code.

Exp: Sync, bump major version, commit, tag, push with tags

```sh
asgard upload-project+++
```

## delete-source

New: Removes a connection between your local project and a copy stored somewhere online. Like unlinking your phone from a cloud backup.

Exp: Removes a remote reference

```sh
asgard delete-source
asgard delete-source -n 'backup'
```

## download-source

New: Makes a complete copy of someone's project from GitHub onto your computer. Like downloading a complete folder from Google Drive.

Exp: Clones a repository to local machine

```sh
asgard download-source
asgard download-source owner/repo
asgard download-source -u 'https://github.com/owner/repo'
asgard download-source -o 'owner' -r 'repo' -d 'my-folder'
```

## set-source

New: Changes where your project sends and receives updates from. Like changing which cloud storage account your files sync with.

Exp: Updates remote URL

```sh
asgard set-source -u 'https://github.com/newowner/repo.git'
asgard set-source -r 'main' -u 'https://github.com/newowner/repo.git'
```

## sync-source

New: Downloads any new changes from GitHub and uploads your changes. Makes sure everyone is working with the same files.

Exp: Fetch, pull with rebase, auto-commit if needed, push

```sh
asgard sync-source
```

## create-timeline

New: Creates a separate workspace where you can experiment without affecting your main work. Like making a copy of your essay to try different edits.

Exp: Creates and checks out new branch after syncing

```sh
asgard create-timeline
asgard create-timeline -n 'dark-mode-feature'
```

## combine-timelines

New: Takes work from one experimental workspace and merges it into your current workspace. Both workspaces still exist after. Like copying chapters from one document into another.

Exp: Merges another branch into current branch

```sh
asgard combine-timelines
asgard combine-timelines -b 'dark-mode-feature'
```

## delete-timeline

New: Permanently deletes an experimental workspace. Use this when you're done with it or don't need it anymore.

Exp: Deletes a local branch

```sh
asgard delete-timeline
asgard delete-timeline -b 'old-experiment'
```

## replace-timeline

New: Combines an experimental workspace into your main workspace, then deletes the experimental one. Use this when your experiment is successful and you want to make it permanent.

Exp: Merges branch into main and deletes source branch

```sh
asgard replace-timeline
asgard replace-timeline -b 'finished-feature'
```

## switch-timeline

New: Moves you from one workspace to another. Like switching between different tabs in your browser - all your work is still there, you're just looking at a different one.

Exp: Checks out different branch after syncing

```sh
asgard switch-timeline
asgard switch-timeline -b 'dark-mode-feature'
```

## view-timeline

New: Shows you all the different workspaces you have in your project and which one you're currently in.

Exp: Lists all local branches

```sh
asgard view-timeline
```

## restore-version

New: Rewinds your entire project back to how it looked at a specific point in the past. Like using "undo" but for your whole project. WARNING: This erases everything after that point.

Exp: Hard reset to specific commit

```sh
asgard restore-version
asgard restore-version -h 'abc1234'
```

## delete-version

New: Removes a label you previously put on a specific version of your project. The actual version is still in your history, you're just removing the bookmark.

Exp: Deletes a git tag

```sh
asgard delete-version
asgard delete-version -t 'v1.0.0'
```

## view-versions

New: Shows all the labeled versions of your project. These are like bookmarks showing important moments in your project's history.

Exp: Lists all git tags

```sh
asgard view-versions
```

## download-file

New: Downloads just one specific file from someone's GitHub project instead of the whole thing. Like downloading a single photo from someone's album instead of the entire album.

Exp: Downloads single file from repository

```sh
asgard download-file
asgard download-file owner/repo src/index.js
asgard download-file -u 'https://github.com/owner/repo/blob/main/src/index.js'
asgard download-file -o 'owner' -r 'repo' -p 'src/index.js' -b 'main'
```

## download-folder

New: Downloads just one folder from someone's GitHub project instead of everything. Like downloading one folder from Dropbox instead of their entire account.

Exp: Downloads specific folder from repository using sparse checkout or raw HTTP

```sh
asgard download-folder
asgard download-folder owner/repo src/components
asgard download-folder -u 'https://github.com/owner/repo/tree/main/src/components'
asgard download-folder -o 'owner' -r 'repo' -p 'src/components' -b 'main'
asgard download-folder --raw -u 'https://github.com/owner/repo/tree/main/src/components'
```

## view-timeline

New: Shows you all the different workspaces you have in your project and which one you're currently in.
Exp: Lists all local branches

```sh
asgard view-timeline
```

## view-versions

New: Shows all the labeled versions of your project. These are like bookmarks showing important moments in your project's history.
Exp: Lists all git tags

```sh
asgard view-versions
```


## publish-project

New: Takes your existing project folder and creates a GitHub repo for it, then sends everything up. Like taking a project you've been working on locally and finally backing it up to the cloud.

Exp: Creates GitHub repository for existing local project, initializes git if needed, creates missing files (README, CHANGELOG, LICENSE, config.asgard), and pushes everything

```sh
asgard publish-project
```

# BIFRÖST

# BIFRÖST PLUGIN 

# THOR

# MIÐGARÐR

A comprehensive React component library with 2500+ production-ready components for building modern web applications.

## UPDATE

Adding a new line option 'Configure Import Call'. Configures your package.json and tsconfig.json files to allow the use of '#baldr' and '#midgardr' in-place of the traditional '~/components/midgardr' and '@a5gard/baldr'

```javascript
import { Command, CommandGroup, CommandItem, CommandList, cn } from '#midgardr'
import { X } from '#baldr'
```
Selecting the full installation will also configure your project for this use as well.

### Quick Start

Install a single component:

```bash
asgard midgardr button
```

### Menu

```bash
asgard midgardr
```

Then select from the interactive menu:
- **Full Install** - Components + Libraries + Tailwind + PostCSS
- **Full Install with Ngin** - Includes 18,000 Tailwind config presets
- **Components + Libraries** - Install without config files
- **Configure Tailwind + PostCSS** - Setup only
- **Configure Tailwind + PostCSS w/ ngin** - Setup with preset that contains 18,000 configurations set with only 3 variables
- **Select Components** - Choose specific components
- **Create Config** - Creates config file that can be used in conjuction with the bunx command

### Flags

Running the command with flags
- `full-w-ngin` - installs all, includes preset ngin
- `full-install` - full install
- `select-components` - provides a list with toggable items to install
- `comps-and-libs` - just installs the components and required libraries
- `create-config` - create config wizard
- `configure-tailwind-postcss` - installs tailwind v3, postcss and configures each for you
- `configure-ngin` - before installing ngin, prompts you for 3 values, creating the file with them instead of having to manually editing them


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
asgard midgardr
# Select: Create Config File
```

Or create it manually:

```jsonc
{
    "theme": "blue",                      // presetting the theme
    "preset": "MODERN",                   // presetting the preset
    "font": "Geist",                      // presetting the font
    "all-components": false,              // auto-install all on `asgard midgardr`
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
| `all-components` | boolean | `false` | Auto-install all components when running `asgard midgardr` |
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
asgard midgardr
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
asgard midgardr
# Select: Configure Tailwind + PostCSS
```

**Ngin Configuration** (18,000 presets):
```bash
asgard midgardr
# Select: Configure with Ngin
```

Or set in config:
```jsonc
{
    "configure-tailwind.config": "ngin"
}
```

## Examples

### Installing a Button Component

```bash
asgard midgardr button
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
asgard midgardr
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

If you would rather a much easier import path to use, I have recently adopted the following and can be configured in your project using the flag 'easy-paths'

```tsx
import { Button, Card, Dialog } from '#midgardr';
```

## Features

- **TypeScript First** - Full TypeScript support with type definitions
- **Accessible** - Built with accessibility in mind following WAI-ARIA standards
- **Customizable** - Highly customizable with Tailwind CSS
- **Tree-shakeable** - Import only what you need
- **Dark Mode** - Built-in dark mode support
- **Responsive** - Mobile-first responsive design
- **Zero Config** - Works out of the box with sensible defaults


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


# BALDR ICONS

## React Icon Library

This is a programmatically generated React icon library designed for simplicity and accuracy.

### Key Features

*   **No Website Needed:** Icons are visually similar across libraries, so a dedicated showcase website is omitted.
*   **Script-Generated & Verified:** The entire library is built using scripts. Upon completion, it automatically scans the icon directory to generate the list below, guaranteeing that every listed icon is available.
*   **Two Search Methods:**
    1.  **Browser Search:** Use your browser's find function (`Ctrl+F` / `Cmd+F`) to search the list on this page.
    2.  **VS Code Extension:** Use the "DevStack" extension from the marketplace for a quick-pick search. It inserts the icon component and adds the necessary import automatically.

### Naming Convention

Icons are named intuitively, so you don't need to memorize their original names. The structure is:

`[Main Theme][Container/Feature][Filled]`

*   **Main Theme:** The core subject of the icon (e.g., `ExclamationPoint`, `Text`).
*   **Container/Feature:** An encompassing shape or added feature (e.g., `Circle`, `File`, `Wrap`).
*   **Filled:** Appended only if the icon has a filled variant.

**Examples:**
*   `ExclamationPointCircle`
*   `TextWrap`
*   `ExclamationPointFile`
*   `QuestionMarkFileFilled`

## Installation

```bash
npm install @a5gard/baldr
# or
pnpm add @a5gard/baldr
```

## Usage

```javascript
import { ArrowBadgeRight } from '@a5gard/baldr'
 
<ArrowBadgeRight />
```

<!-- icon start -->

## Icons

- Abc
- Ac
- Ace
- Aleph
- Algiz
- Alien
- AlignCenter
- AlignEndVertical
- AlignJustified
- AlignJustify
- AlignLeft
- AlignRight
- Alpha
- Amazon
- AmericanExpress
- Android
- Ansuz
- Anthropic
- AppWindow
- Apple
- Archive
- ArchiveX
- ArrowBadgeDown
- ArrowBadgeLeft
- ArrowBadgeRight
- ArrowBadgeUp
- ArrowBigDown
- ArrowBigLeft
- ArrowBigRight
- ArrowBigUp
- ArrowDown
- ArrowDownFromLine
- ArrowDownLeft
- ArrowDownRight
- ArrowLeft
- ArrowLeftRight
- ArrowRight
- ArrowSwap
- ArrowUp
- ArrowUpDown
- ArrowUpFromLine
- ArrowUpNarrowWide
- ArrowUpRight
- Assemblyai
- Asterisk
- Astro
- At
- AtSign
- Atari
- AudioWaveform
- Award
- Aws
- Azure
- Badge
- BadgeCheck
- Ban
- Banknote
- BarChart
- BarChartArea
- BarChartAreaBig
- BarChartFile
- Baseten
- Bat
- Bed
- BeggarsHand
- Bell
- Berkano
- Beta
- Beth
- Biohazard
- Biome
- Bitcoin
- Bitcoin2
- Blackforestlabs
- Blackforestlabs1
- Blocks
- Bluetooth
- Bmw
- Bold
- Book
- BookOpen
- BookOpenText
- Bookmark
- Bot
- Bower
- Box
- Boxes
- Braces
- BracketsAngle
- Brain
- BrandAstro
- Briefcase
- BrightnessDown
- BrightnessUp
- Browser
- Brush
- Bug
- Building
- Bun
- Burger
- C
- Calc
- CalcDoubled
- Calculator
- Calendar
- CalendarCheck
- CalendarCheck2
- CalendarDays
- CalendarPlus
- Camera
- Capture
- Car
- CarFront
- CaretDown
- CaretLeft
- CaretRight
- CaretUp
- Cb
- Cen
- Cerebras
- Check
- CheckCircle
- CheckSquare
- Checkbox
- CheckboxCheckedFilled
- ChefHat
- ChevronDown
- ChevronLeft
- ChevronRight
- ChevronUp
- ChevronsDown
- ChevronsLeft
- ChevronsLeftRight
- ChevronsRight
- ChevronsUpDown
- Circle
- CircleOff
- CirclePlus
- Circleci
- Cirrus
- Claude
- Clipboard
- ClipboardCheck
- ClipboardData
- ClipboardText
- Clock
- Cloud
- CloudRain
- CloudUpload
- Code
- Codemirror
- Coffeescript
- Cog
- Cohere
- ColorPicker
- ColorSwatch
- ColoredStar
- Columns
- Columns3
- Columns4
- Command
- CommandK
- Compass
- Component
- Component1
- Computer
- ComputerChip
- Construction
- Cookie
- Coolermaster
- Copy
- CornerUpLeft
- CornerUpRight
- Cplusplus
- Cpu
- CreditCard
- Crown
- Css
- Cssmodules
- Cva
- Cweord
- Dagaz
- Dart
- Dashboard
- Database
- Datefns
- Deepgram
- Deepinfra
- Deepmind
- Deepseek
- Delete
- Delta
- DeviceCode
- Digamma
- DirectDebit
- Discord
- Discover
- Docker
- Docusaurus
- Dog
- DollarSign
- Dot
- Dotenv
- Dots
- DotsVertical
- Download
- Droplets
- EPassport
- Ear
- Editorconfig
- Ehwaz
- Electron
- Elevenlabs
- Embla
- Epsilon
- Eraser
- Eslint
- Eta
- Etcd
- ExclamationPointMessageCircle
- ExclamationPointOctagon
- ExclamationPointTriangle
- Expand
- ExternalLink
- Eye
- EyeClosed
- EyeOff
- Facebook
- Fal
- Figma
- File
- FileCode
- FileExport
- FileImage
- FileInput
- FileJson
- FileOutput
- FilePlay
- FilePlus
- FileSpreadsheet
- FileText
- FileTypeBmp
- FileTypeCss
- FileTypeCsv
- FileTypeDoc
- FileTypeDocx
- FileTypeHtml
- FileTypeJpg
- FileTypeJs
- FileTypeJsx
- FileTypePdf
- FileTypePhp
- FileTypePng
- FileTypePpt
- FileTypeRs
- FileTypeSql
- FileTypeSvg
- FileTypeTs
- FileTypeTsx
- FileTypeTxt
- FileTypeVue
- FileTypeXls
- FileTypeXml
- FileTypeZip
- FileTypography
- FileX
- Filter
- Fireworks
- FishBone
- Flag
- Flame
- FloppyDisk
- Focus
- Folder
- FolderCheck
- FolderClosed
- FolderDown
- FolderOpen
- FolderPlus
- FolderRoot
- FolderSearch
- FolderTree
- FolderUp
- FolderUpload
- Foobar2000
- Footprints
- Forward
- FourOhFour
- Frame
- Funnel
- FuseJs
- GalleryVerticalEnd
- Gamepad
- Gamepad2
- Gamma
- Gar
- Gatsby
- Gauge
- Gavel
- Gebo
- Gem
- Gemini
- Gemini1
- Ger
- Ghost
- GhostFilled
- GhostFloating
- GhostFloatingFilled
- Gift
- GitBranch
- GitCommit
- GitCommitVertical
- GitCompare
- GitMerge
- GitPullRequest
- GitPullRequestClose
- Github
- Gitignoredotio
- Gitlab
- Gladia
- Globe
- GlobeLock
- Gnubash
- Go
- Golang
- Google
- Googledataproc
- Googlegemini
- Googlejules
- GraduationCap
- Graphql
- GreekDelta
- Grid
- Grid3X3
- GripVertical
- Grok
- Grunt
- Gulp
- H1
- H2
- H3
- H4
- H5
- H6
- Hackaday
- Haglaz
- Hammer
- Handlebarsdotjs
- HardDrive
- HardHat
- Hash
- Heading
- Headphones
- Heart
- HeartHandshake
- Hexagon
- Highlight
- Home
- Html
- Html5
- Huggingface
- Hume
- ICircle
- Image
- Import
- Inbox
- IndentDecrease
- IndentIncrease
- Ingwaz
- InputOtp
- Instagram
- Ior
- Isaz
- Italic
- Iwaz
- Jack
- Javascript
- Jcb
- Jest
- Json
- Kanban
- Kaph
- Kappa
- Key
- Keyboard
- King
- Klarna
- Koppa
- Kotlin
- Lambda
- Laptop
- Laukaz
- Layers
- LayoutGrid
- Less
- LetterCaseLower
- LetterCaseToggle
- LetterCaseUpper
- Lexical
- Library
- LifeBuoy
- Lightbulb
- LineDashed
- LineHeight
- Link
- Linkedin
- List
- ListCheck
- ListChecks
- ListFilter
- ListFilterPlus
- ListMusic
- ListOrdered
- ListRestart
- Lmnt
- Loader
- LoaderCircle
- Lock
- LockOpen
- LogIn
- LogOut
- Loki
- Lota
- Lucide
- Luma
- Maestro
- Mail
- MailCheck
- Mannaz
- Map
- MapPin
- Markdown
- Marko
- MasterCard
- Maximize
- Mdx
- Megaphone
- Mem
- Menu
- MessageCircle
- MessagePlus
- MessageSquare
- MessagesSquare
- Messenger
- Mic
- MicrochipBoard
- Microphone
- Microsoft
- Microsoft1
- Minimize
- Mintlify
- Minus
- Mistralai
- Mocha
- MonacoEditor
- Monitor
- MoodBoy
- Moon
- MousePointer
- Move
- Mu
- Music
- Mysql
- Naudiz
- Navigation
- Newspaper
- Nextdotjs
- Nextjs
- Nodejs
- NotebookText
- NotepadText
- Npm
- Nu
- Number20Small
- Nun
- Odin
- Odin2
- Ollama
- Omicron
- OpenSource
- Openai
- Os
- Othalan
- Package
- Pacman
- Paintbrush
- Palette
- PanelLeft
- PanelLeftClose
- PanelLeftOpen
- PanelRight
- Paperclip
- Pause
- Paypal
- Pdf
- Pe
- Pen
- PenTool
- Pencil
- PencilCheck
- Percent
- Perl
- Perplexity
- Pertho
- Phone
- Photo
- PhotoCircle
- Php
- Pi
- PictureInPicture
- PieChart
- PiggyBank
- Pin
- Pipecat
- Pixel2Accommodate
- Pixel2Add1
- Pixel2Adjust2
- Pixel2Alarm
- Pixel2Alert
- Pixel2Anchor2
- Pixel2Arrest
- Pixel2Ascend
- Pixel2Ask
- Pixel2Attract
- Pixel2Bake
- Pixel2Barbecue
- Pixel2Believe
- Pixel2Bite
- Pixel2Blaze
- Pixel2Bloom
- Pixel2Blow
- Pixel2Bookmark2
- Pixel2Broadcast
- Pixel2Build1
- Pixel2Caffeinate
- Pixel2Calculate1
- Pixel2Call1
- Pixel2Camp
- Pixel2Capture
- Pixel2Celebrate
- Pixel2Charge
- Pixel2Chop
- Pixel2Clamber
- Pixel2Climb
- Pixel2Close1
- Pixel2Code2
- Pixel2Collect
- Pixel2Condemn
- Pixel2Connect
- Pixel2Cook
- Pixel2Copy1
- Pixel2Create1
- Pixel2Crop2
- Pixel2Cry
- Pixel2Cut1
- Pixel2Dazzle
- Pixel2Decorate
- Pixel2Defend
- Pixel2Develop
- Pixel2Die
- Pixel2Dig
- Pixel2Divide
- Pixel2Download1
- Pixel2Dream
- Pixel2Drill
- Pixel2Drink
- Pixel2Drive
- Pixel2Drown
- Pixel2Eat
- Pixel2Enlarge
- Pixel2Enter
- Pixel2Equal
- Pixel2Explode
- Pixel2Explore1
- Pixel2Fight
- Pixel2Film1
- Pixel2Find
- Pixel2Finish
- Pixel2Fit
- Pixel2Flag2
- Pixel2Forbid
- Pixel2Forward2
- Pixel2Gamble
- Pixel2Game
- Pixel2Give
- Pixel2Go
- Pixel2Groom
- Pixel2Grow
- Pixel2Hack
- Pixel2Hammer
- Pixel2Hang
- Pixel2Harvest
- Pixel2Home2
- Pixel2Hurt
- Pixel2Impregnate
- Pixel2Join
- Pixel2Keep
- Pixel2Kill
- Pixel2Kiss
- Pixel2Label1
- Pixel2Launch1
- Pixel2Lift
- Pixel2Link2
- Pixel2Listen
- Pixel2Load
- Pixel2Locate
- Pixel2Lock1
- Pixel2Love
- Pixel2Marry
- Pixel2Merge
- Pixel2Narrow
- Pixel2Navigate
- Pixel2Open
- Pixel2Pause2
- Pixel2Pay
- Pixel2Perform
- Pixel2Photograph
- Pixel2Pin
- Pixel2Ping
- Pixel2Plug1
- Pixel2Point
- Pixel2Power1
- Pixel2Prank
- Pixel2Press
- Pixel2Primp
- Pixel2Print1
- Pixel2Produce
- Pixel2Protect
- Pixel2Push
- Pixel2Race
- Pixel2Rain
- Pixel2Record
- Pixel2Redo1
- Pixel2Reflect
- Pixel2Reply2
- Pixel2Report1
- Pixel2Resize
- Pixel2Rewind
- Pixel2Rule1
- Pixel2Save2
- Pixel2Saw
- Pixel2Scare
- Pixel2Schedule
- Pixel2Search2
- Pixel2Send2
- Pixel2Shine
- Pixel2Sit
- Pixel2Sleep
- Pixel2Smell
- Pixel2Smoke
- Pixel2Solve
- Pixel2Sound
- Pixel2Spin
- Pixel2Spook
- Pixel2Stack
- Pixel2Stamp
- Pixel2Steam1
- Pixel2Stop2
- Pixel2Store
- Pixel2Strike
- Pixel2Subtract
- Pixel2Swim
- Pixel2Tag2
- Pixel2Target
- Pixel2Time
- Pixel2Tower
- Pixel2Travel
- Pixel2Type
- Pixel2Undo2
- Pixel2Unlock1
- Pixel2Upload1
- Pixel2Urbanize
- Pixel2Use
- Pixel2Wait
- Pixel2Watch1
- Pixel2Wear
- Pixel2Weld
- Pixel2Win
- Pixel2Wonder
- Pixel2Write
- PixelAd
- PixelAdSolid
- PixelAlignCenter
- PixelAlignCenterSolid
- PixelAlignJustify
- PixelAlignJustifySolid
- PixelAlignLeft
- PixelAlignLeftSolid
- PixelAlignRight
- PixelAlignRightSolid
- PixelAnalytics
- PixelAnalyticsSolid
- PixelAndroid
- PixelAngellist
- PixelAngleDown
- PixelAngleDownSolid
- PixelAngleLeft
- PixelAngleLeftSolid
- PixelAngleRight
- PixelAngleRightSolid
- PixelAngleUp
- PixelAngleUpSolid
- PixelApple
- PixelArrowAltCircleDown
- PixelArrowAltCircleDownSolid
- PixelArrowAltCircleLeft
- PixelArrowAltCircleLeftSolid
- PixelArrowAltCircleRight
- PixelArrowAltCircleRightSolid
- PixelArrowAltCircleUp
- PixelArrowAltCircleUpSolid
- PixelArrowCircleDown
- PixelArrowCircleDownSolid
- PixelArrowCircleLeft
- PixelArrowCircleLeftSolid
- PixelArrowCircleRight
- PixelArrowCircleRightSolid
- PixelArrowCircleUp
- PixelArrowCircleUpSolid
- PixelArrowDown
- PixelArrowDownSolid
- PixelArrowLeft
- PixelArrowLeftSolid
- PixelArrowRight
- PixelArrowRightSolid
- PixelArrowUp
- PixelArrowUpSolid
- PixelArweave
- PixelAt
- PixelAtSolid
- PixelBadgeCheck
- PixelBadgeCheckSolid
- PixelBank
- PixelBankSolid
- PixelBars
- PixelBarsSolid
- PixelBehance
- PixelBell
- PixelBellExclaimation
- PixelBellExclaimationSolid
- PixelBellMute
- PixelBellMuteSolid
- PixelBellSolid
- PixelBloomberg
- PixelBluesky
- PixelBold
- PixelBoldSolid
- PixelBolt
- PixelBoltSolid
- PixelBookHeart
- PixelBookHeartSolid
- PixelBookmark
- PixelBookmarkSolid
- PixelBoxUsd
- PixelBoxUsdSolid
- PixelBrightnessHigh
- PixelBrightnessHighSolid
- PixelBrightnessLow
- PixelBrightnessLowSolid
- PixelBulletList
- PixelBulletListSolid
- PixelBullhorn
- PixelBullhornSolid
- PixelBusiness
- PixelCalender
- PixelCalenderSolid
- PixelCc
- PixelCcSolid
- PixelChartLine
- PixelChartLineSolid
- PixelChartNetwork
- PixelChartNetworkSolid
- PixelCheck
- PixelCheckBox
- PixelCheckBoxSolid
- PixelCheckCircle
- PixelCheckCircleSolid
- PixelCheckList
- PixelCheckListSolid
- PixelCheckSolid
- PixelChevronDown
- PixelChevronDownSolid
- PixelChevronUp
- PixelChevronUpSolid
- PixelCircleNotch
- PixelCircleNotchSolid
- PixelClipboard
- PixelClipboardSolid
- PixelClock
- PixelClockSolid
- PixelCloud
- PixelCloudDownloadAlt
- PixelCloudDownloadSolid
- PixelCloudUpload
- PixelCloudUploadSolid
- PixelCode
- PixelCodeBlock
- PixelCodeBlockSolid
- PixelCodeSolid
- PixelCog
- PixelCogSolid
- PixelComment
- PixelCommentDots
- PixelCommentDotsSolid
- PixelCommentQuote
- PixelCommentQuoteSolid
- PixelCommentSolid
- PixelComments
- PixelCommentsSolid
- PixelCopy
- PixelCopySolid
- PixelCreditCard
- PixelCreditCardSolid
- PixelCrown
- PixelCrownSolid
- PixelCrunchbase
- PixelCybersecurity
- PixelDataScience
- PixelDigg
- PixelDiscord
- PixelDiscourse
- PixelDivider
- PixelDividerSolid
- PixelDownload
- PixelDownloadAlt
- PixelDownloadAltSolid
- PixelDownloadSolid
- PixelEdit
- PixelEditSolid
- PixelEllipsesHorizontal
- PixelEllipsesHorizontalCircle
- PixelEllipsesHorizontalCircleSolid
- PixelEllipsesHorizontalSolid
- PixelEllipsesVertical
- PixelEllipsesVerticalCircle
- PixelEllipsesVerticalCircleSolid
- PixelEllipsesVerticalSolid
- PixelEnvelope
- PixelEnvelopeSolid
- PixelExclaimation
- PixelExclaimationSolid
- PixelExclamationTriangle
- PixelExclamationTriangleSolid
- PixelExpand
- PixelExpandSolid
- PixelExternalLink
- PixelExternalLinkSolid
- PixelEye
- PixelEyeCross
- PixelEyeCrossSolid
- PixelEyeSolid
- PixelFaceThinking
- PixelFaceThinkingSolid
- PixelFacebookRound
- PixelFacebookSquare
- PixelFigma
- PixelFileImport
- PixelFileImportSolid
- PixelFilter
- PixelFilterAltCircle
- PixelFilterAltCircleSolid
- PixelFilterSolid
- PixelFinance
- PixelFire
- PixelFireSolid
- PixelFlag
- PixelFlagCheckered
- PixelFlagCheckeredSolid
- PixelFlagSolid
- PixelFolder
- PixelFolderOpen
- PixelFolderOpenSolid
- PixelFolderSolid
- PixelFuturism
- PixelGaming
- PixelGiphy
- PixelGithub
- PixelGlobe
- PixelGlobeAmericas
- PixelGlobeAmericasSolid
- PixelGlobeSolid
- PixelGolden
- PixelGoogle
- PixelGoogleNews
- PixelGrid
- PixelGridSolid
- PixelH1
- PixelH2
- PixelH3
- PixelHackernoon
- PixelHackernoonPurcat
- PixelHeading1Solid
- PixelHeading2Solid
- PixelHeading3Solid
- PixelHeadphones
- PixelHeadphonesSolid
- PixelHeart
- PixelHeartSolid
- PixelHighlight
- PixelHighlightSolid
- PixelHockeyMask
- PixelHockeyMaskSolid
- PixelHome
- PixelHomeSolid
- PixelHuggingface
- PixelImage
- PixelImageSolid
- PixelImgur
- PixelIndent
- PixelIndentSolid
- PixelInfoCircle
- PixelInfoCircleSolid
- PixelInstagram
- PixelIos
- PixelItalics
- PixelItalicsSolid
- PixelKaggle
- PixelLifeHacking
- PixelLightbulb
- PixelLightbulbSolid
- PixelLineHeight
- PixelLineHeightSolid
- PixelLink
- PixelLinkSolid
- PixelLinkedin
- PixelLocationPin
- PixelLocationPinSolid
- PixelLock
- PixelLockAlt
- PixelLockAltSolid
- PixelLockOpen
- PixelLockOpenSolid
- PixelLockSolid
- PixelLogin
- PixelLoginSolid
- PixelLogout
- PixelLogoutSolid
- PixelMachineLearning
- PixelManagement
- PixelMastodon
- PixelMedia
- PixelMessage
- PixelMessageDots
- PixelMessageDotsSolid
- PixelMessageSolid
- PixelMinds
- PixelMinus
- PixelMinusSolid
- PixelMoon
- PixelMoonSolid
- PixelMusic
- PixelMusicSolid
- PixelNewsbreak
- PixelNewspaper
- PixelNewspaperSolid
- PixelNpm
- PixelNumberedList
- PixelNumberedListSolid
- PixelOctagonCheck
- PixelOctagonCheckSolid
- PixelOctagonTimes
- PixelOctagonTimesSolid
- PixelOpenAi
- PixelOutdent
- PixelOutdentSolid
- PixelPageBreak
- PixelPageBreakSolid
- PixelPaperclip
- PixelPaperclipSolid
- PixelParagraph
- PixelParagraphSolid
- PixelPause
- PixelPauseSolid
- PixelPen
- PixelPenNib
- PixelPenNibSolid
- PixelPenSolid
- PixelPencil
- PixelPencilRuler
- PixelPencilRulerSolid
- PixelPencilSolid
- PixelPeopleCarry
- PixelPeopleCarrySolid
- PixelPhoneRingingHigh
- PixelPhoneRingingHighSolid
- PixelPhoneRingingLow
- PixelPhoneRingingLowSolid
- PixelPinterest
- PixelPlane
- PixelPlaneDeparture
- PixelPlaneDepartureSolid
- PixelPlaneSolid
- PixelPlay
- PixelPlaySolid
- PixelPlaylist
- PixelPlaylistSolid
- PixelPlus
- PixelPlusSolid
- PixelPodcasts
- PixelPrint
- PixelPrintSolid
- PixelPro
- PixelProSolid
- PixelProductHunt
- PixelProductManagement
- PixelProgramming
- PixelQuestion
- PixelQuestionSolid
- PixelQuoteLeft
- PixelQuoteLeftSolid
- PixelQuoteRight
- PixelQuoteRightSolid
- PixelReceipt
- PixelReceiptSolid
- PixelReddit
- PixelRefresh
- PixelRefreshSolid
- PixelRemote
- PixelRetroCamera
- PixelRetroCameraSolid
- PixelRobot
- PixelRobotSolid
- PixelRss
- PixelSave
- PixelSaveSolid
- PixelScience
- PixelSearch
- PixelSearchSolid
- PixelSeedlings
- PixelSeedlingsSolid
- PixelShare
- PixelShareSolid
- PixelShop
- PixelShopSolid
- PixelShoppingCart
- PixelShoppingCartSolid
- PixelShuffle
- PixelShuffleSolid
- PixelSia
- PixelSociety
- PixelSort
- PixelSortSolid
- PixelSoundMute
- PixelSoundMuteSolid
- PixelSoundOn
- PixelSoundOnSolid
- PixelSparkles
- PixelSparklesSolid
- PixelSpinner
- PixelSpinnerSolid
- PixelSpinnerThird
- PixelSpinnerThirdSolid
- PixelStar
- PixelStarCrescent
- PixelStarCrescentSolid
- PixelStarSolid
- PixelStartups
- PixelSteam
- PixelStrikeThrough
- PixelStrikeThroughSolid
- PixelSun
- PixelSunSolid
- PixelTable
- PixelTableSolid
- PixelTag
- PixelTagSolid
- PixelTechCompanies
- PixelTechStories
- PixelTechnology
- PixelTextSlash
- PixelTextSlashSolid
- PixelThemes
- PixelThemesSolid
- PixelThreads
- PixelThumbsdown
- PixelThumbsdownSolid
- PixelThumbsup
- PixelThumbsupSolid
- PixelThumbtack
- PixelThumbtackSolid
- PixelTiktok
- PixelTimes
- PixelTimesCircle
- PixelTimesCircleSolid
- PixelTimesSolid
- PixelTranslate
- PixelTranslateSolid
- PixelTrash
- PixelTrashAlt
- PixelTrashAltSolid
- PixelTrashSolid
- PixelTrending
- PixelTrendingSolid
- PixelTrophy
- PixelTrophySolid
- PixelTwitch
- PixelTwitter
- PixelUnderline
- PixelUnderlineSolid
- PixelUnlock
- PixelUnlockAlt
- PixelUnlockAltSolid
- PixelUnlockSolid
- PixelUnsplash
- PixelUpload
- PixelUploadAlt
- PixelUploadAltSolid
- PixelUploadSolid
- PixelUser
- PixelUserCheck
- PixelUserCheckSolid
- PixelUserHeadset
- PixelUserHeadsetSolid
- PixelUserSolid
- PixelUsers
- PixelUsersCrown
- PixelUsersCrownSolid
- PixelUsersSolid
- PixelViewblocks
- PixelVoteYeah
- PixelVoteYeahSolid
- PixelWallet
- PixelWalletSolid
- PixelWeb3
- PixelWikipedia
- PixelWindowClose
- PixelWindowCloseSolid
- PixelWriting
- PixelX
- PixelYoutube
- Plane
- Platformio
- Play
- PlayerSkipForward
- PlayerTrackNext
- PlayerTrackPrev
- Playstation
- Plus
- Pnpm
- Pointer
- Popcorn
- Porsche
- Postcss
- Power
- Powershell
- Prescription
- Prettier
- Printer
- Prisma
- Pug
- PuzzlePiece
- Python
- Qoph
- QrCode
- Queen
- QuestionMarkCircle
- QuestionMarkMessageCircle
- Quote
- R
- Radar
- Radio
- Radixui
- Raido
- RatingStar
- Razer
- React
- ReactArea
- ReactAria
- ReactDayPicker
- Readme
- Reason
- Redis
- Redo
- RefreshCcw
- RefreshCw
- Remark
- Remix
- Repeat
- Replicate
- Reply
- ReplyAll
- Res
- Revai
- Rho
- Rive
- RobotFace
- Rocket
- Rollupdotjs
- RotateCcw
- RotateCw
- Ruby
- Ruler
- Rust
- Sade
- Samekh
- San
- Sanity
- Sass
- Save
- Scala
- Scale
- Scan
- ScanLine
- Scissors
- Search
- SearchX
- Selector
- Send
- Sentry
- Server
- Settings
- Shadcnui
- Share
- Sharp
- Shield
- Ship
- ShoppingBag
- ShoppingCart
- Sidebar
- SidebarRight
- Sigel
- Sigma
- SkipBack
- SkipForward
- Skype
- Slack
- SlidersHorizontal
- Smartphone
- Smile
- SmilePlus
- Solo
- Sony
- SortAscending
- SortDescending
- Sparkles
- Split
- Spotify
- Square
- SquareSplitHorizontal
- SquareTerminal
- Stan
- Star
- StarOff
- Steam
- Stopwatch
- Store
- Storybook
- Strikethrough
- Stripe
- Stylelint
- Sublimetext
- Subscript
- Subtitles
- Sun
- Superscript
- Svelte
- Svg
- Swift
- Switch
- Table
- TableColumn
- TableRow
- Tabler
- Tablet
- Tag
- Tailwindcss
- Tally1
- Tally2
- Tally3
- Tally4
- Tally5
- Target
- Tau
- Terminal
- Terminal2
- Testinglibrary
- TextCursorInput
- TextDecrease
- TextIncrease
- TextSize
- TextWrap
- TextWrapColumn
- TextWrapDisabled
- Theodinproject
- Theta
- ThumbsDown
- ThumbsUp
- Ticket
- Tilde
- Timer
- Tiwaz
- TogetherAi
- Toml
- Trash
- Trash2
- TrendingDown
- TrendingUp
- Trophy
- Truck
- Tsnode
- Tv
- Twitch
- Twitter
- Type
- Typescript
- Underline
- Undo
- Upload
- Upsilon
- Uruz
- User
- UserCheck
- UserCircle
- UserDown
- UserHeart
- UserMinus
- UserPlus
- UserSettings
- UserSquareRounded
- UserStar
- Users
- UsersGroup
- Utensils
- UtensilsCrossed
- Vercel
- Vertex
- Video
- VideoOff
- View360
- Visa
- VisaElectron
- Vite
- Volume
- Volume2
- VolumeDown
- VolumeOff
- VolumeUp
- VolumeX
- Vue
- Vuedotjs
- Vulknut
- Walk
- Wallet
- Wallpaper
- Wand
- Waveform
- Waves
- Webassembly
- WesternUnion
- Wifi
- Wireshark
- World
- Wrench
- Wunjo
- X
- XAi
- XCircle
- Yaml
- Yarn
- Yodh
- Youtube
- Yr
- Zap
- Zeta
- ZoomIn
- ZoomOut

<!-- icon end -->

## Basic Usage

### Import specific icons

```tsx
import { Home, User } from '@a5gard/baldr';

function App() {
  return (
    <div>
      <Home className="text-primary" size={24} />
      <User className="text-gray-500" size={32} strokeWidth={1.5} />
    </div>
  );
}
```

### Dynamic icon rendering

```tsx
import { Icon, icons } from '@a5gard/baldr';

function DynamicIcon({ iconName }: { iconName: string }) {
  return <Icon name={iconName} icons={icons} className="text-blue-500" />;
}
```

## Props

All icons accept the following props:

- `size`: number | string (default: 24) - Size of the icon
- `color`: string (default: 'currentColor') - Stroke color
- `strokeWidth`: number | string (default: 2) - Width of the stroke
- `className`: string - CSS classes (works with Tailwind!)
- All standard SVG attributes

## Tailwind CSS Integration

Works seamlessly with Tailwind:

```tsx
<Home className="w-6 h-6 text-blue-500 hover:text-blue-700" />
<User className="text-primary dark:text-primary-dark" size={20} />
```































