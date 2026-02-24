> [!IMPORTANT]
>
> Any time you see a feature mentioning finding it among the status bar menus, this has recently been changed as all status bar menus have been moved into the activity bar. If it is not apparent as to which activity bar view it currently resides in, then it will be covered under the devstack menu sidebar. As this has been the single point of focus when consolidating and exposing all of vscodes features as well as hosting as a menu system for this extensions features.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Quick Setup (2 minutes)
   
### Step 1 Restart VS Code
After installation, restart VS Code to apply layout configurations.
   
### Step 2 Clean Up Activity Bar
Right-click the Activity Bar and uncheck these default items:
   - Explorer
   - Search
   - Source Control
   - Run and Debug
   - Extensions
   
### Step 3 You're Done!
All features are still available - just in better places.

***In terms of removing the extensions icon, there is no replacement for this exactly. The only reason I have removed it personally is due to the fact that whenever I have a situation where an extension could help me with coding, instead of searching the marketplace for a solution, I simply just build it myself. So for this item, you may leave in the activity bar if you would like.***

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Setup

This extension has become so large and massive, I would have never guessed it would be where it is today, or where it will get to tomorrow. 

I have tried to make the onboarding experience as best as I can, and only falling short in a couple of areas due to vscodes restrictions, for example I have included a base layout configuration that is included with the workspace config. This allows for a much easier process for you to set up workspace context layouts. If you do not wish to use this feature, just remove the layout config item from your workspace config. 

Even though, the experience and UI will change for you, I have coded it so that items like your desired registered theme, font size, word wrapping, breadcrumbs, and more will carry over into the layout config item that gets generated for each workspace you create. Which means, yes a lot will change, but not for configurations you love and enjoy that do not need be overwritten. If you have already installed the extension, but not yet restarted your instance the layout config has already been created for you and I would ask for you at this time, to restart the vscode instance.

If your worried about loosing your place here, as soon as you restart the intance there is an oboarding page that will pop up when your vscode instance loads up that can be toggled off or even kept on if you desire.

Once loaded back into vscode, you will see there is a lot going on in a lot of different places. The UI as a whole, but to make the experience better I will go over a couple of changes that need to be done manually to finalize the process.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> The Activity Bar

Situated to the left of the window ( depending on your settings but this is the default location ), currently this will have exploded with new items for you and need to remove the default vscode features. We are just removing the icons, not the actual feature so in the case that you actually would rather use the vscode variant, your more than welcome to remove the extensions icon and replace with vscodes. Or in the case of developing new features, if something were to break later down the road, for example a new feature was added to the search but happened to break other features, till it is fixed you can easily swap out search engines.

This process is very simple despite the amount of new items you have, as all you need to do is toggle off every single vscode feature making it so the only remaining items are provided from this extension. 

Before moving on, yes there are a couple of features you will notice that aren't among the icons in the activity bar. Do not worry, trust me, they have actually been replaced but just reside else where while at the same time offering a better ux than the default.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Before / After

### Before 
<img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/ui/vanilla.png"   style="vertical-align: middle; horizontal-align: middle;">

### After
<img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/ui/extension.png"   style="vertical-align: middle; horizontal-align: middle;">

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Default Configs

When you first install the extension, you will have a choice of selecting configs consisting of examples and configs consisting of a single folder.

If this is your first time using the extension I suggest the option containing examples as if gives a wide range of what can be accomplished with all the many different config types that include:
- examples of each config item
- examples showacase extended use of its config item type
- how to include env variables with config items
- how to create and use hidden item types
- and much more...

Even if you do not plan on editing the config itself, and only use the ui elements to add, edit or remove items. They will still provide value on what exactly you can include with each config item.

The workspace default config, while limited in terms of examples provided it does come with a layout config item to allow for a much easier and faster workspace context layout configuration. Which we will expand upon later on in the docs.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> To Get The Most Out Of This Extension

Or in other terms, hit the ground running. The best way to go over the documentation is to go over the terminal ngin and its config items, and the layout ngin.

The config items that are used in devstacks sidebar are still by far the most powerfull feature that can be found in the extension. But its power is built over time as you build your config, as config items are built as you need them when coding. 

Where as, that layout ngin is just one config item and you get immediate gratification of an entire new vscode expereience that can't get from any other extension, seriously.

Then using the rest the features as you would vscodes features, they are there waiting to be used and will be available to you when the need arises. At that time, come back to the docs and refer to its section learn about it. 

Currently the docs sit over 72+ files and that isn't even including the long list of features I had put off on documenting or forgot to come back to. So this list will grow and it would be stupid for someone to sit there and read all of the docs in one setting. 

This strategy not only gives you that wow factor, or instant gratification of, "shit this extension is cool". While it also sets you perfectly down the correct path in getting the most out of the config items.

<!-- #region --->

> [!TIP]
>
> I mentioned this in the readme, but lets talk about your VSCodes performance and if you opt in to taking the suggestions laid out, I promise you this will be the single most largest improvement to your applications performance you have ever seen. As I had noticed that, even till today, these changes were and are still the biggest gains I have ever gotten when optimizing the application for performance.
>
> These will include features that I know there will be people that just... cannot live without them. Which is why this is being presented as a tip and a suggested path to take since I didn't think it would be the most friendliest of things to do without informing them.
>
> LETs GET THE MOST HUNGRY, MEMORY STARVING GLUTTON OUT OF THE WAY FIRST THAT PLAGUES EVERY SINGLE VSCODE INSTANCE... GitHub.
>
> Yes, I know... Literally everyone uses it to the point that it was integrated into vscode a default feature. But, lets be real... You do not need the functionality it offers, no one does. It sits there constantly hammering your systems performance, for what? A notification in the activity bar telling you how many files are dirty in comparison to your repo? I disabled it over 6 months ago, not only have I NOT missed it, I haven't... even really thought about it. Which is GREAT, because that means it offered nothing I couldn't live without. 
>
> Before we move on to the how, lets go over the why. In terms of why you NEED to get rid of it and what I have done to ensure... you not only don't even miss having it, you'll be wondering why you didn't do this sooner, as it seriously gives that much performance back to you.
>
> As you code, every single key stroke you make... github reacts, and then does all sorts of manner of things behind the scenes without you even know. Not to mention, in addtion to horribly running as a background process, it does its job incredily ineffeciently at the same time. Why do you need to index 1000's of files, that I have't open in weeks. Even going so far as not even opening the root parent directory, so why are you scanning my remote repo... to compare against those files? 
>
> If you work in larger projects, the second you disable github... you will feel like you can finally breath since the elephant that was sitting on your chest finally was shoved off. Actually, that's the way it felt for me. As that one settting turned a slugish vscode instance, into a snappy and responsive editor again. Making me disable it everywhere, across the board... immediatly.
>
> If you want to get into the really nerdy details and go down the rabbit hole to learn more. I just recovered a vscode extension archecture breakdown that goes over all manner of things of vscode and the technical side of why it does what it does, that goes against industry wide beleif of why and how to fix the performance issues. That's is the first topic covered in the vscode extension building guide, if you are on the fence about reading it, go read it. As it will be the best resource and a view at vscodes internals that you cannot find anywhere else, since 99% of the information that is out there... is wrong.
>
> Anyways, if your sitting there panicking wondering how your going to live without github. Rest assured, not only do I have a solution for you it is a far better ux than anything that deals with github currently.
>
> It took me longer than expected but I got there, to where I was so fed up and annoyed with github that I was going to create a wrapper for it. It's not because I don't know how to use github, I've built the entire backends of multiple projects to use github as a source of truth... which is a very difficult task for 95% of devs out there, not to mention getting it done right so you never have to deal with an error message... ever.
>
> I forget which command sequence exactly, but I just remember looking at it saying, "fuck that man, why do they have to make it... so stupidly and needlessly complicated", and heres the proof of that.
>
> The end result being a github cli wrapper, that is integrated in your new ui, situated in one of the new sidebar views that you currently have. The valknut, or in other words the same icon that is used as the red section indicator in all the markdown docs, the sidebar is labeled HEIMDALLR, vigilant guardian of the Aesir who watches over Asgard from his dwelling, Himinbjörg. Known for his superhuman senses, he can hear wool growing on sheep and see hundreds of miles. 
>
> Upon opening that sidebar you will be greeted with a file tree view containing 4 folders:
> - BIFROST - The platform agnostic installer that uses a lot of the same functions HEIMDALLR has, which you will see why shortly
> - BALDR Icons - triggering that file item activates the installation process for that react icon library. 
> - MIDGARDR SDK UI Components CLI Tool... but instead of using the cli, you have nice and easy items to click on in place of typing out terminal commands that require you to go to the docs every time you need to use it
> - last but not least, HEIMDALLR
>
> Created with a very specific mindset and strict goals and requirements to adhere to when it was being built such as:
> - replace githubs naming convention, in its entirety as it truly makes no sense while at the same time the names that are used hold absolutely zero meaning to the functionality they are relevant to in addition to holding zero significant previoous experience or knowledge to go off of in order for a user to quickly come to the conclusion of what each function might do when used
> - replace every single command sequence... literally throw them all in the garbage so we never have to look at or use them again so much so that you forget entirely on how to use the cli, thankfully... I'm almost at that point where if I ever have to use it again, I will have to look up every single command
> - a strict no exception requirement: every single operation has to be completed with a single command... or click as this did start off as a npm library but thought better of it and just merged it into devstack. Which means the halarity of command required command acrobatics needed to do any one thing... is a thing of the past so no more:
>     - git add * .--
>     - git commit blah blah
>     - and so on and so forth
> Just to sync your remote to your local... like cmon.
> Even worse is the fucking create project command sequence, making you not only use the terminal, but actually making you leave your vscode instance, navigate to the site, come back and then play window tab tag in order to copy all the relevant information that is required in order to move forward with the process. 
>
> So with this github wrapper, what do you need to do in order to create a project now? 
> 
> Well to begin with a running start in comparison to the sluggish start that default process will be taking its a single click of the file item labeled "create project"... man that naming convention was fucking tuff, ehh? Almost missed the mark on that one too.... lol, I can only laugh at that. It's so bad, that it takes the average user a rediclously long time to learn a simple process. Then making it even harder for users with even more confusing commands. 
>
> Anyways, this starts project wizard as it will guide in IN VSCODE on what values to provide in order to create the project locally. Once you have supplied the required values... that is it. It does everything for you. The end result being, you have a folder with a project started on your computer... and you have a backup of it on some dudes computer in the clouds with the first push already done for you. This not only reduces the surface area of mistakes that could be made, but its simple. It will prompt for the following values:
> - project name
> - project description to be included in your package.json
> - which package manager you would like to use
> - which license you would like to have included in your project, from the get go
> - its not updated in the docs, but I have since added a changelog template wizard and readme template wizard as well
> - asks if you woud like to install the icons library once your new project has intialized
> - also asks about the ui components library ( which also installs and configures tailwind for you )
> - finishing off with asking if you would like to have the installation process done for you
>
> I did purposly fail to mention a few things, because compared to what github requires you to do we sprinted across the finish line and didn't want to rub it in harder then we needed to, BUT WAIT, THERES MORE!
>
> I automate as much as I can everywhere possible so there will obviously be functions happening during this process:
> so much more I have to pull up the code just to... I'm an idiot but super smart at the same time. For each menu option, there is a hoverable markdown preview where I included the ENTIRE docuemntion for each and every single item. Just so you or I, or anyone else has to waste time digging through documentation looking for things.
> - sility create the new project folder for you
> - cd into the project 
> - create readme
> - license
> - package.json
> - .env and .dev.env ( more on that later )
> - .gitignore, with a base config to ensure that you never include the neccesities any push to your remote moving forward
> - instailize github project locally
> - creates the remote repo
> - adds, commits and all other manner of commands to finalzie the creation of your new repo remotely
> - creates asgard.config with the provided values to be used in the future
> - if you did opt in for pre installing the UI library it not only installs the required libraries, tailwind, postcss, creates the required config files for you, but in place of using some boring default config for tailwind. You will happily learn that it instead provides the tailwind config preset ngin, that allows you to control not only your apps theme, with like 75+ themes to choose from, but also providing 110+ fonts and finally allowing you to customize the apps presets which controls the overall feel and look of your entire app by changing the padding, margins, borders and more across your entire application
>
> What do you need to do in order to benefit from the tailwind ngin? Opening your new tailwind.config.ts, you will very quickly notice that there is a terminal menu style UI that will greet you when you open the file. Each section outlines what options are available for you to choose from, along with very conveiently allowing you to set its relevant value within the same menu section as well. Thus, you never even have to look at the working source code, and by changing 3 simple variables at the top of the file, you have 40,060 configurable combinations to choose from. 
>
> SO, in summary... we all know what githubs process entails and the depressing state of affairs we end up with...
>
> HEIMDALLR, in comparison leaves you stranded with a project that is set up currently with :
> - readme, license and changelog files are not only created for you, but somewhat prefilled with a template to go off of so you never have to scour the web for an example to base yours off of
> - your package.json, also somewhat filled out for you.
> - all of the required commands needed to ensure that your remote repo is set up correctly, is done for you
> - you apps node_modules have already been installed
> - tailwind is already configured and ready to go
> - post css is in the same state of affairs
> - you already have a icons library installed
> - and finally instead of having to resort to some UI libraries website to re-read their documention on how to install the components... you didn't even have to open a browser and you will have roughly 125+ components in your apps file structure
> - BUT WAIT... THERES MORE!! whenever you opt into installing the UI library during the create project wizard, it goes out of its way to make your life even easier. By configuring your app so that whenever you go to import a component and or icon, configures the import statement so that its not only easier to type out, but also more memorable due to the fact that... there is only one single path that imports EVERYTHING found in the library, including all 2800+ components. For icons the import path is '#baldr' and components '#midgardr'
> - BUT WAIT... THERES MORE!!! lol, once your project is initialized, packages are installed and everything is ready to go. Instead of making you close that vscode window only to have to manually open the new workspace like some kind of muggle. It automatically saves all editors in that vscode instance, closes that instance and opens a new instance inside your new workspace... all automatically for you so you do not have to lift a finger.
>
> Tada... you are now presented your new project, with a remote repo in your newly created vscode instance that is in your new workspace.
>
> Every single command sequence from github is now... that easy.
>
> Forever gone are the terms like stash... I don't even remember them anymore, lol, checkout, stage changes, poping this, dropping that, tagging it... Rebase branch... like what? I've built entire back ends that perfectly use github with 0 errors... and at this point I actually have forgotten the terminalogy, and re-reading them again now... like what the fuck does any of the names have to do with its functionality? How is a stage relevant to anything that has to do with github? Checkout, did we go shopping? I don't remember grabbing a shopping cart, apparently we did though because it is a clickable option. Show github output... no, why don't you just work well enough that you do not need to provide that as a default menu option.
>
> Speaking of which, for the devs that are already paranoid about commands erroring out and not finalizing your most recent push.
>
> The command sequence that has been implemented was very specifically engineered in a way that each and every single push will be succesful. To further put your mind at ease I will walk through that process.
>
> Across the entire implementation, there are specific checks that are required to be met. If any one of them are not met, the accompanying wizard will step in to save the day and help you by fixing whatever it is you are missing. For example, if you would rather create a project via a config file instead of the prompting wizard, you more then welcome to do so. If a value is missing that is needed, the wizard pops in prompts you for the value, and send you on your way for a successful project launch.
>
> The next process is multi-beneficial... or multi functional, where the majority of the functions start a github process before the desired function is even triggered. Using a real example that you will use a lot, Upload +. If you look at the menu options there are four different upload variants, the standard plainly pushes the repo, while the other also update your projects version / tag in the same process, turning a 6-8 command sequence to a single click. Each upload process goes as follows:
> - workbench action files saveFiles - saves all currently open editors in your workspace to ensure all of your local files are clean from a workspace context. This also serves several other functionality requirements, that aren't as well known. Almost every single function in this extension triggers the save all feature for vscode. As this help vscodes in app versioning and history of your apps files system. Thus will provide a much better chance at recovering any lost data, in whatever event that happened that made you loose it. There are 2 ways ways that you can recover files using vscodes features. BUT I have already included a much easier, less painful and more readily available solution that can be found in your sidebar that uses the same triggers as vscodes implementations. You can review the files to find the one you need, right clicking you can either re-create the file or copy its contents to your clipboard.
> - it then checks to see if you currently have a config.asgard file in your project, if not it starts the wizard OR if you are missing any details, it still goes through the same wizard technically but each step in the wizard does a series of checks to see if you have the value it is about to prompt for and if so, skips it and moves on. 
> - it then retreives your github access token, checking in two places: 
>     - the first being, vscodes secrets context storage system
>     - if there isn't one saved at that location, it then scans your .env file for 'GITHUB_TOKEN' 
> - once it has required your token, it then checks to see if the stated repo, actually exists before proceeding
> - if this were any other function, meaning not a sync function itself this would be the step where that function first checks your config, checks the repo and finally syncing before moving on. Syncing with te following commands:
>     - git add -A -- .
>     - git commit -m "Auto-sync: ${new Date()}"
>     - git pull --tags
>     - git push
> This sequence ensures that... before you even push your local up to your remote repo, both projects file system states... are matching and because it does this for every single function, BEFORE the actual functions is triggered ensures that you will always be in a state where both your remote and local will never have to deal with an failed push since you will always be progmatically taken care of no matter what you do... or don't do, as the not doing of a lot of diffrent github things will eventually make it so that you will have to deal with that failed push.
> - next, everything that isnt a sync runs the desired fucntion, meanwhile the upload + we triggered will scan to see which package manager you opted for, first by checking your config, if you failed to include that fail it then checks your file system to see which lock file currently resides in your workspaceRoot using the appropriate terminal command.
> - git push
> - git push --tags
>
> To push your new tags to your remote. In the 9 or so months, in which the to do feature in this extension uses github as a single source of truth, I have no encountered a single error while absolutely hammering that feature across several instances at once WHILE, some instances have unsaved lists open. 
> 
> Meanwhile I open them in other workspaces to edit and save them... Never revealed this before in the docs, but it works SO WELL that, there isn't a locally available copy to fall back on... if one of the github command sequences were to fail, I'm THAT confident in it, so much so I don't even think of that feature saving the way it does as you will not experience a versioning mismatch between instances, failed pushes due to git HEADS not doing...whatever it is that heads do to compare...heads? 
>
> Finishing this off by going over the remaining naming conventions... if you haven't taken a second and looked at the other names. Just for fun... stop for a couple of minutes and read the names that have been implemented and guess as to which does which.
>
> Each name that was chosen was carefully looked at, compared, broken down to ensure that each of the names hold not only a previously indoctirned meaning that defines that work for each person... but ensuring that each endocturned meaning is relevant to its coresponding functionality. Which means, someone in the first week of coding can actually succesufully guess what each name represents.
>
> - project - is your local repo so anytime project is referenced its refering to the local representation of your remote repo
> - source - refers to your remote, as it is the source of your project
> - timeline - is your branch, timeline was chosen because whether you are new or not timeline immediatly tells someone that it can be temparay, can be deleted or can become the final project 
> - version - replacing tags, this name immediatly conveys a versioning system where as tags... simply does not
>
> I'll admit it will feel weird at first, but you will get used to it pretty quickly, as I don't even have source control on my activity bar anymore.
>
> SO, hopefully I was able to ease your mind in that regard before giving you the values to completely disable github in your vscode application. I'll provide two sets of values for you to choose from, the first being "taking it slow" approch with just disabling github at the time. The second option will be placed in an accordian below as it will contain my settings values that I have manicured and spent hours on to the point now... all the large projects that once gave me troubles... run so smoothly its no longer a concern.
>
> With saying that, it probably helps that the only extension I run is devstack, aside from the base extension everyone and their mum installs such as:
> - prettier
> - prisma
>
> While I do have othere installed, every other extension is disabled, but just for transparency that list includes:
> - AI Assistant by jetbrains - I dont think I've ever actually used this one
> - batch rename - becasuse I forgot to uninstall it at some point which I'll do now
> - CodeGeeX - AI Coding Assistant
> - gemini code assist
> - github co-pilot - I really need to figure out how I can uninstall this without vscode loosing its mind. Every time I have gone to uninstall it, it freaks out. Even if it's out of date, it just sits there and complains about life even though, it doesn't get used nevermind the fact that it's disabled
> - markdown tree, whatever that is
> - open wsl support
> - sqlite
> - tauri - which i just uninstalled
>
> Just uninstalled virtually everything, copilot already freaking out lol. 
>
> While on the topic of AI Coding memory pig assistants. These are far worse for your performance than github ever was, BUT not all is lost in terms of AI as with a couple of simple configurations you can tame these performance hogs to a much more reasonable state. 
> 
> When I was running tests against the loki ai limitless, I installed every possible solution that was in the marketplace and available for download. While... when they first loaded, brought my vscode instance to an absolute halt as each assistant was not only scanning the entire file system in its entirety, but also has watchers in place waiting for any incoming event, while also hovering over all of your open editors waiting for you to press a single key, then it excitedly freaks out and does things which tank your performance. ONCE, I had configured them all I was actively running 16 different ai's in my single instance at once, absolutely hammering every single one of them, all at once. So while they come pre configured to ruin your day, they are simple to stop. Simnply open the extensions settings, they ALL have these options to configure,.. Aa if it is making enable one of them to view the settings... and already its doing things I don't want or need. Lol, as if I needed to enable it to see the settings, anyways... 
>
> - whatever you do, do not enable yolo mode, that is just irresponsible on the devs behalf
> - code generation pane view enabled - nope, don't need that
> - enable the use of .gitignore so that you can configure what it can and can't scan - yes enable this, as simply just enabling this will lock it out of node_modules at the very least
> - display inline context hint - no
> - enable telemtry - no, so much so you shouldn't enable this across the board for any extension
> - inline suggestions: enable auto - no thank you, we do not need a perverted ai micro managing every key stroke we make
> - local codebase awarenesss - sigh, no
> - outlines: automatic outline generation - no, lol
> - inline suggestions: next edit predictions - if you want to yolo your performance right into the dumpster fire that will become your workstation, this is something you would want. That must be a new setting, I was joking do not enable this
>
> Or if you would rather deal with the settings file, instead I'll place gemeni's settings. No maatter which engine you install, the settings you WANT disabled are basically all named the same and this will serve as a reference on what to look for among the intellisense options  
> 
> Simply any and all anything having to do with inline suggestions, auto scanning of files no matter what term they coined and try to use in order to trick you into enabling it, anything with the word automatic, or suggestion, telemetry, auto or enable auto, disable all of these. The end result being an AI assistant that is reactive instead of letting it run around like a 3 year old with a sugar high. 
>
> In terms of extensions, keep whatever extension you may have for the mean time, till you get antiquated with the features that are provided through this one. It does, actually, cover the same feature set from 150+ extensions so it should replace virtually any and all extensions. Even themes, as you now have 125+ registered themes, product icon theme, file icon theme... and a ton more features to use
>
> Between removing all unneeded and or redundant extensions, removing github, taming the ai's your vscode instance should be in a different realm of performance levels compared to what it was just at. 
>
> If you do work in large projects I'll leave more settings for you to help you out below, other than that I hope you enjoy. I'm working on the docuemntation again, as currently it is not in a good state since so much has to be replaced as well as it seems I lost some in the latest docuemntation conversion. Even so, each function you will find was created in a way that for 95% of the features that you can use, don't even need documentation in order to use. For example, opeing the editors context menu by right clicking any file, opening the shadcn submenu, it is very apparent as to what each option does with just a cursory glance. The same for open github at file, while there is documentation for it, it's not really needed. Any feature that is more complicated in nature, does have docs associated to it but the docs will be completly re-written, I've just been holding off on it because it entails... writing docuemntation for 150+ extensions. How is that ai still active after completely uninstalling it, and restarting the instance...
>
> Cheers
>

<!-- #endregion --->

```json
{
    "geminicodeassist.displayInlineContextHint": false,
    "geminicodeassist.enableTelemetry": false,
    "geminicodeassist.inlineSuggestions.enableAuto": false,
    "geminicodeassist.localCodebaseAwareness": false,
}
```
> [!TIP]
>
> If your aren't used to navigating to the 2 places that the settings files are placed, instead of navigating the maze of file explorers, a cheat is already in place for you to take advantage of. In the sidebar, open the devstack menu, you will be presented with a long list of buttons to click. Each section is categorically organized, VSCode Config folder, by deafult, should already be expanded granting viewable access to both available options for workspace and the more annoying sibling to navigate to your global setttings file. I suggest using the global settings file, as there are a surprising amount of settings that can only be set in the global file. Basically the workspace file is for a custom theme, and any workspace specific settings, otherwise using the global over the workspace is more advantageous in the long run.
>
> I will go over each of the settings so that you can determine if loosing that feature will be worth while to keep, as going down this path we look at settings slightly differently. As the number one priority is performance in-place of total feature count. Really, it's a game of, can you live without it and there are a surprisingly large amount of features that yes... you can infact live without.
>
> I'll leave my settings as they are currently configured, because I'm surprised as to how many I have left enabled because I stopped disabling features once the vscode instance returned to a state that I expect it should be in.
>
> The only thing residing in my workspace settings are extension settings, and themes that are automatically placed in the workspace config by the layout ngin, but due to the sheer size of json schemas object and the file nesting configuration, I have removed these so as not make you scroll needlessly everywhere.

```json
{
    "css.validate": false,
    "diffEditor.codeLens": false,
    "debug.openDebug": "neverOpen",
    "debug.toolBarLocation": "hidden",
    "debug.showInStatusBar": "never",
    "editor.inlineSuggest.enabled": false,
    "workbench.editor.enablePreviewFromQuickOpen": false,
    "editor.inlayHints.enabled": "off",
    "editor.parameterHints.enabled": false,
    "editor.suggestOnTriggerCharacters": false,
    "editor.acceptSuggestionOnEnter": "off",
    "editor.acceptSuggestionOnCommitCharacter": false,
    "editor.wordBasedSuggestions": "off",
    "editor.formatOnType": false,
    "editor.formatOnPaste": false,
    "editor.formatOnSave": false,
    "editor.semanticHighlighting.enabled": true,
    "editor.occurrencesHighlight": "off",
    "editor.selectionHighlight": true,
    "editor.codeLens": false,
    "editor.lightbulb.enabled": "onCode",
    "merge-conflict.codeLens.enabled": false,
    "multiDiffEditor.experimental.enabled": false,
    "jsonc.validate.enable": true,
    "json.validate.enable": true,
    "prettier.enable": true,
    "javascript.validate.enable": true,
    "markdown.validate.enable": false,
    "extensions.ignoreRecommendations": true,
    "github.copilot.enable": {
        "*": false,
        "plaintext": true,
        "markdown": false,
        "scminput": false
    },
    "files.watcherExclude": {},
    "files.exclude": {},
    "search.exclude": {
        ".vscode/ocrmnavigator/odin/version": true
    },
    "typescript.validate.enable": true,
    "markdown.server.log": "off",
    "html.validate.scripts": false,
    "search.smartCase": true,
    "search.useIgnoreFiles": false,
    "Codegeex.GenerationPreference": "line by line",
    "Codegeex.Privacy": false,
    "Codegeex.License": "",
    "codegeex.codeLens.functionQuickOptions": {
        "addComment": false,
        "ghostComment": false,
        "fixBug": false,
        "generateUnitTest": false,
        "reviewCode": false,
        "codeOptimization": false,
        "addDocString": false,
        "addExceptionHandling": false,
        "printLogForDebugging": false,
        "improveRunningEfficiency": false,
        "renameSymbols": false,
        "newFileForDebugging": false,
        "tryANewApproach": false,
        "explainCode": false
    },
    "codegeex.codeLens.classQuickOptions": {
        "explainCode": false,
        "ghostComment": false,
        "fixBug": false,
        "generateUnitTest": false,
        "reviewCode": false,
        "addDocStringForClass": false,
        "addDocStringForMethods": false,
        "addComment": false
    },
    "geminicodeassist.chat.changeView": "Default diff view",

    "[typescriptreact]": {
        "editor.defaultFormatter": "vscode.typescript-language-features"
    },
    "[json]": {
        "editor.defaultFormatter": "skyler.ocrmnav"
    },
    "[typescript]": {
        "editor.defaultFormatter": "skyler.ocrmnav"
    },
    "explorer.fileNesting.enabled": true,
    "explorer.fileNesting.expand": false,
   
    "workbench.startupEditor": "none",
    "explorer.decorations.colors": false,
    "problems.decorations.enabled": false,
    "window.menuBarVisibility": "toggle",
    "window.commandCenter": false,
    "menubar.layoutControls": false,
    "editor.renderControlCharacters": false,
    "editor.renderWhitespace": "none",
    "editor.minimap.enabled": true,
    "breadcrumbs.enabled": false,
    "workbench.sideBar.location": "left",
    "workbench.layoutControl.enabled": false,
    "workbench.secondarySideBar.showLabels": false,
    "workbench.navigationControl.enabled": false,
    "workbench.editor.showTabs": "multiple",
    "menubar.navigationControls": false,
    "menubar.share": false,
    "primarySidebar.display": true,
    "secondarySidebar.display": true,
    "panel.display": false,
    "panel.alignment": "center",
    "panel.view": "output",
    "modes.centeredLayout": false,
    "modes.fullScreen": false,
    "modes.zenMode": false,
    "window.zoomLevel": -1,
    "editor.glyphMargin": true,
    "editor.folding": true,
    "editor.lineNumbers": "relative",
    "editor.showFoldingControls": "always",
    "editor.minimap.maxColumn": 50,
    "editor.minimap.showRegionSectionHeaders": true,
    "editor.minimap.showMarkSectionHeaders": false,
    "editor.minimap.autohide": "mouseover",
    "editor.minimap.showSlider": "mouseover",
    "editor.minimap.side": "left",
    "editor.minimap.size": "fill",
    "editor.minimap.renderCharacters": false,
    "editor.wordWrap": "on",
    "editor.fontFamily": "Geist Mono",
    "editor.fontLigatures": true,
    "editor.fontVariations": true,
    "workbench.editor.pinnedTabsOnSeparateRow": true,
    "workbench.editor.alwaysShowEditorActions": true,
    "workbench.editor.wrapTabs": true,
    "workbench.externalBrowser": "Chrome",
    "workbench.remoteIndicator.showExtensionRecommendations": false,
    "workbench.commandPalette.history": 30,
    "window.restoreWindows": "one",
    "workbench.editor.autoLockGroups": true,
    "workbench.panel.showLabels": false,
    "editor.foldingImportsByDefault": false,
    "git.diffEditor.renderGutterMenu": false,
    "git.decorations.enabled": false,
    "editor.scrollBeyondLastLine": false,
    "terminal.integrated.fontSize": 12,
    "editor.fontSize": 12,
    "scm.diffDecorationsGutterAction": "none",
    "scm.diffDecorations": "none",
    "workbench.iconTheme": "baldr-icons",
    "workbench.activityBar.location": "default",
    "workbench.editor.decorations.colors": false,
    "window.newWindowDimensions": "inherit",
    "workbench.editor.highlightModifiedTabs": false,
    "markdown.preview.scrollPreviewWithEditor": false,
    "markdown.preview.scrollEditorWithPreview": false,
    "ocrmnavigator.devstack.icons": true,
    "ocrmnavigator.devstack.snapshotNgin": true,
    "ocrmnavigator.devstack.ivaldi": true,
    "ocrmnavigator.devstack.devstack": true,
    "ocrmnavigator.devstack.odin": true,
    "ocrmnavigator.devstack.formatters": true,
    "ocrmnavigator.devstack.titlebar.search": true,
    "ocrmnavigator.devstack.titlebar.refresh": true,
    "ocrmnavigator.devstack.titlebar.config": true,
    "ocrmnavigator.devstack.titlebar.ui": true,
    "ocrmnavigator.baldr.icons": true,
    "ocrmnavigator.odin.settings.exlcude.default": "",
    "ocrmnavigator.odin.contextLinesBefore": 4,
    "ocrmnavigator.odin.contextLinesAfter": 10,
    "ocrmnavigator.odin.query": "",
    "ocrmnavigator.odin.replace": "",
    "ocrmnavigator.odin.includePattern": "",
    "ocrmnavigator.odin.excludePattern": "",
    "ocrmnavigator.odin.useRegex": false,
    "ocrmnavigator.odin.caseSensitive": false,
    "ocrmnavigator.odin.matchWholeWord": false,
    "ocrmnavigator.odin.useFuzzy": false,
    "ocrmnavigator.odin.searchInOpenEditorsOnly": false,
    "ocrmnavigator.odin.useExcludeSettings": false,
    "ocrmnavigator.odin.includeEnabled": false,
    "ocrmnavigator.odin.excludeEnabled": false,
    "ocrmnavigator.odin.searchScope": "workspace",
    "ocrmnavigator.vfs.onFileOpen": "openInSetCol",
    "ocrmnavigator.vfs.targetEditorGroup": 1,
    "ocrmnavigator.codesnap.windowControlStyle": "Windows",
    "ocrmnavigator.codesnap.showWindowTitle": true,
    "ocrmnavigator.codesnap.windowBorderRadius": "8px",
    "ocrmnavigator.codesnap.windowTitleStyle": "Filename",
    "ocrmnavigator.codesnap.showLineNumbers": true,
    "ocrmnavigator.codesnap.realLineNumbers": false,
    "ocrmnavigator.codesnap.transparentBackground": false,
    "ocrmnavigator.codesnap.trimEmptyLines": false,
    "ocrmnavigator.vfs.AUTO_FOLD_PKGJSON_2": false,
    "ocrmnavigator.vfs.AUTO_FOLD_PKGJSON_2_3": true,
    "ocrmnavigator.vfs.AUTO_FOLD_1": false,
    "ocrmnavigator.vfs.AUTO_FOLD_1_2": true,
    "ocrmnavigator.devstack.tasks": true,
    "ocrmnavigator.devstack.npmScripts": true,
    "ocrmnavigator.devstack.snippets": true,
    "ocrmnavigator.devstack.be": true,
    "ocrmnavigator.AUTORUN_DIR": "src",
    "ocrmnavigator.UPDATE_PROMPT_OBJECTS": false,
    "ocrmnavigator.AUTORUN_SCRIPTS": true,
    "ocrmnavigator.CONVERT_README_DEV_MD": false,
    "ocrmnavigator.PRO7": false,
    "ocrmnavigator.CONCURRENT": "bleeding-edge",
    "ocrmnavigator.ARCHIVER": "custom",
    "ocrmnavigator.DELETE_OLD_VSIX": true,
    "ocrmnavigator.AUTO_INSTALL_VSIX": true,
    "ocrmnavigator.OPEN_PUB_DASH": true,
    "ocrmnavigator.RELOAD_INSTANCE": true,
    "ocrmnavigator.todo.isPriv": false,
    "ocrmnavigator.todo.checkRemindersInterval": "10",
    "ocrmnavigator.todo.syncInterval": "20",
    "ocrmnavigator.todo.syncOnSave": true,
    "ocrmnavigator.todo.owner": "8an3",
    "ocrmnavigator.todo.branch": "main",
    "ocrmnavigator.runar.repository": "https://github.com/8an3/mynotesrepo.git",
    "ocrmnavigator.todo.repo": "mynotesrepo",
    "ocrmnavigator.todo.repository": "8an3/mynotesrepo",
    "ocrmnavigator.runar.repo": "runardb",
    "ocrmnavigator.runar.owner": "8an3",
    "ocrmnavigator.runar.branch": "main",
    "ocrmnavigator.devstack.item.hidden.toggle": true,
    "ocrmnavigator.strPrismaUpdater": true,
    "ocrmnavigator.commands": true,
    "ocrmnavigator.vscodecmdref": true,
    "ocrmnavigator.markdownViewer": true,
    "ocrmnavigator.snippetsInEditor": true,
    "ocrmnavigator.editorContextSnippets": true,
    "ocrmnavigator.formatters": true,
    "ocrmnavigator.trailingCommas": true,
    "ocrmnavigator.batchRename": true,
    "ocrmnavigator.eslintPrettier": true,
    "ocrmnavigator.remixUtils": true,
    "ocrmnavigator.theme": true,
    "ocrmnavigator.vscode.theme.blacked": true,
    "ocrmnavigator.vscode.theme.window.differentiator": true,
    "ocrmnavigator.shadCNComponents": true,
    "ocrmnavigator.repoMgr": true,
    "ocrmnavigator.openGithub": true,
    "ocrmnavigator.githubFunctions": true,
    "ocrmnavigator.prismaFunctions": true,
    "ocrmnavigator.remixComponents": true,
    "ocrmnavigator.clickToSchema": true,
    "ocrmnavigator.crudResolvers": true,
    "ocrmnavigator.fileNesting": true,
    "ocrmnavigator.revealExplorer": true,
    "ocrmnavigator.devstack.item.path.copy": true,
    "ocrmnavigator.bookmarks": true,
    "ocrmnavigator.searchBar": true,
    "ocrmnavigator.clipBoardHistory": true,
    "ocrmnavigator.lucideIcons": true,
    "ocrmnavigator.share": true,
    "ocrmnavigator.url": true,
    "ocrmnavigator.format.json.remove.comments.file": true,
    "ocrmnavigator.con": true,
    "ocrmnavigator.format.remove.comments.file": true,
    "ocrmnavigator.unusedFunctions": true,
    "ocrmnavigator.viewers": true,
    "ocrmnavigator.uiDashboard": true,
    "ocrmnavigator.devStackFunctions": true,
    "ocrmnavigator.devstack.site.md.render": true,
    "ocrmnavigator.project.index.smart.create": true,
    "ocrmnavigator.devstack.site.tailwindConverter": true,
    "ocrmnavigator.remix.project2agnostic.convert": true,
  
}
```

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Closing Notes

I'm aware that being so upfront about the extension and exactly how it will effect your coding enviroment will turn some people away because of how large of a change it is. Which is fine, this extension will not be for everyone. 

But for anyone who does try it out, I hope you enjoy the new experience as I have, so much so I no longer even thinking about trying to find a new platform. 

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Extra: Attempting this yourself

Please do not look at this and say to yourself, "If he can do it so can I.". I touch more on this in the background section but, this was not something I had orginally set out to do and is a massive undertaking. 

The best way I could explain it to someone with as little words as possible. Would you like to not only create the code for each feature but also maintain it for bugs and updates, not just the code base but the documentation as well for 175+ extensions? 

If you answer yes, good luck my friend, truly. As the path you are about to embark on will truly suck, lol. VSCode, as you may already know, is notorious for horrible documentation that you will 100% run into time and time again and you will be coding entirely blind. 

Don't get me wrong, I am happy with where this path has lead me as it allows to code on a level of effeciency that vscode... may never be able to reach all on its own. Not to mention, you have to overcome VSCodes BIGGEST handicap... its performance. I hope it is still there, I will check to see if it is and if it's not I will ensure that it is, but there is a section contained in the layout documentation that goes over this handicap in great detail and reveal to you exactly where this handicap is from and how to work with it. 

The last peice of advice I have for anyone who is crazy enough to try this, learn to code in such a way that the codebase does not need you for updates from the start. If you do not learn this early, or if you do learn this later on you must go back and update your code to update itself on its own. IF you do not do this... you will be forever chained to the codebase and updating it constantly as I was early on in the development of this extension. 

I am truly happy with this extension because if I had set out to create this from the start, I don't think I would have even started. For the ones that do start, I hope you use this tool to help you on your journey because I know that some features I still have planned will be able to help you massively with that undertaking.

I know I already said one last peice of advice but something I had just thought of. I attribute the success of this extension entirely with luck by starting out with creating a virtual file system with using it as a shortcut system. Now you don't have to start out with this feature, but it will make everything easier as you continue creating features in so many different ways. For example, starting with this gives you the oppurtunity in creating a terminal ngin from the start, rather than when you are 40 features deep. The terminal ngin is crucial, not just for performance, but also for a much better user experience as they only have to endure one or two terminal windows instead of 30+. The terminal ngin also ensures a much easier coding experience since you are tunneling all of your features use of the terminal into a single point in your codebase.

Instead of just giving tidbits of information maybe I should just create a guide instead... That unfortuantly will have to take a seat at the back of the bus in terms of priority. Because there are wide range of things I could go over, that just simply are not covered by any blog or how to you could find. The best example of this is the terminal ngin, as I have never even seen another example such as this anywhere, and discussing such a thing is so hard to protray exactly what it is, and what it does by supplying just a couple of sentences. Re-reading that last paragraph from a users point of view I immediatly am asking myself, what the fuck does that even mean? lol

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Extra: Background


I have not yet had the chance to experience this myself as my vscode instance grew incrementally over time so in the near future I will re install vscode, since I only use vscode-insiders, and install the extension to experience this as you do. So if there are changes needed to be made, I will come back and do so.

I will be straight with you, this will change your experience with VSCode entirely. While I'm not the first to try to treat vscode as some kind of library you use to build upon in order to create a better user expereince. I can say with confidence, I'm the first to finish. Typically when devs set out to accomplish this goal, they do not realize just how big of an undertaking it is. The only reason why I was able to do it, is because I did not set out with creating an extension with that goal. 

It started with replacing a single extension, because it was just that terrible. Ended up being such a better alternative, not only to the extension that made me do it, but also every other marketplace offering that was in the same category. 

Then, when the next extension pushed me past a tipping point because of just how horrible of a ux it had, I thought, well the last one worked out great lets try it again.

This happened again... and again... to the point of where we are today.

The only reason I can promise a better UX across such a wide variety of features is not only was this extension for my use and my use only to help me code everyday. The bigger reason is because of exactly how I got into programming in the first as I was in sales for 15 years prior. 

In sales, you are subjected to whatever applications you are given. There is no way around that as sales people, almost entirely, do not have any background in any tech related... anything really. When it had come to light, just how much time I was wasting every day, week, month and year. Was the second I decided to make an entire crm for the automotive industry. 

While I did not have a background in tech, development or something similar, I did have a very very small amount of experience with coding. As I had built the adsolute best finance calculator a sales person could ever lay there hands on. Being at the top of my field, I was so... extreme when it came to building the calculator that, while I was using it day in and day out for my job. Any time I noticed that I could save even just half a second in doing any one thing pertaining to my job, later that night I would go home and make that change. Followed by, coming in the very next day and using that update first hand in the job. To this day, not a single other finance calculator even comes close to not just the features but the level it goes to help sales people with the most important aspect of their job.

Now that you have some background on how attentive I was with a single aspect of my job, will give some context for when I found out exactly how much time my crm was wasting, every day. Won't go into the event or the events leading up to it, but one night I had calculated that with only dealing with one single process of my job with that crm ended up to wasting over... 71 days a year. Just one of the many processes a sales person needs to do day in and day out, and we already at 71 days a year. Meanwhile, there is atleast 75-100 more that to this day I'm scared to death to even attempt to try to measure each one due to the fact that, when I had learned I was wasting that much time. I spent the next 2 weeks, everyday whenever I had a free moment to recalculate that amount because... I just could not come to terms with that reality. Being the best in my field, actually the best, I not only couldn't wrap my head around that figure, I could not accept it as a fact because... how could I? How is it that the best sales person, no matter where they sell, wastes that much time every year?

So much so, because of that and what I have learned coding... I cannot go back to that career without using my own crm and or tools in order to do the job. If I didn't have my own tools, I would simply go insane knowing full well just how much time I was wasting doing any process while I was doing it.

SO, as I got better with programming... I'm starting to notice the same fucking trend in this industry. Despite the fact that, the people in this industry... can actually make the needed changes in order to improve their day to day work lives. While as a sales person, this feat was so far in terms the realm of posibilities of ever being accomplished. While I was still working as a sales person, I had made the crm I was working on... to work entirely with the crm I had at work... but silently so that no one would even know or suspect that I was using anything but the provided crm. 

That is why, contained in this 'simple' extension that you will find free features that paid features pale in comparison with not just feature parity but also UX as well. Since every tool or feature I have ever built, I too will use it in addition to the user base and the last thing I need is another shitty tool to use. Since those are plentiful and are littered everywhere.




**Please excuse the state of the README.md document, as the renderer I have made doesn't seem to like the table. This does give me the oppurtunity to create a better version for users to focus on updating. Lets be honest, me adding anything to the readme at this point will not do anything in terms of persuading someone to try to the extension or not try it. So moving forward it will probably become that the readme featured in the in-app docs will be the one to go off of for users, once I have the time to go through it and update it to a new format, which that in itself will take a long time to complete since there are so many items.**