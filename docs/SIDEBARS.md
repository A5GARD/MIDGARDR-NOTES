

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> DevStack Menu

Essentially, taking vscodes fragmented menu system and consolidating it to a single sidebar, in addition to that also creating line items that vscode failed to include within their menu system.

A lot of the created menu items will trigger an extensions function despite having its very own vscode command. This is because the command has been bundled up with other commands to make that command more effecient. For example, there are a lot of commands in which you need to trigger a save or save all event for the command to result in the desired outcome. 

With saying that, in respect to the save all command being bundled with other commands. There is another more important and rather a lot more secritive reason for this. Well, vscode keeps it a secret but obviously thats not the case here. 

Virtually every single function is bundled with the save all function, this is due to ensure that the recovery system set in place by vscode remains up to date and creates as many versions of the file and its data as possible.

Here is a outline of the current root level menu options that you can expect from this sidebar, along with any section that is expanded by default:
- 8an3
- Show Docs
- SEARCH/
  - ODIN: Search Editor
  - MIDGARDR Ul Components
  - BALDRIcons
  - DevStack Cmds
  - VSCode Cmds
  - Real Time VSCode Cmds
  - VSCode Product Icons
- Run Dev Server
- New Window
- New Terminal
- Format
- Organize
- Rename
- DevTools
- Kill Terminals
- Clear All Notifications
- Package.json SCRIPTS/ ( although devstack ( not the menu ) currently automatically displays ALL scripts these menu options refer to ones that are more commonly found no matter what project you are in )
    - Compile
    - Build
    - Start
    - Install
    - Dev
    - Kill
    - Clean
- VSCode/
- ,env/
- DEVSTACK CONFIG/
  - Search DevStack Config
  - Global Devstack Config
  - Workspace DevStack Config
- VSCode CONFIG/
  - GBL Settings File
  - WS Settings File
- FUNCTIONS/
- Shortcuts/
- THORCSS/
- FREYR/
- GitHub/
- SAGA: To Do/
- Prisma/
- Fold/
- Restart Instance

If you are wondering, "where are all the UI element triggers?", do not worry... there is an entire sidebar view devoted to the ui, as it too consolidates the even more fragmented menu system that manipulates the ui and even creating a very long list of other toggles that vscode forgot to include with its UI entirely.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Data And File Recovery

A lot of people do not know of this feature but a lot of people know of versioning through github and typically rely on that for file and data recovery.

There are, as far as I know, 3 recovery methods we have at our disposal and will go over each listing from easiest and well known to slightly difficult and rarely known:
1. timeline view - shows file history including git commits and local history combined
2. Local History - VSCode's built-in timeline of local file edits
3. workspaceStorage and History folders - this one being the most unknown recovery option and requires the user to open a specific folder residing in the vscode file system on your workstation.

All three options have menu options that work with all three, even the last option. The last option first checks what os your currently running, then checks to see which version of vscode your running, whether it is code or code-insiders and then opens the required folder needed to view these files.

Once that folder has opened you will very quickly notice that vscode did not anticipate users to access this folder, as it's very cryptic with its naming convention of files that are found within your workspace.

Each folder represents a file in your workspace, within that folder there will be several files for you to go through. Each file represents a recovery save point for that specific file. Due to the cryptic naming convenstions implemented by vscode, it might takes a couple of minutes just for you to find the right folder that you are looking for that is relevant to the data that you are trying to recover.

After writing this... because of how stupid vscode implementation is I might look into creating a new sidebar view devoted to file recovery.


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Clipboard History Pro

Multi-item clipboard manager that tracks and stores your clipboard history.

**Access:** Click `Clipboard++` on the status bar

**Features:**
- Track last 20 clipboard items
- Hover previews for quick reference
- Status bar access for convenience
- Persistent storage across sessions
- Quick paste from history

---

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Global Bookmarking System

Never lose your place in large projects again. The extension provides a persistent, global bookmarking system that allows you to tag specific lines of code and jump back to them instantly, even after restarting VS Code.

✨ Key Features
Persistent Storage: Bookmarks are saved to a bookmarks.json file in your global storage, ensuring they survive across sessions and workspaces.

Status Bar Integration: A permanent $(bookmark) Bookmarks item in your Status Bar provides one-click access to your list.

Quick-Access Navigation: Use the Quick Pick menu to search and filter your bookmarks. They are sorted by "most recent," so your latest work is always at the top.

Automatic Cleanup: To keep things fast and organized, the system maintains a rolling limit of 100 bookmarks, automatically removing the oldest ones as you add new ones.

Smart Updates: Adding a bookmark to a line that is already bookmarked will refresh its position to the top of your list.

#### Commands 

- ocrmnavigator.bookmarks.add
  - Adds the current line in the active editor to your bookmarks
  - Right-click line → DevStack → Add Bookmark
- ocrmnavigator.bookmarks.show
  - Bookmarks button in status bar

#### 🛠 Technical Details
Storage Location: %AppData%/Code/User/globalStorage/[extension-id]/bookmarks.json

Relative Paths: The navigation menu displays relative paths to make it easier to identify files within your current workspace.

#### Pro-Tip: How to Use
Place your cursor on a line you want to remember.

Right-click line → DevStack → Add Bookmark

Later, click the $(bookmark) Bookmarks icon in the Status Bar to see your history and jump back instantly.

![Bookmarks](https://raw.githubusercontent.com/8an3/midgardr-notes/main/bookmarks/bookmark.jpg?raw=true)

---


> [!NOTE]
>
> Whether it is product icons, file icons or themes, they need to activated via the file drop down menu > prefrences > themes > and selecting the desired option

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Custom Product Icons

Please refer to file icons sidebar for full list of custom icons to view, in addition to vscodes default file icons.

Selecting any menu option will copy the value to your clipboard to be used anywhere you would like.


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> File Icons
A variety of custom icons has been created for use within the explorer pane. Icons are styled the same as they were created by the original creators and even following the original color scheme, only deviating on a few select colors such as black for example. 

Despite using the original logo's, each svg was edited in order to obtain the most clarity out of each svg. Where applicable a black background was place behind the logo, in order for the text/logos to appear sharper when rendered while at the same time, not letting your current color scheme change the overall look of each of the icons.

Different colored icons were used when needed in order to seperate different file types, for example js and jsx extensions, while both javascript files two seperate colors were used to allow you to quickly discern which is which.

An idea that was adopted ( we'll see how this one goes, but seems to be working as intended ), vscode allows for a different icon to be used for open folders. Instead of following the norm in which the same color is used for both icons, I opted to instead use a different color which provides a stark contrast to its neibhouring folders. When quickly moving your cursor over to expand or collapse the desired folder allowing you to continue looking at what your working on and only identifying the folder out of the corner of your instead of having to follow the cursor over.

The color scheme that was implemented, again going against the norms, instead of having both light and dark themed icons in its place a single color was used. Using the entire span of the color wheel, but only using the 500 variant from each. Giving it a vibrant enough color that can be used with dark or light themes, while also allowing you to not only more quickly get used to the colors, since there are half of them to get used to, but also cuts down on the amount of time to become accustomed to the new color variations whenever you swap from light to dark themes and vice versa. But this point really only being important when a stock logo was unavailable for use with certain file extensions. Currently, I'm not worried about color collisions, as each folder is typically pretty well organized when it comes to containing file extensions. As you normally wouldn't host all of your image and video files along side all of your different files type catering to your code.

Lastly when a stock logo was unavailable for a specific file type, a specific placeholder was used instead for example for files ending in png, the icon used features a file with the capital letters PNG featured at the bottom. In addition to that, different colors were used for each file type in order to help quickly pick out by file type based on color alone.

png - teal #14b8a6
bmp - purple-600 #9333ea
txt - sky #0ea5e9
csv - green #22c55e
doc - blue-600 #2563eb
pdf - red #dc2626
gif - amber #f59e0b
ttf - yellow #eab308
jpg - emerald #10b981
zip - cyan #06b6d4

blue #3b82f6
orange #f97316
lime #84cc16
indigo #6366f1
violet #8b5cf6
purple #a855f7
fuschia #d946ef
pink #ec4899
rose #f43f5e


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> BALDR

A React icon library designed for simplicity and accuracy with a sensible naming convention.

**Installation:**

```bash
npm install @a5gard/baldr
# or
pnpm add @a5gard/baldr
```

**Usage:**

```javascript
import { Message } from '@a5gard/baldr'
```

**Features:**
- Clean, logical naming convention
- Filled variants available
- Customizable colors
- Flexible sizing options
- Designed for React applications

![NPM Icon Library](https://raw.githubusercontent.com/8an3/midgardr-notes/main/icons/npm-icon.jpg?raw=true)


---

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Icons Sidebar


Browse and insert icons from the @a5gard/baldr library directly in your editor


**Access:** Editor context menu → Catalyst → Icons

**Features:**
- Integrated search functionality
- Instant insertion at cursor position
- Complete library access
- Preview icons before insertion

**Naming Convention:**  
Icons follow a logical pattern: `[MainTheme][Container/Feature][Filled]`

**Example:** `MessageSquareFilled`, `UserCircle`, `SettingsGear`

> [!NOTE]
>
> You will now be able to search through vscodes file icons and the registered file icon theme pack that is registered through this extension that also contains a fuzzy search at the top of the sidebar to allow for easier filtering

 
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> VSCode Icons

Visual reference for all available VSCode icons and their identifiers.

**Access:** DevStack Quick Pick menu in status bar

**Features:**
- Browse complete icon library
- Search by name or category
- Quick copy icon identifiers
- Visual preview of all icons
- Integration with custom commands

**Usage:** Perfect for customizing your extension commands, status bar items, and UI elements with the right visual indicators.

**Note:** Regularly updated to include new VSCode icon additions and improvements.


---

[🡄 Return](https://github.com/8an3/DevStack)



## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> SAGA
### Notes Manager & GitHub Sync Extension

A comprehensive VS Code extension for managing notes, todos, reminders, and post-it pads with GitHub synchronization capabilities.

> [!NOTE] 
> I thought I would mention this because, it didn't dawn on me the gravity of the situation when it comes to the level of issues, well lack of to be more precise since I haven't had a single reject push while using github as a source of truth. 
>
> If your thinking that I may be babying the system, far from it. At times I'll have 4 workspaces open, all have their own "instance" of the note app meaning that, they aren't linked to one another in any way, except the repo. I'll create a note in one, leave it unsaved, jump to another workspace create and save a new note, jump to another workspace create a new note but not for my current workspaces files, but for the one that still has an unsaved note open. Saving that note, jumping back to the original workspace to finish off that note and save it. 
>
> Meanwhile under the hood, every save event executes a custom push sequence where I have not experienced a single reject in 9-10 months. Not to mention, making matters worse, the UI is pretty sweet when it comes to the to do lists. This is due to the fact that you do not even need to open the file, to check or uncheck to do items, each check pushes the save to github and if you do 3 or 4 really fast... that's ok, because if one push were to be triggered before the current one finishes, it just gets added to a queue. Even when you trigger it 10 times, theres 10 items in the queue and they get done when they get done.



### Table of Contents

1. [Notes Manager & GitHub Sync Extension](#notes-manager--github-sync-extension)

2. [To-Do Extension Feature Comparison](#to-do-extension-feature-comparison)
   - [DevStack vs Marketplace Leaders](#devstack-vs-marketplace-leaders)
   - [Marketplace Leaders Overview](#marketplace-leaders-overview)
   - [Feature Comparison Table](#feature-comparison-table)

3. [Key Differentiators](#key-differentiators)
   - [DevStack To Do's Unique Advantages](#devstack-to-dos-unique-advantages)
   - [Why DevStack Doesn't Need Their "Features"](#why-devstack-doesnt-need-their-features)

4. [The Real Comparison](#the-real-comparison)
   - [What Each Extension Actually Does](#what-each-extension-actually-does)
   - [The Use Case Difference](#the-use-case-difference)

5. [Why The Comparison Is Misleading](#why-the-comparison-is-misleading)
   - [The Real Competitive Landscape](#the-real-competitive-landscape)

6. [Bottom Line](#bottom-line)

7. [Features](#features)
   - [📝 Note Management](#-note-management)
   - [✅ Todo/Checklist Management](#-todochecklist-management)
   - [⏰ Reminder System](#-reminder-system)
   - [📌 Post-It Pads](#-post-it-pads)
   - [🔄 GitHub Synchronization](#-github-synchronization)
     - [Core Sync Operations](#core-sync-operations)
     - [Repository Management](#repository-management)
     - [Git Operations](#git-operations)
     - [Advanced Features](#advanced-features)

8. [Getting Started](#getting-started)
   - [Personal Access Token Guide](#personal-access-token-guide)
   - [Configuration Options](#configuration-options)

9. [Usage](#usage)
   - [Creating](#creating)
   - [Editing](#editing)
   - [Deleting](#deleting)
   - [Code Highlighting](#code-highlighting)

10. [Troubleshooting & Advanced Commands](#troubleshooting--advanced-commands)

11. [To Do, Notes and Reminders PWA Web App](#to-do-notes-and-reminders-pwa-web-app)
    - [Architecture Overview](#architecture-overview)

### To-Do Extension Feature Comparison

### DevStack vs Marketplace Leaders
### Marketplace Leaders Overview
- **To Do 1** (6,773,736 installs) - Searches code for TODO/FIXME comments
- **To Do 2** (455,503 installs) - Manages TaskPaper-style todo files

---

| Feature | DevStack To Do | To Do 1 | To Do 2 |
|---------|------------------|-----------|-------|
| **Installation Base** | Growing | 6.7M | 455K |
| **Core Functionality** |
| Purpose | Full task management system | Code comment scanner | Todo file manager |
| Multiple Note Types | ✅ (Notes, Todos, Reminders, Post-Its) | ❌ (Comments only) | ✅ (Todos only) |
| Hierarchical Organization | ✅ (Priority, Normal, Completed, Trashed) | ✅ (By folder/tag) | ✅ (Projects) |
| Nested Checklists | ✅ (Unlimited depth with collapsible sections) | ❌ | ❌ |
| Label System | ✅ (Custom labels) | ⚠️ (Tags in comments) | ✅ (Tags) |
| **Storage & Sync** |
| File-Based Storage | ✅ (Markdown in `.vscode/ntrsync/`) | ❌ (Scans existing code) | ✅ (Custom format) |
| GitHub Sync | ✅ (Full bidirectional) | ❌ | ❌ |
| Cloud Backup | ✅ (GitHub as source of truth) | ❌ | ❌ |
| Offline Support | ✅ (Full offline capability) | ✅ (Local only) | ✅ (Local only) |
| Cross-Device Sync | ✅ (Automatic via GitHub) | ❌ | ❌ |
| **Access & Availability** |
| VSCode Interface | ✅ | ✅ | ✅ |
| Web UI | ✅ (Full PWA) | ❌ | ❌ |
| Mobile Access | ✅ (PWA on phone) | ❌ | ❌ |
| Offline Mobile Use | ✅ (Works with zero cell service) | ❌ | ❌ |
| Desktop App Access | ✅ (PWA) | ❌ | ❌ |
| Works Without VSCode | ✅ (Web UI always accessible) | ❌ (VSCode required) | ❌ (VSCode required) |
| **Reminders & Time** |
| Due Date Tracking | ✅ (Full date/time support) | ❌ | ⚠️ (Manual tags) |
| Reminder Categories | ✅ (Coming Up, Missed, etc.) | ❌ | ❌ |
| Active Reminder Notifications | ✅ (Triggers inside VSCode) | ❌ | ❌ |
| Time Estimates | ❌ (Not needed - GitHub tracks actual time) | ❌ | ✅ (`@est` tags) |
| Time Tracking | ✅ (GitHub commit timestamps & history) | ❌ | ⚠️ (Manual `@started` tags) |
| Overdue Notifications | ✅ | ❌ | ❌ |
| **Post-It Notes** |
| Post-It Pad Feature | ✅ (5 color-coded pads) | ❌ | ❌ |
| Auto-Save | ✅ (500ms debounce) | N/A | ⚠️ (On file save) |
| Quick Actions | ✅ (Copy, clear, delete all) | N/A | N/A |
| **GitHub Integration** |
| Push to GitHub | ✅ | ❌ | ❌ |
| Pull from GitHub | ✅ | ❌ | ❌ |
| Bidirectional Sync | ✅ | ❌ | ❌ |
| Create Repository | ✅ (From VSCode) | ❌ | ❌ |
| Branch Management | ✅ (Create, switch, rename, delete) | ❌ | ❌ |
| Collaborator Management | ✅ (Granular permissions) | ❌ | ❌ |
| Private Repositories | ✅ | ❌ | ❌ |
| Conflict Resolution | ✅ (Smart merge) | ❌ | ❌ |
| Auto-Sync | ✅ (Configurable interval) | ❌ | ❌ |
| **Git Operations** |
| Commit Management | ✅ (Standard, staged, amend, undo) | ❌ | ❌ |
| Stash Operations | ✅ (Create, apply, pop, drop) | ❌ | ❌ |
| Tag Management | ✅ (Create, delete, push) | ❌ | ❌ |
| Remote Management | ✅ (List, add, remove) | ❌ | ❌ |
| **Code Integration** |
| Find TODO in Code | ⚠️ (Coming soon) | ✅ (Main purpose) | ✅ (Embedded todos) |
| Highlight in Editor | ⚠️ (Coming soon) | ✅ (Configurable) | ✅ (Configurable) |
| Custom TODO Tags | ✅ (Unlimited markdown sections) | ✅ (Fully customizable) | ✅ (Fully customizable) |
| Regex Search | ❌ (Not needed - proper organization) | ✅ (ripgrep) | ✅ (ag/rg/js) |
| **Tree View & UI** |
| Tree View in Activity Bar | ✅ | ✅ | ✅ |
| Expand/Collapse Todo Lists | ✅ (Each file collapses/expands) | ✅ | ✅ |
| Expand/Collapse Nested Sections | ✅ (Sections act as folders) | ❌ | ❌ |
| Single-Click Complete | ✅ (Click checkbox = done + sync) | ❌ (Must open file) | ❌ (Must open file) |
| Single-Click Edit | ✅ (Click title = open file) | ✅ (Click = navigate to line) | ✅ (Click = open file) |
| Filter/Search | ✅ | ✅ | ✅ |
| Context Menu Actions | ✅ | ✅ | ✅ |
| Drag and Drop | ❌ (Not needed - context menus) | ❌ | ❌ |
| Status Bar Integration | ❌ (Full sidebar UI) | ✅ (Counts) | ✅ (Statistics) |
| **Advanced Features** |
| Custom Sections in Markdown | ✅ (Unlimited, any name you want) | ❌ | ⚠️ (Projects only) |
| Hierarchical Organization | ✅ (Files + nested collapsible sections) | ⚠️ (Folders only) | ⚠️ (Projects only) |
| Statistics | ❌ (GitHub provides better tracking) | ⚠️ (Basic counts) | ✅ (Detailed stats) |
| Time Tracking | ✅ (GitHub commit timestamps & history) | ❌ | ⚠️ (Manual `@started` tags) |
| Archive System | ✅ (Completed/Trashed folders) | ❌ | ✅ (Archive section) |
| Markdown Support | ✅ (Native markdown files) | ✅ (Markdown todos) | ⚠️ (Custom format) |
| Formatting | ✅ (Full markdown) | ❌ | ✅ (Bold, italic, code) |
| Multi-line Todos | ✅ | ✅ (Configurable) | ✅ |
| **Data Management** |
| Export Functionality | ✅ (Via GitHub) | ✅ (To file) | ❌ |
| Import Functionality | ✅ (Via GitHub) | ❌ | ❌ |
| Backup System | ✅ (GitHub) | ❌ | ❌ |
| Version Control | ✅ (Full Git history) | ❌ | ❌ |
| **Collaboration** |
| Team Sharing | ✅ (Via GitHub repo) | ❌ | ❌ |
| Permission Control | ✅ (GitHub collaborators) | ❌ | ❌ |
| Real-time Sync | ✅ (Configurable) | ❌ | ❌ |
| **Security** |
| Private Data Support | ✅ (Private repos) | ✅ (Local only) | ✅ (Local only) |
| Token Security | ✅ (VSCode secrets API) | N/A | N/A |
| Auto .gitignore | ✅ (`.vscode/ntrsync/`) | N/A | N/A |
| Encryption Support | ⚠️ (Via Pro7 tool) | ❌ | ❌ |
| **Progressive Web App** |
| Offline-First Architecture | ✅ | ❌ | ❌ |
| Local Caching | ✅ | ❌ | ❌ |
| Sync Queue | ✅ | ❌ | ❌ |
| Conflict Resolution | ✅ | ❌ | ❌ |
| Zero Data Loss | ✅ | N/A | N/A |
| Works on Plane/Subway | ✅ | ❌ | ❌ |

---

### Key Differentiators

### DevStack To Do's Unique Advantages

1. **True Cross-Platform System**
   - Works in VSCode, web browser, mobile, desktop
   - Fully functional offline (even with zero cell service)
   - Not locked to VSCode being open
   - **ONLY todo extension using GitHub as source of truth**

2. **Enterprise-Grade Architecture**
   - GitHub as source of truth
   - Bidirectional sync with conflict resolution
   - Private repository support
   - Team collaboration with granular permissions

3. **Perfect Tree View UX**
   - Single-click checkbox to complete (never open file)
   - Single-click title to edit (opens when you need it)
   - Collapsible todo lists (organized by filename)
   - Nested collapsible sections (folders within lists)
   - Hierarchical organization without complexity
   - Zero confusion - interface explains itself

4. **Complete Task Management**
   - Multiple note types (Notes, Todos, Reminders, Post-Its)
   - Hierarchical organization (Priority → Normal → Completed → Trashed)
   - Unlimited custom markdown sections (name them whatever you want)
   - Due date tracking with overdue detection
   - **Active reminder notifications inside VSCode**
   - Label system for categorization
   - GitHub provides automatic time tracking via commit history

5. **Git Integration**
   - Full repository management from VSCode
   - Branch operations, stash management, tag control
   - Collaborator management with permission levels
   - Complete commit workflow

### Why DevStack Doesn't Need Their "Features"

**Regex Search**: They need regex because their systems are disorganized. DevStack has proper hierarchical organization (files, nested sections, priority folders, labels) - you can find anything instantly without searching.

**Manual Time Tracking Tags**: They type `@started` and `@est(2h)` manually. DevStack uses GitHub which automatically tracks every save, commit, and edit with timestamps, contribution graphs, and full version history.

**Custom Tag Systems**: They let you rename rigid categories (TODO → FIXME → HACK). DevStack uses markdown files where you create unlimited sections with any names you want (`dildo` if you want). Complete freedom.

**Statistics Counters**: They show "You created 47 todos!" DevStack uses GitHub which provides real productivity data: commit history, contribution graphs, actual completion tracking.

**Drag and Drop**: Slow and imprecise. DevStack uses context-aware right-click menus that show only relevant actions per item type.

**Status Bar Counts**: Tiny counter showing "5 TODOs". DevStack IS the entire sidebar with full tree view, nested organization, and instant interaction.

**Code TODO Scanning**: Only needed because their todo systems suck so badly that developers prefer leaving `// TODO` comments. DevStack makes creating proper todos so easy (5 seconds, single click in sidebar) that code comments become unnecessary. *Note: Adding highlight feature anyway because it's nice UX.*

---

### The Real Comparison

### What Each Extension Actually Does

**To Do 1** is a **code comment scanner**. It helps developers find TODO/FIXME comments scattered throughout their codebase. It's not a task management system - it's a search tool.

**To Do 2** is a **plain text todo file manager**. It manages todo lists in dedicated files using a custom format. It's VSCode-only and local-only.

**DevStack To Do** is a **complete task management platform** that happens to integrate with VSCode. It's the only extension that:
- Works outside of VSCode
- Syncs across devices automatically
- Functions fully offline on mobile
- Uses GitHub for backup and collaboration
- Provides team collaboration features
- Has enterprise-grade architecture

### The Use Case Difference

**To Do 1 Users**: "I need to find all the TODO comments in my code"
- Scans existing codebase
- Highlights todos in editor
- Quick navigation to comments

**To Do 2 Users**: "I need a text-based todo list inside VSCode"
- Creates dedicated todo files
- Manages tasks in plain text
- Local-only workflow

**DevStack To Do Users**: "I need a complete task management system that works everywhere"
- Manages all types of notes/tasks/reminders
- Works on phone, tablet, laptop, desktop
- Functions offline in subway/plane/remote areas
- Syncs automatically across all devices
- Collaborates with team via GitHub
- Never loses data

---

### Why The Comparison Is Misleading

Comparing DevStack To Do to To Do 1 or To Do 2 is like comparing:
- **Notion** vs **grep** (they both find text, right?)
- **GitHub** vs **local Git** (they both version control, right?)
- **Google Drive** vs **File Explorer** (they both manage files, right?)

The marketplace "leaders" aren't actually competitors - they solve different problems:
- **To Do 1**: Development workflow tool for navigating code comments
- **To Do 2**: Lightweight text-based task list for developers
- **DevStack To Do**: Enterprise task management platform with offline-first PWA

### The Real Competitive Landscape

DevStack To Do competes with:
- **Todoist** (requires internet, no offline mobile)
- **Notion** (requires internet, limited offline)
- **Microsoft To Do** (requires internet, breaks offline)
- **Google Keep** (requires internet, no offline support)
- **Asana/Trello/Jira** (require internet, enterprise only)

And DevStack To Do beats all of them because:
1. Works fully offline (zero cell service)
2. Free (GitHub as backend)
3. Private (your data, your repo)
4. Integrated with development workflow
5. No vendor lock-in
6. Open data format (Markdown)

---

### Bottom Line

**To Do 1** has 6.7M installs because it solves a simple, common problem: finding TODO comments. It does one thing well.

**To Do 2** has 455K installs because it's a solid text-based todo manager for developers who want simplicity.

**DevStack To Do** is the only VSCode extension that provides:
- Full offline mobile access (works with zero cell service)
- Cross-device automatic sync
- **GitHub as source of truth (ONLY extension)**
- Active reminder notifications inside VSCode
- Works without VSCode being open
- Enterprise-grade architecture
- Progressive Web App functionality

The install count isn't something I track or prioritize. DevStack was built entirely for my own use—every feature exists because I needed it. The documentation only exists for two reasons: first, users somehow found and started using the extension even before any readme existed, and second, I needed a reference for myself to remember what's currently in DevStack and how it's configured. Without that unexpected user base, the docs would be far less detailed than they are now.

Honestly, I'm still baffled by how those initial users even discovered the extension. It had a confusing name that bore no relation to its functionality, and there was literally zero documentation. I only published it to the marketplace so I could easily install it across different machines where I code—I never anticipated anyone else downloading it. The only reason I included the above comparison, is because in regards to this extensions features, previously I was selling each feature short and not including enough reasons on why you should use it.

### Features

![Explorer pane](https://raw.githubusercontent.com/8an3/midgardr-notes/main/todo/main.jpg)

### 📝 Note Management
- **Multiple Note Types**: Support for regular notes, todos (checklists), and reminders
- **Hierarchical Organization**: Notes organized by priority (Priority, Normal, Completed, Trashed)
- **Label System**: Organize notes with custom labels
- **File-based Storage**: All notes stored as Markdown files in `.vscode/ntrsync/`

### ✅ Todo/Checklist Management
- **Nested Checklists**: Support for indented, hierarchical todo items
- **Check Item Tracking**: Toggle completion status for individual items
- **Auto-parsing**: Automatically parses Markdown checklist syntax (`- [ ]` and `- [x]`)
- **Tree View**: Visual representation with expand/collapse functionality

### ⏰ Reminder System
- **Due Date Tracking**: Set and track reminder due dates
- **Smart Categorization**: 
  - Coming Up (next 24 hours)
  - Missed (overdue)
  - Normal, Completed, Trashed
- **Date Format**: `DUE: YYYY-MM-DD HH:MM` in note content

### 📌 Post-It Pads
- **5 Color-Coded Pads**: White, Green, Blue, Indigo, Orange
- **Auto-Save**: Content saves automatically with 500ms debounce
- **Quick Actions**: Copy content, clear individual pad, delete all pads
- **Persistent Storage**: Content saved to workspace state

### 🔄 GitHub Synchronization

#### Core Sync Operations
- **Push**: Upload local changes to GitHub repository
- **Pull**: Download remote changes to local workspace
- **Sync**: Combined pull + push operation
- **Queue Management**: Prevents concurrent push operations

#### Repository Management
- **Create Repository**: Initialize new GitHub repos directly from VS Code
- **Select Repository**: Browse and connect to existing repositories
- **Branch Management**: Create, switch, rename, and delete branches
- **Privacy Control**: Support for both public and private repositories

#### Git Operations
- **Commit Management**: 
  - Standard commits, staged commits, commit all
  - Amend commits, undo last commit
  - Abort rebase operations
- **Change Management**:
  - Stage/unstage all changes
  - Discard all changes
- **Stash Operations**:
  - Create, apply, pop, drop stashes
  - Include untracked files option
- **Tag Management**:
  - Create, delete, push tags
  - Remote tag deletion
- **Remote Management**:
  - List, add, remove remotes
  - Fetch operations with pruning

#### Advanced Features
- **Collaborator Management**: 
  - Share repositories with permission levels (Read, Triage, Write, Maintain, Admin)
  - Remove collaborators
- **Auto-Sync**: Configurable automatic synchronization
- **Conflict Resolution**: Smart merge handling
- **Rate Limit Handling**: Graceful handling of GitHub API limits

### Getting Started

1. Click on the `DevStack` button found on the left hand side of the status bar to pull up the quickpick

![Explorer pane](https://raw.githubusercontent.com/8an3/midgardr-notes/main/todo/status-bar.jpg)

> [!TIP] 
> When starting this process, it will be a lot easier if you already have your github access token created with the value temparirly stored somewhere, like your .env file. ( the process to start follows these two tip sections )
> Once you input your access token, just make sure to delete it where ever you placed it, as you will only need this once.
>
> Creating a classic token is far easier, of the two available options, [click here to navigate straight to the classic tokens page](https://github.com/settings/tokens).
>
> Once there, there is only 2 requirements but if you want to do everything from the extension, you should enable more access. Personally through my access token I can create, edit, share, unshare and delete repos and more.
>
> When this was first build, it was built in a way where it did not limit you in order to do anything in regards to your repo.
>
> Once completed with setting the permissions, don't forget to name it.
>
> If your new to tokens, as soon as the key generates copy it to your clipboard and, for the time being, place it within your .env file till you get to that point in the set up process as this token only shows up once, if you navigate anywhere from that page you will have to remake a new one.
>
> Then within the devstack menu, under saga select 'set all' and it will guide you through the process.
>
> You can technically skip, and place everything but your access token into your settings.json file.

```json
{
    "ocrmnavigator.todo.branch": "main",
    "ocrmnavigator.todo.repo": "mynotesrepo",
    "ocrmnavigator.todo.owner": "8an3",
}
```


1. `To do / Notes` → `Set All`
  - this initiates the configuration process for everything that is needed
  - you can create a new repo to start one dedicated to to do lists, notes and reminders
  - you can set that repo to private or public
  - set the repo name, everything
  - when finished it creates a folder in your .vscode workspace folder to store everything so it does NOT clutter up your workspaces root file system

![Explorer pane](https://raw.githubusercontent.com/8an3/midgardr-notes/main/todo/qp.jpg)

2. OR if you would like, you may configure each item on its own, setting repo, access token branch, owner, and so forth

Once you have already inputted your access token, it becomes very easy to `select` a repo to use as your source of truth, for example:
  - if you have two / three to do repos as sources, for work, personal and so on
  - all you have to do is is use `list repo` and select the repo you would like to use, and it automatically pulls the repo, replacing whatever other sources data file you had already, ensuring there is no data leakage from other sources

3. OR if you would like to configure via settings.json instead, you may do so for everything BUT inputting githubs access token

```json
{
  "ntrsync.owner": "user",
  "ntrsync.repo": "repo",
  "ntrsync.branch": "main",
  "ntrsync.isPrivate": false,
  "ntrsync.autoSync": true,
  "ntrsync.syncInterval": 300000,
  "ntrsync.checkRemindersInterval": 15
}
```

### Usage

### Creating

Click `+` in the sections title pane

### Editing

- To do lists
  - left clicking a to do list item, checks it off or marks it as complete and syncs to github
  - left click on any to do lists title, to open that lists markdown file to view, edit, create, delete line items as you see fit
- notes / reminders
  - clicking on any items title will open the relevant markdown file to edit
- items, depending on its type, will also automatically set their own labels based on events, such a `coming up` or `missed` for reminders
- you may also set the priority of any item by right clicking the item, and selecting the desired option

![Explorer pane](https://raw.githubusercontent.com/8an3/midgardr-notes/main/todo/context.jpg)

### Deleting

- each item, regardless of type, has a context menu which will allow you to delete that item
- there are two options for deleting
  - first option is `move to trash`, essentially a recycle bin allowing to `soft` delete items
  - `delete`, this not only deletes the item locally, but also in your repo as well
  - allowing you to control who to grant share permission and who to revoke those same permission

> [!TIP] 
> If for whatever reason, something does happen during a github process ( one that I have yet to run into ), there is every single github command available to you in order to fix, whatever issue you may run into
> To top it off, there is even a `custom` input allowing you to run any github command from the to do local repo instance
>
> These commands were never meant to be used as a troubleshooting solution, but were added at this features creation because I thought they were needed due to working with a github repo as the source of truth
>
> Personally... I haven't touched any of those functions in over 8 months. The only reason I left them, is because they were already coded, and maybe who knows. There be an edge case that would benefit from them so I never saw the need to spend the time to remove them. These can be found in the to do section of the DevStack quickpick.
> These menus are labeled:
>   - `basic`
>   - `ADV`
>   - `settings`
> If you use the `Set All` option when first starting out, you will not run into any problems at any time, and will not need to use any other menu option to set anything up
> The only time you may run into an issue, is if you remove `.vscode/ntrsync` from .gitignore, as the extension automatically adds this to that file to ensure you do not run into any problems. As we are running a repo, inside of a repo, without this there may be weird times where your github functionality through the vscode interface, may act strangely. Even so, these `issues` were a case by case basis and did not effect everyone. Adding this rule to .gitignore, made it so that no one had an issue, at any time.
> But what is included in those menus, you might be wondering
> - basic
>   - Commit
>   - Changes
>   - Pull
>   - Push
>   - Pull Push
>   - sync
>   - Branch
>   - Remote
>   - Stash
>   - Tags
>
> - ADV
>   - Clone
>   - Checkout
>   - Fetch
>   - Tags
>   - Diff Cached
>
> - settings
>   - patch Version
>   - share Repo
>   - remove Collab
>   - set access token
>   - show access token 
>   - navigate To Token Gen
>   - configure Github Sync
>   - go to Settings File
>   - place AllSettings In Clipboard
>   - reload Ext
>   - toggle Auto Sync
>   - reset Local Directory Pull Repo
>   - customCmd
>   - showConfig

> [!TIP] IF you need to do a complete RESET of your to do, notes and reminders
>
> For whatever reason, and you have to do a hard reset ie, deleting everything locally and pulling from your repo to start fresh
> `devstack` quickpick menu → `To do / Notes` → `Settings` → `reset Local Directory Pull Repo`
 
> [!TIP] IF you want / need to verify your access token that is currently in use
>
> `devstack` quickpick menu → `To do / Notes` → `Settings` → `show access token`

> [!TIP] IF you need to set an access token, because for some reason you didn't during the set up process
>
> `devstack` quickpick menu → `To do / Notes` → `Settings` → `set access token`

> [!TIP] IF you need to access the custom github command feature 
>
> `devstack` quickpick menu → `To do / Notes` → `Settings` → `customCmd`

![Explorer pane](https://raw.githubusercontent.com/8an3/midgardr-notes/main/todo/github-functions.jpg)



### Code Highlighting

On any line item use the following format

```markdown
- [ ] terminal engine - currently if there is a dev server, nothing will execute... need to check and see if the current terminal window is busy... if it is create a new terminal instance 
- [ ] HL:src\helpers\master.ts:330-371
```

```markdown
- [ ] terminal engine - currently if there is a dev server, nothing will execute... need to check and see if the current terminal window is busy... if it is create a new terminal instance HL:src\helpers\master.ts:330-371
```

- IF a line item is completed, the code will NOT be highlighted
- IF a line item is un-completed, the code will be highlighted


### To Do, Notes and Reminders PWA Web App

- **Progressive Web App** (PWA) with offline functionality
- **Local storage/caching** for all your to-dos
- **Sync queue** that uploads changes when connection returns
- **Conflict resolution** for when multiple devices edit offline
- **Full CRUD operations** without internet

### The architecture:
1. GitHub as source of truth
2. Local caching on every device (phone, laptop, VSCode, desktop)
3. Works completely offline
4. Syncs automatically when connection available
5. Zero data loss

You can be:
- On a plane (no service)
- In a subway (no service)  
- In the middle of nowhere (no service)
- Still add/edit/complete to-dos
- Everything syncs when you get connection back

Meanwhile the "competition":
- **VSCode extensions**: Require VSCode to be running
- **Notion/Todoist/etc**: Require internet connection
- **Most to-do apps**: Break completely without connection

MEANWHILE, no extension available on the marketplace has the ability to not only view, edit and delete items via vscode interface but also sync with a pwa web app that has full synch capabilities. To top it off the web app ui contains features not found in any other to do app, even through other sources other than vscodes marketplace. The added `slice of life` touches to the ui, really makes the user experience just that much better by alleviating as much friction when using the application.
 


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> ODIN Workspace Context File Versioning And History
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> ODIN FILE EXPLORER
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> ODIN SEARCH
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> ERRORS
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> BROKKR MENU
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> BROKKR VIEWER
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> GITHUB / WORKSPACE CONTEXT NOTES
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> COLOR WHEEL
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> HEIMDALLR

