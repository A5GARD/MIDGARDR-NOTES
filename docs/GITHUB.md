# GitHub 


- [Github Wrapper](#github-wrapper)
- [Repo Management](#repo-management)
- [Open Repo in Browser](#open-repo-in-browser)
- [Open Repo at File](#open-repo-at-file)

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Github Wrapper**

This npm library already does far more than just a simple github wrapper as I no longer care for have 8+ npm libraries and would rather shrink them down to one, with saying that I already know I'm going to have atleast three, icons, ui components and lastly this new one. This library will work cohesively with the icons and components library, but will also be a platform installer, platform plugin system, and much more. As far as the github wrapper goes, I did make it with devstack in mind so it will work quite easily and nicely with it. The terminal menu styling, I need to work on as I found after working on it 13 hours straight there really isn't a library that does them reasonably. Who knows maybe I missed the one that does, but that does need working on so whenever you go to use it don't mind that. But I'll place the relevant docs from the library here for you to review.


### Installing

```sh
npm install @a5gard/asgard
```

### Usage

To display the main menu / help screen

```sh
asgard menu
```

Otherwise you can use the commands that are designed for each feature

> [!IMPORTANT]
> Currently in alpha, if you have never used my projects before so as to not waste time I conduct testing as I code, once an issue crosses my path it gets fixed immediatly. Your more than welcome to use this, but if you come across an issue before I do, this is why

### TOC

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

### GitHub 

### Overview

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


### create-project

### With no arguments

```sh
asgard new-project
```

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
- creates asgard.config with the provided values to be used later

Proving just how much easier life will become when using this resource, as this now perfectly sets you up to dive into whatever project you were planning on creating.

### With arguments

```sh
asgard new-project project-name
```

Obviously you may replace project-name with whatever you would like to call your project, doing this skips the prompt process with a set of defaults:
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


### delete-project

New: Removes saved temporary work that you previously set aside. Think of it like deleting a bookmark of your work in progress.

Exp: Removes a stash entry

```sh
asgard delete-project
```

### load-project

New: Brings back work you temporarily set aside. Imagine you put some papers in a drawer to work on something else - this takes those papers back out and puts them on your desk.

Exp: Restores and removes a stash entry (pop operation)

```sh
asgard load-project
```

### save-project

New: Packages up all your current changes, labels them with a note, and sends them to GitHub. It's like saving your video game progress to the cloud.

Exp: Stages all changes, commits with message, and pushes to remote

```sh
asgard save-project
asgard save-project -m "added login page"
```

### upload-project

New: Makes sure your local work matches what's on GitHub, then sends your changes up. Prevents conflicts by always checking first.

Exp: Syncs local with remote then pushes

```sh
asgard upload-project
```

### upload-project+

New: Sends your changes to GitHub and automatically updates your project's version number by one tiny step (like going from 1.0.5 to 1.0.6). Use this for small bug fixes.

Exp: Sync, bump patch version, commit, tag, push with tags

```sh
asgard upload-project+
```

### upload-project++

New: Sends your changes to GitHub and updates your version number for a new feature (like going from 1.2.0 to 1.3.0). Use this when you add something new but don't break existing features.

Exp: Sync, bump minor version, commit, tag, push with tags

```sh
asgard upload-project++
```

### upload-project+++

New: Sends your changes to GitHub and updates your version number for major changes (like going from 2.0.0 to 3.0.0). Use this when you make big changes that might break things for people using your code.

Exp: Sync, bump major version, commit, tag, push with tags

```sh
asgard upload-project+++
```

### delete-source

New: Removes a connection between your local project and a copy stored somewhere online. Like unlinking your phone from a cloud backup.

Exp: Removes a remote reference

```sh
asgard delete-source
asgard delete-source -n 'backup'
```

### download-source

New: Makes a complete copy of someone's project from GitHub onto your computer. Like downloading a complete folder from Google Drive.

Exp: Clones a repository to local machine

```sh
asgard download-source
asgard download-source owner/repo
asgard download-source -u 'https://github.com/owner/repo'
asgard download-source -o 'owner' -r 'repo' -d 'my-folder'
```

### set-source

New: Changes where your project sends and receives updates from. Like changing which cloud storage account your files sync with.

Exp: Updates remote URL

```sh
asgard set-source -u 'https://github.com/newowner/repo.git'
asgard set-source -r 'main' -u 'https://github.com/newowner/repo.git'
```

### sync-source

New: Downloads any new changes from GitHub and uploads your changes. Makes sure everyone is working with the same files.

Exp: Fetch, pull with rebase, auto-commit if needed, push

```sh
asgard sync-source
```

### create-timeline

New: Creates a separate workspace where you can experiment without affecting your main work. Like making a copy of your essay to try different edits.

Exp: Creates and checks out new branch after syncing

```sh
asgard create-timeline
asgard create-timeline -n 'dark-mode-feature'
```

### combine-timelines

New: Takes work from one experimental workspace and merges it into your current workspace. Both workspaces still exist after. Like copying chapters from one document into another.

Exp: Merges another branch into current branch

```sh
asgard combine-timelines
asgard combine-timelines -b 'dark-mode-feature'
```

### delete-timeline

New: Permanently deletes an experimental workspace. Use this when you're done with it or don't need it anymore.

Exp: Deletes a local branch

```sh
asgard delete-timeline
asgard delete-timeline -b 'old-experiment'
```

### replace-timeline

New: Combines an experimental workspace into your main workspace, then deletes the experimental one. Use this when your experiment is successful and you want to make it permanent.

Exp: Merges branch into main and deletes source branch

```sh
asgard replace-timeline
asgard replace-timeline -b 'finished-feature'
```

### switch-timeline

New: Moves you from one workspace to another. Like switching between different tabs in your browser - all your work is still there, you're just looking at a different one.

Exp: Checks out different branch after syncing

```sh
asgard switch-timeline
asgard switch-timeline -b 'dark-mode-feature'
```

### view-timeline

New: Shows you all the different workspaces you have in your project and which one you're currently in.

Exp: Lists all local branches

```sh
asgard view-timeline
```

### restore-version

New: Rewinds your entire project back to how it looked at a specific point in the past. Like using "undo" but for your whole project. WARNING: This erases everything after that point.

Exp: Hard reset to specific commit

```sh
asgard restore-version
asgard restore-version -h 'abc1234'
```

#### view-versions

New: Shows all the labeled versions of your project. These are like bookmarks showing important moments in your project's history.

Exp: Lists all git tags

```sh
asgard view-versions
```

### download-file

New: Downloads just one specific file from someone's GitHub project instead of the whole thing. Like downloading a single photo from someone's album instead of the entire album.

Exp: Downloads single file from repository

```sh
asgard download-file
asgard download-file owner/repo src/index.js
asgard download-file -u 'https://github.com/owner/repo/blob/main/src/index.js'
asgard download-file -o 'owner' -r 'repo' -p 'src/index.js' -b 'main'
```

### download-folder

New: Downloads just one folder from someone's GitHub project instead of everything. Like downloading one folder from Dropbox instead of their entire account.

Exp: Downloads specific folder from repository using sparse checkout or raw HTTP

```sh
asgard download-folder
asgard download-folder owner/repo src/components
asgard download-folder -u 'https://github.com/owner/repo/tree/main/src/components'
asgard download-folder -o 'owner' -r 'repo' -p 'src/components' -b 'main'
asgard download-folder --raw -u 'https://github.com/owner/repo/tree/main/src/components'
```

### view-timeline

New: Shows you all the different workspaces you have in your project and which one you're currently in.
Exp: Lists all local branches

```sh
asgard view-timeline
```

### view-versions

New: Shows all the labeled versions of your project. These are like bookmarks showing important moments in your project's history.
Exp: Lists all git tags

```sh
asgard view-versions
```


### publish-project

New: Takes your existing project folder and creates a GitHub repo for it, then sends everything up. Like taking a project you've been working on locally and finally backing it up to the cloud.

Exp: Creates GitHub repository for existing local project, initializes git if needed, creates missing files (README, CHANGELOG, LICENSE, config.asgard), and pushes everything

```sh
asgard publish-project
```


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Repo Management**

Comprehensive GitHub repository management and functionality accessible from multiple locations

**Access Options:**
- Status bar → DevStack Quick Pick
- Right-click editor → GitHub → Select option

**Features:**
- Complete repository management
- Git operations integration
- Direct browser access
- File-specific navigation

See DevStack Quick Pick documentation for full feature outline.

![GitHub Functions](https://raw.githubusercontent.com/8an3/midgardr-notes/main/github/github-pic.jpg?raw=true)
![GitHub Context Menu](https://raw.githubusercontent.com/8an3/midgardr-notes/main/github/contextr.jpg?raw=true)

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Open Repo in Browser**

Open your GitHub repository in browser directly from any file in your workspace

**Access:** Right-click → Open GitHub Repo

**Features:**
- Instant browser access
- Works from any file
- Automatic repository detection
- No manual URL entry needed

[Video Demo](https://youtu.be/CQ2rYtbZKJk)


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Open Repo at File**

Navigate directly to a specific file's location in your GitHub repository

**Access:** Right-click → Open GitHub at File

**Features:**
- Direct file navigation
- Opens exact file location in GitHub
- Preserves directory structure
- Line number support

[Video Demo](https://youtu.be/0CLkYvWSVqI)


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Pro7 Archiver**

Create password-encrypted archives containing sensitive files for safe inclusion in your GitHub repository

**Access Options:**
- DevStack Quick Pick menu
- Automatically runs in `G4 & .vsix` workflow
- Custom command sequences (concurrent/sequential objects)

**How It Works:**

1. **Configuration Scan:**
   - Scans workspace root for `.pro7` config file
   - If found: collects files specified in `.pro7` (similar to `.gitignore` but for inclusion)
   - If not found: defaults to including `.env` file only

2. **Password Setup:**
   - Checks `.env` file for `PRO7_PASSWORD` value
   - If not found: prompts for password input
   - Uses password to encrypt archive

3. **Archive Creation:**
   - Creates password-protected `.7z` archive
   - Places archive in workspace root
   - Updates archive automatically with latest changes

4. **Integration:**
   - Runs automatically in `G4 & .vsix` workflow
   - Ensures archive is up-to-date before GitHub push
   - Zero extra effort required

**`.pro7` Configuration Example:**

```
.env
.secrets.env
config/
secrets/
*.key
*.pem
api-keys.json
```

**Custom Command Integration:**

To include Pro7 Archiver in custom command sequences:

```json
{
  "label": "Your Label",
  "type": "command",
  "path": "ocrmnavigator.pro7.acrhive",
  "hidden": true
}
```

**Alternative: Standalone Script**

If the extension version doesn't work reliably, use the standalone script approach:

1. Place `pro7.js` in your autorun folder
2. Set extension setting to false: `"ocrmnavigator.PRO7": false`
3. Script runs separately from other autorun scripts

**Why Separate Script?** Microsoft's antivirus checks flag password-protected archives within `.vsix` files, causing potential issues.

<details>
<summary><b>pro7.js - Standalone Script</b></summary>

```javascript
const fs = require('fs');
const path = require('path');
const { glob } = require('glob');
const sevenBin = require('7zip-bin');
const { extractFull, add, list } = require('node-7z');

const WORKSPACE_ROOT = path.join(__dirname, '..', '..');
const PRO7_FILE = path.join(WORKSPACE_ROOT, '.pro7');
const ENV_FILE = path.join(WORKSPACE_ROOT, '.env');
const OUTPUT_PATH = path.join(WORKSPACE_ROOT, `pro7-${Date.now()}.7z`);
require('dotenv').config({ path: ENV_FILE });

async function pro7Archiver() {
    try {
        const password = process.env.PRO7_PASSWORD;
        if (!password) {
            console.error('✗ PRO7_PASSWORD is not set in .env file!');
            console.log('\nPlease set PRO7_PASSWORD in your .env file');
            process.exit(1);
        }

        let filesToArchive = [];

        if (fs.existsSync(ENV_FILE)) {
            filesToArchive.push(ENV_FILE);
            console.log('\n✓ Found .env file');
        }

        if (fs.existsSync(PRO7_FILE)) {
            console.log('✓ Found .pro7 file');

            const content = fs.readFileSync(PRO7_FILE, 'utf8');
            const lines = content.split('\n');

            for (const line of lines) {
                const trimmed = line.trim();

                if (!trimmed || trimmed.startsWith('#')) continue;

                if (trimmed.includes('*')) {
                    const globFiles = await glob(trimmed, { cwd: WORKSPACE_ROOT, absolute: true });
                    filesToArchive.push(...globFiles);
                    console.log(`✓ Found ${globFiles.length} files`);
                } else {
                    const fullPath = path.join(WORKSPACE_ROOT, trimmed);
                    if (fs.existsSync(fullPath)) {
                        filesToArchive.push(fullPath);
                        console.log(`✓ Added: ${trimmed}`);
                    } else {
                        console.log(`✗ Not found: ${trimmed}`);
                    }
                }
            }

            filesToArchive = [...new Set(filesToArchive)];
        } else {
            console.log('✗ .pro7 file not found');
        }

        if (filesToArchive.length === 0) {
            console.error('\n✗ No files to archive!');
            process.exit(1);
        }

        console.log('\n✓ Cleaning up old archives...');
        const existingArchives = await glob('pro7-*.7z', { cwd: WORKSPACE_ROOT, absolute: true });
        for (const archive of existingArchives) {
            fs.unlinkSync(archive);
            console.log(`  Deleted: ${path.basename(archive)}`);
        }

        const stream = add(OUTPUT_PATH, filesToArchive, {
            password: password,
            method: ['0=BCJ2', '1=LZMA2'],
            $bin: sevenBin.path7za,
            $progress: true
        });

        await new Promise((resolve, reject) => {
            stream.on('end', resolve);
            stream.on('error', reject);
        });

        console.log('✓ Archive path:', OUTPUT_PATH);

        const listStream = list(OUTPUT_PATH, {
            password: password,
            $bin: sevenBin.path7za
        });

        let fileCount = 0;
        listStream.on('data', (data) => {
            if (data.file) fileCount++;
        });

        await new Promise((resolve, reject) => {
            listStream.on('end', resolve);
            listStream.on('error', reject);
        });

        console.log(`✓ Archive contains `);
        console.log(`✓ ARCHIVING COMPLETED SUCCESSFULLY - CONTAINS ${fileCount} ${fileCount === 1 ? 'FILE' : 'FILES'}`);

    } catch (error) {
        console.error('\n' + '='.repeat(60));
        console.error('✗ ARCHIVE CREATION FAILED');
        console.error('='.repeat(60));
        console.error('\nError message:', error.message);
        console.error('Stack trace:', error.stack);
        process.exit(1);
    }
}

console.log('='.repeat(60));
console.log('PRO7 ARCHIVER');
console.log('='.repeat(60));
pro7Archiver();
```


</details>
---

[🡄 Return](https://github.com/8an3/DevStack)
*Her fingers dance along your length through the fabric, teasing and tempting.* "So what do you say, stud? Ready to show me what you've got...or are you all talk?"