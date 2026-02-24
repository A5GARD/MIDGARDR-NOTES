
### <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="25"  style="vertical-align: middle; margin-bottom: 4px;"> IDEAS

- regex scratch pad - check current regex feature if this is too close to what is currently already there, a panel where you paste text, write a regex, and see matches highlighted live as you type.

### <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="25"  style="vertical-align: middle; margin-bottom: 4px;"> DOCUMENTATION NEEDED

- [X] auto port ngin ie dynamic oort & tunnel management
  - Provide the entire powershell command  replacing the port number with ${PORT}  Devs struggle with "Which port is my app running on?" and "How do I show this to my teammate?"The Feature: A Sidebar View that automatically detects all active local ports (e.g., 3000, 8080) and provides a one-click button to: Kill the process on that port (no more lsof -i :3000). Expose it via a secure tunnel (like Ngrok or VS Code Port Forwarding) and copy the URL. Label the port based on the process name (e.g., "Frontend - Vite"). The Utility: It turns the terminal-heavy task of port management into a visual dashboard
- midgardr sdk: heimdallr
- session journal / workspace context project notes - manually log notes against current git branch or file set, or even becasue we already have workspace context up and running so well already, maybe add a note item to the the terminal ngin that creates a note folder that is hidden from the devstack pane and acts as a data source for all notes within that workspace
- heracles / batch rename
- visualizer
- vscode tailwind
- vanilla md renderer
- Workspace Context File History / Versioning - 
- updating search features 
- local workspace context backup system
- license tempalte wizard
- readme tempalte wziard
- changelog template wizard
- file icons, baldr icons, and product icons searchable sidebar
- searchable book marks and clipbaord histry
- data and file recovery sidebar
- workspace context file history and versioning
  - saves the last 50 file saves providing a in app versioning and history system for file
- Sqlite3



### <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="25"  style="vertical-align: middle; margin-bottom: 4px;"> TO DO


- [ ] BROKKR V2
- [ ] Option B: Extension-Based Snippets (The "Pro" Way)
  Since you mentioned building a VS Code Extension in your philosophy, you can use the vscode.TextEditorEdit API. This allows you to literally teleport code to the top of the file while dropping code at the cursor.
  Here is a simplified logic for your extension:
  JavaScript
  // Inside your extension command
  editor.edit(editBuilder => {
      // 1. Insert the import at the very top (0, 0)
      editBuilder.insert(new vscode.Position(0, 0), "import { Input } from '#midgardr/Input';\n");
      // 2. Insert the usage at the current cursor position
      editBuilder.insert(editor.selection.active, "<Input $0 />");
  });
- [ ] REMOTE ACCESS / EDITING
  - [ ] access to:
  - [ ] config
  - [ ] snippets
  - [ ] todo, notes and reminders
  - [ ] be able to download your config from anywhere
  - [ ] set up user profile on site
  - [ ] user github email for syncing data
- [ ] COPY WORKSPACE FOLDER
  - [ ] to make it even easier to configure new / existing configs
  - [ ] provid a list of folders contained within other configs once clicked pastes it into the current configs file
- [ ] creating incoming tunnel 
  - The Pain: working on a mobile   Detects SQLite by magic bytes (SQLite format 3\0), Not by extension  app or an external API that needs to see your local server. You have to open a    separate terminal, remember your ngrok or localtonet command, copy the new URL,   and paste it into your config. It automates the "copy-paste" loop between the  terminal and your code. A specialized command  that launches a tunnel (like ngrok  http 3000), captures the generated URL, and automatically updates a specific  line in your config.ts or .env with the new public URL. The Fix: A tunnelLauncher
- [ ] api secret grabber
  - (vaultFetch) You need a staging/prod API     key that isn't in your local .env for security reasons. You have to log into AWS Secrets Manager, 1Password, or  your company Wiki, find the key, and copy it.  A type  that fetches a value from a CLI-based vault (like gh secret, aws secretsmanager, or a  local encrypted file). It executes the CLI fetch and uses your existing copyToClipboard logic to put the secret in your hand instantly. 
- [ ] log to lens
  - (errorParser) The Pain: Your build failed or your  test crashed. The terminal is a wall of 500 lines of red text. You have to scroll up,  find the file path in the stack trace, copy it, Ctrl+P, and paste the path to fix the bug. Scans the last output of the integrated terminal for file paths and line numbers. It then populates the Navigator with "Jump to Last Error" items. 
- [ ] vedrfolnir - resource, hardware and process information
  - providing information on resources, ports used, etc, a HWInfo for your vscode, if you will. List views of currently running processes, even background ones, provding info on resource usage Gauges displaying usages for cpu, memory, storage
- [ ] github tag navigator
  - simply a to provide a better ux to navigate between tags, branches, commites and etc
- [ ] prisma visualizer
  - visually maps relations
- [ ] devarchive
- [ ] remote resource management
- [ ] extened usage preview
- [ ] artifact cache mgr
  - A package manager cache available in any workspace   ├── Architecture  ├── projects.cache  ├── modules.cache  └── extensionStorage  └── node-modules-cache ├── react@18.2.0/ └── react@18.3.1/  hijacks install process scanning local registry and use local matches first before downloading any other libraries  installing them into the registry to be used in your project. places all new modules in ext  folder and registry. Once installation has been completed triggers background process to  scan all other projects leveraging the system and matching the registy with the current state of each projects package data, ensuring nothing gets stale and libraries that are no longer in use are removed from your file system
- [ ] faker ngin
  - Grabs your workspaces schema file and automatically  creates a file that generates data for all schema declarations that can be called in your seed file  Ensures that the automated mock data generation stays seperate from your projects code  instead of implementing it into it
- [ ] changelog ngin
- [ ] readme ngin

- [ ] backup to github
  - Saves a backup to a github repo that includes all workspace configs and your global config. I don't know why I thought of this  because its not really a necessity by any means. But more of an offsite  back up, to protect against unforeseen issues, like your computer failing. As of now, if that were to happen there is currently no means to restore your configs or anything else that pertains to this extension. Which is why I have already started and have plans to continue moving the storage of features to github such as the snippets. But again, this extension does not NEED this type of feature and is more of an insurance policy.
- [ ] Copy workspace folder
  - Provides a list of folders contained within other configs,  once clicked pastes it into the current configs file
- [ ] brokkr v2
- [ ] conditional config item
- [ ] dependency manager


- [ ] NEW TOOLS
  - [ ] messsenger
  - [ ] event calendar
  - [ ] appointment calendar
  - [ ] catalyst editor
  - [ ] rich text editor



---

[🡄 Return](https://github.com/8an3/DevStack)