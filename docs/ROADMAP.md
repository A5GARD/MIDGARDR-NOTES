### <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="25"  style="vertical-align: middle; margin-bottom: 4px;"> **ROADMAP**



#### todo
- [x] need to fix context menu for notes
- [x] need to create add items functions for apiCall
- [x] need to create add items functions for settingsToggle
- [ ] recreate creation process for cmdChain, concurrent, chain via opening jsonc file and implementing a intellisense system to help with creating the new item type
- [x] need to create add items functions for search
- [x] need to test BE concurrent function
- [x] need to test BE sequential function
- [x] add new tools to drop down and devstack quickpick
- [x] need to create a section on how to benefit from the local / vs production database env toggle


- [ ] need to update snippet editor

- [ ] ### README.md

- [ ] ### Need to implement function on / off switches for:
- [ ] need to implement `ocrmnavigator.vfs.tasks`
- [ ] need to implement `ocrmnavigator.vfs.npmScripts`
- [ ] need to implement `ocrmnavigator.todoNotesReminders`
- [ ] need to implement `ocrmnavigator.codesnap.backgroundPalette` and others

- [ ] ### remote access / editing
- [ ] access to:
- [ ] config
- [ ] snippets
- [ ] todo, notes and reminders
- [ ] be able to download your config from anywhere
- [ ] set up user profile on site
- [ ] user github email for syncing data

- [ ] ### Copy workspace folder
- [ ] to make it even easier to configure new / existing configs
- [ ] provid a list of folders contained within other configs once clicked pastes it into the current configs file

- [ ] ### move item
- [ ] opens a quick pick with that folders items, when an item is clicked on it takes the item ur moving and places it ontop of the item you clicked on, same as when you go to cut an entire line in vscode and paste it, it places it ontop of the line you placed ur cursor on

- [ ] ### The "Log-to-Lens" (errorParser)
- [ ] The Pain: Your build failed or your test crashed. The terminal is a wall of 500 lines of red text. You have to scroll up, find the file path in the stack trace, copy it, Ctrl+P, and paste the path to fix the bug.
- [ ] The Fix: An extractFileFromOutput type.
- [ ] How it works: It scans the last output of the integrated terminal for file paths and line numbers. It then populates the Navigator with "Jump to Last Error" items.
- [ ] Time Saved: 90%. You click the Navigator item instead of manually parsing the terminal's "wall of text."

- [ ] #### conditionalChain: Logic-based execution. 
- [ ] Utility: Run Command A; if it succeeds, run Command B; if it fails, run Command C. (This adds a "Scripting" layer to the NavigatorItem).

- [ ] #### The "Proxy/Tunnel" Toggle (portManager)
- [ ] The Pain: You’re working on a mobile app or an external API that needs to see your local server. You have to open a separate terminal, remember your ngrok or localtonet command, copy the new URL, and paste it into your config.
- [ ] Value: It automates the "copy-paste" loop between the terminal and your code.
- [ ] The Workflow: A specialized command that launches a tunnel (like ngrok http 3000), captures the generated URL, and automatically updates a specific line in your config.ts or .env with the new public URL.
- [ ] The Fix: A tunnelLauncher type.


#### feature request quick pick
- [ ] query current user base via a toast on load up, once clicked opens a vscode quick pick with current feautres to pick, once they select a value they are then presented an input to supply their own feature request

#### ideas that are a 'meh', need to mull these over

##### The "API Secret Grabber" (vaultFetch)
- [ ] The Pain: You need a staging/prod API key that isn't in your local .env for security reasons. You have to log into AWS Secrets Manager, 1Password, or your company Wiki, find the key, and copy it.
- [ ] The Fix: A type that fetches a value from a CLI-based vault (like gh secret, aws secretsmanager, or a local encrypted file).
- [ ] How it works: It executes the CLI fetch and uses your existing copyToClipboard logic to put the secret in your hand instantly.
- [ ] Value: Huge security and speed boost. No more "hunting for the wiki page."


#### item type ideas???
- [ ] dependencyManager 
- [ ] Install/uninstall/update multiple npm packages in one click with predefined sets (ie "React setup" installs react, react-dom, types in one go vs typing each npm install command)
 
#### focusMode: A specialized toggle.Utility: Toggles Zen Mode, hides the Sidebar, and hides the Activity Bar all in one click to help with deep work
 
#### fix add item via web 

#### VISUALIZE SCHEMA OBJECT - start from scratch and build it on the browser side
- [ ] within the web app, build a schema wizard. I find that as the schema / project continues to build and expanded on I'm constantly jumping back and forth, from object to object, grabing the value to link to another object, then going back ensuring everything was done right, then triple checking. All the while, your bouncing down 450 lines, then back up 450, then down 550, shit went to far... searching for it again, saying under my breath, where the fuck did it just go... lol
- [ ] whenever working with an object, have a + relation button, when clicked opens a command to search and select a object to link to
- [ ] being able to insert pre built objects
- [ ] with nice, thought-out and planned ui, would make it so easy to work with, like having a command on the left to search for or select the object to edit, this object should be linked, so editing the user object needing to add that relation, technically, you can remove half that processes work laod. Steps to complete would be: 1) select user object, 2) click add relation, and select review object

#### new tools
- [ ] messsenger
- [ ] event calendar
- [ ] appointment calendar
- [ ] catalyst editor
- [ ] rich text editor


- [ ] DevArchive
- [ ] I’ve noticed a disturbing trend: the "Great Deleting." The people who built the web are retiring or passing on, and their servers are going dark. I’ve lost count of how many times I’ve needed a specific resource only to find the site no longer exists.

- [ ] I’m building DevArchive because I’m tired of watching knowledge disappear. I’m building it for myself, but I’m opening it to everyone.

- [ ] The "Hit by a Bus" Philosophy Most platforms require constant human intervention. DevArchive is different. It is being built to require virtually zero man-hours to maintain. Whether I get sick for a year or pass the torch 50 years from now, this system is designed to be a self-sustaining utility, not a chore for the next person.

- [ ] What it is: A home for your code, your docs, and your research. What it isn't: A host for images or video (the costs are simply too high for now).

- [ ] This is a place where data survives. Whether you want to share your knowledge with the world or keep it private, you can finally rely on the "Save" button again.


- [x] last stable version 351
- [x] add global settings file opener in quick pick
- [x] need to add md pre-processor to readme
- [x] convert node .js scripts over to extension functions allowing other workspaces the same functionality

- [ ] TO-DO
  - [x] when logging in if the user is different then the current user in indexed reset all datqa
  - [x] changed createNote in configureAction to return note instead of redirect
  - [x] if (isTrashed) { return json({success: false, message: 'Note is in trash'}) }
  - [x] merge with devstack
  - [x] i wantimplement a queue system for rapid line item pushes. instead of cancelling subsequent operations, enqueue each push request and process them sequentially in FIFO order, with each waiting for the previous operation to complete before executing




---

[🡄 Return](https://github.com/8an3/DevStack)