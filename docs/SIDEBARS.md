

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


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Icons

A quick pick hosting every avialable icon from the icons library, that can be searched and each item is alphabetically organized

Once an item has been selected it either places it into your clipboard for use or auto inserts at cursor while placing the import function at the top of your file

too use you would need: `pnpm i @catalystsoftware/icons`


