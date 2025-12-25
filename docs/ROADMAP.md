### <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="25"  style="vertical-align: middle; margin-bottom: 4px;"> **ROADMAP**

### Upcoming 

Items listed below will also contain upcoming features for the ui library

- need to implement `ocrmnavigator.vfs.tasks`
- need to implement `ocrmnavigator.vfs.npmScripts`
- need to implement `ocrmnavigator.todoNotesReminders`
- need to implement `ocrmnavigator.codesnap.backgroundPalette` and others

- need to update snippet editor

### remote access
- be able to download your config from anywhere
- set up user profile on site

### Copy workspace folder
- to make it even easier to configure new / existing configs
- provid a list of folders contained within other configs once clicked pastes it into the current configs file

### move 
opens a quick pick with that folders items, when an item is clicked on it takes the item ur moving and places it ontop of the item you clicked on, same as when you go to cut an entire line in vscode and paste it, it places it ontop of the line you placed ur cursor on

### The "Log-to-Lens" (errorParser)
- The Pain: Your build failed or your test crashed. The terminal is a wall of 500 lines of red text. You have to scroll up, find the file path in the stack trace, copy it, Ctrl+P, and paste the path to fix the bug.
- The Fix: An extractFileFromOutput type.
- How it works: It scans the last output of the integrated terminal for file paths and line numbers. It then populates the Navigator with "Jump to Last Error" items.
- Time Saved: 90%. You click the Navigator item instead of manually parsing the terminal's "wall of text."

#### conditionalChain: Logic-based execution. 
- Utility: Run Command A; if it succeeds, run Command B; if it fails, run Command C. (This adds a "Scripting" layer to the NavigatorItem).

#### The "Proxy/Tunnel" Toggle (portManager)
- The Pain: You’re working on a mobile app or an external API that needs to see your local server. You have to open a separate terminal, remember your ngrok or localtonet command, copy the new URL, and paste it into your config.
- The Fix: A tunnelLauncher type.
- The Workflow: A specialized command that launches a tunnel (like ngrok http 3000), captures the generated URL, and automatically updates a specific line in your config.ts or .env with the new public URL.
- Value: It automates the "copy-paste" loop between the terminal and your code.

#### feature request quick pick
- query current user base via a toast on load up, once clicked opens a vscode quick pick with current feautres to pick, once they select a value they are then presented an input to supply their own feature request

#### ideas that are a 'meh', need to mull these over

##### The "API Secret Grabber" (vaultFetch)
- The Pain: You need a staging/prod API key that isn't in your local .env for security reasons. You have to log into AWS Secrets Manager, 1Password, or your company Wiki, find the key, and copy it.
- The Fix: A type that fetches a value from a CLI-based vault (like gh secret, aws secretsmanager, or a local encrypted file).
- How it works: It executes the CLI fetch and uses your existing copyToClipboard logic to put the secret in your hand instantly.
- Value: Huge security and speed boost. No more "hunting for the wiki page."


#### todo
- [x] need to fix context menu for notes
- [ ] need to create add items functions for apiCall
- [ ] need to create add items functions for settingsToggle
- [ ] need to create add items functions for search
- [ ] need to test BE concurrent function
- [ ] need to test BE sequential function
- [x] add new tools to drop down and devstack quickpick
- [x] need to create a section on how to benefit from the local / vs production database env toggle


#### item type ideas???
  - [ ] dependencyManager - Install/uninstall/update multiple npm packages in one click with predefined sets (ie "React setup" installs react, react-dom, types in one go vs typing each npm install command)
 
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


#### DevArchive
As time continues to go on, we are reaching a point in time where a large number of costodians of information are about to commit an act of the largest removal of data / informtation this planet has ever seen. A lot of the people who started either, slightly earlier or getting in when everyone else did in the dot com boom, are coming to an age in which they no longer desire to maintain or host their webservers holding that data, or sadly they are starting to pass away. 
Personally, I have seen it grow in frequency of late. X problem comes up where I need said resource to follow the process laid out in order to overcome that issue. Only to find out that that site no longer exists. 
This entire event that will come to pass, was the main selling point back when everyone was getting on the hype train of the dot com boom. No longer is data on paper they said, infomrmation wil be faster than ever... Back then, I honestly didn't have opinion on that specific matter or cared enough to even think about it. It's not because I'm older, its because I value information and knowledge a lot more than I used to.

Currently there IS a hole as far as offerings go, like what do I do with this data, how do I store, how would I access it, if I were to choose x to go with are they going to be around for a while? I'm a huge fan of sharing knowledge, and I can't be the only person with this issue. Even though, I'm primarily building it for myself if theres anyone who wishes to also use it, your more than welcome. 

It will be built in a way where there will be virtually 0 maintenance in regards to man hours in taking care of it. SOLELY due to the fact that, lets say 20, 30, or 100,000 people end up using this. If I die one day, or absolutely have to pass it off to someone. IT CANNOT be in a state where it's a burden on whoever it gets past onto in 50 years. 
At the same time this way of thinking will solve a plethora of other issues as well, ie what if I get sick for a year... or get hit by a bus and can't type for the next 12 months. Who takes care of it then? If you asked yourself the same questions I did, rest assured this will not be going anywhere.

But anyways... DevArchive will be a storage provider for all things data for not just in the respect of a daily resource in which you visit it everyday, ie the place you keep resources for to solve problems bookmarks, code snippets, pdfs and so on. It will also provide storage of almost anything you need except image and video. Strictly due to cost. If this were to generate money down the road and be able to maintain itself in terms of storage costs by generating enough income to take care of itself. This is something I would defeiantly revert on.

In summary, a place where you can store data, share data or even just keep your data private to yourself. This will be something you can rely on



[🡄 Return](../README.md)