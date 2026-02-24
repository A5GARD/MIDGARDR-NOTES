# DEV WORKSHOP

A growing number of ngins pulled out of the extension and exposed for your use. You get the same implementation that powers the extension itself — not a watered down version, not a wrapper around a wrapper. The actual thing.

> [!NOTE]
>
> As promised, here are the tools that a lot of people seem to have troubles or issues with in one form or another. Going over them for the remainder of this talking point, I'm sure I'm going to sound llike a pompoous ass hat, but theres no getting around that.
>
> Not only do I wish I had something like this to access, as it would have saved me from hours of headaches and what felt like the equivlant of my hand in waffle griddle while somone held it down. Because when it comes to features like these, if there are even docs out there... they suck, lets be real. I can't sit here and say microsofts strong point is their documentation and everyone should model themselves after them with the exemplary standard they set forth. lol, not to mention vscodes UNDOCUMENTED quirks, because those are always fun running into at which point your developing blindy. It's like poking a bear with blindfold on, but the bear will random swat back at you.
>
> If you have ever used anything I've built, I truly do hate setting limitations in any and all forms. Because of that, I've literally coded it in such a way that, it's as if its in your own code base. You all the benefits, with none of the negatives. You didn't have to figure it out, you don't have to maintain it, you don't have to think about updates, or adding features and all the testing that comes along with it.
>
> Essentially handing you the keys to the best examples that can be found on the marketplace in their given categories. I dont even know if any other dev has done something like this through a vscode extension.
>
> SO NOT ONLY, do you get prebuilt, pretested, and in some cases I intentiontlly hammered them and brought hell down on them essentially to get them to break and fix them if they do.
>
> That reminds me, jotting this down so I don't forget to actually add this to the workshop. The to do, reminders and notes back end implementation using github as a single source of truth. This is one feature... that I have... not held back in any way LOL, butttt it IS in a state that it never enters any thought process of what needs to be done, or looked out for. As you can, perfectly too keep that in mind, open to do lists, reminders and notes in one workspace. Open a new workspace, leaving the previous in a DIRTY state, because who needs the save feature. To THEN open them AGAIN, in the new workspace... because I don't want to tab over to use them in the previous window... do some edits, save... then open another workspace, while the first still have unsaved data. Close that workspace, to open another and again opening even more items in this workspace... editing them... leaving those unsaved too. To go back to the first workspace... see that I didn't save... save it finally and on and on the I carry out torturing a system a lot of people would be absolutely paranoid if this were happening. That was an EASY testing session. There have been times, I've done that times 3 in additiion to trying to open as many workspaces as I possibly can... just to try to break it. Now that I've thought about it I'll make sure that is also available shortly, because coding these features, were surprisngly quick. Everything is already built, I guess. 
>
> Oh, I failed to mention... My confidence being so high with that system, and going about it treating it like dirt with not a care in the world of whether the push to github was successful or not. Its use of github as a source of truth... well its not JUST a source of truth, as this feature doesn't even have a local copy to back up off of if something does go wrong... but it doesn't meanwhile, even lately, seeing devs talk about such features as if they're going to break as they talk about them and not interacting with them and going so far as creating recovery wizards as standard default functionality. If you have a friend like this... tell them to keep an eye out for it so they finally not stress about it and sigh in releif that, its taken care of.
>
> Not only getting the, now 4 features, but I have for a while now been coding the extension in a composable and as modular of a design as far as I can take it. Last I checked, this extension was exposing 2700+-3000+ functions. Now, a lot of those are due to the components library but even so, they are all in your grasp to do... whatever it is you want to do. As I abolutely hate whe people put walls, or guards up or anything in any resstrictive manner and impede you with what you want to do. Each feature, was originally built with that in mind and trying to bring that surface area to non-existant as much as I possibly could. While coding the exposure of these features, I can say... there is not a single restriction put in place. If that makes you uneasy, thats fine everyone can have their own opinion on any subject they want, with saying that... were devs, we will break shit, but the best thing about being a dev is after breaking it... we can fix it. 
>
> It's probably that mentality that helps me deal in areas, like not having the proper documentation in order to get something done and working. As I have no problem sitting there, coding away, prodding at it and trying to find a solution and make it work. It does not couple well with the fact that, I will not stop till it works the way I need / want it to, and even take a feature that I've spent days on... and just delete it to start over in order to get it where it needs to be.
>
> The current feature set you can access:
> - Context Ngin - every ui element is tracked which you have access to and it was coded so that you have full read / write access to do as you wish and even providing a couple of objects that... are 100% yours to add data in whatever amount you need to it
> - Workspace Context Ngin - Literally, the exact implementation that I use in this extension, yours free to do as you wish. This one being the only feature so far that I couldn't give straight access to due to the way its coded into the extension. When I built it... I never forsaw this being a feature that would end up becoming a reality. With saying that, it is a 1-1 clone. Every single function is the same, how it discerns workspaces between one another, how it merges the configs before the user get its data to work with in whatever capacity that you want
> - Terminal Ngin - Not only giving you direct access, but over time I've built myself some cheats and hacks to use it in all manner of ways accross the wide surface of this extension. Rebuilt them so that... you literally cannot make a mistake with them. The originals were built with that in mind, the oringinals... just looked ugly more than anything, since these functions are pieces of code I never thought would ever get shared
>
> The terminal ngin, while imo just as powerful as the context ngin, does offerr a lot more without having to think of anything too much. As you now have:
> - file
> - fileAtLine
> - url 
> - command 
> - powershellCommand
> - debianCommand
> - snippet
> - chain
> - concurrent, and because you are directly accessing the terminal ngin, you also get all the new recent nice updates it just got. Auto port ngin, env variables, the complete rewrite of concurrent and all the other goodies
> - copyValue
> - cmdChain
> - settingsToggle
> - apiCall
> - label
> - search
> - layout
> - folder
> - npmScripts
> - tasks
> - md
> - conditionalChain
> - wait
>
> Yes, you have progmatic access to the layout, you can even build your own version of it if you wanted.
>
> Shortly, there will also be a ngin for gitub as well. I'm sure I'll think of more, but these features being... I believe and hope to be the most impactful that could have been chosen out of the toy chest of features out of this extension. As I did think a lot about which features to expose and why one over another. It just weirdly happens to be the fact that, these features a lot of devs to find challenging to the point, that they loose interest in continuing with it. And it just so happens to be the strongest parts of my code, as each of the three are so ahead of the other marketplace offerings to the point where they are in a class all on their own and each of them would be the sole focus of an extension all on their own, if it were any other dev that built them. 
> 
> In addition to the exposed tools, I will also be making a guide for anyone interested in reading it. The portion will entirely be disucssing vscode, how it was built, how its underlying code functions, going into how and why every single blog is wrong when they discuss any one thing in terms of vscodes performance, and how you can improve your vscode today. 
> 
> Every single user encounters performance issues when using this software, and while yes just deleting the installed extensions will give some of that performance back... even though they state, that itself is the issue... it is not. I will be keeping in a lot of the material that was written previously as it goes into optimizing the settings vscode has in order not only get that performance back, but ensures moving forward you do not run into those issues ever again. 
> 
> For example, recently as I was testing Loki AI limitless and in order to conduct te testing as quickly as I could and across as big as a focus group that I could get my hands on, I ended up installing, it was well over 20 different ai extensions. Yes, it rendered my vscode instance to a grinding halt that... I could not do a single thing because of how each of these extensions sets their defaults. BUT, after optimzing them I was able to run all the ones that actually worked... all running at the same time, in addition to this extension along with whatever else I had installed at the time. So there was A LOT happening in terms of processes and even then my instance ran perfectly. No hiccups, no weirdness, but if it weren't for optimizing the settings... No computer would be able to handle that. While the original information is up and can be viewed, I haven't yet even went over it yet. Despite that fact, just learning how vscode is actually built and how to optimize it, will go a long way in terms of developing extenions as you will know what could or should be done or in some cases, what shouldn't be implemented in your code.

# devShop

Three engines pulled out of the extension and exposed for your use. You get the same implementation that powers the extension itself — not a watered down version, not a wrapper around a wrapper. The actual thing.

## Setup — Run In This Order

These three engines depend on each other. Initialize them in this exact order inside your extension's `activate` function:

```typescript
import * as vscode from 'vscode'

export async function activate(context: vscode.ExtensionContext) {
  const ext = vscode.extensions.getExtension('skyler.ocrmnav')
  const api = await ext.activate()

  const workspaceFolder = vscode.workspace.workspaceFolders?.[0]
  const workspaceRoot = workspaceFolder.uri.fsPath

  // 1. Workspace context first — resolves projectId and config layers
  const wsCtx = api.DevWorkspaceContextNgin.getInstance()
  await wsCtx.init(context, workspaceRoot)

  // 2. State manager second — needs projectId and workspaceRoot from step 1
  const devCtx = api.DevContextNgin.getInstance()
  await devCtx.init(context, workspaceRoot, userEmail, wsCtx.getProjectId())

  // 3. Terminal engine last — needs the fully resolved ctx object from the extension
  // ctx is the DevStackContext object provided by the extension at runtime
  const terminal = api.DevTerminalNgin.getInstance()
  terminal.init(ctx)

  // --- from here you have full access to all four engines ---

  // DevWorkspaceContextNgin — read the merged global + workspace config
  const config = wsCtx.get()
  console.log(config.categories)

  // DevContextNgin — read or write resolved VSCode state
  const editorState = devCtx.getState()
  console.log(editorState.colorTheme)

  // DevContextNgin — store anything you need globally
  devCtx.setStore('myExtensionKey', { initialized: true, version: '1.0.0' })

  // DevTerminalNgin — run a terminal command
  await terminal.run('npm install')
}
```

Your `package.json` needs this or the extension may not be activated before yours:

```json
"extensionDependencies": ["skyler.ocrmnav"]
```

---
