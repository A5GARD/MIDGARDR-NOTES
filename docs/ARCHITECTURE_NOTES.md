## Architechture Notes

I know, in passing, I have gone over a couple of items that will be listed here, but the following subject matter will go over how key items are built. In so doing you will know how the underlying code works when putting together your config, and it would be too much of a chore to individually go through each readme item and placing them in their relevant sections. Considering the redesign in code lately everything has been built to work off engines / classes in order to make the code base as a whole, run more efficiently.

The items listed will prioritze areas that will be of a greater benefit for you to learn about, items listed at or near the top will be more important than items at the end of the list. Because learning about the modular structure would help you greatly to take advantage of the extension as whole, but learning how the custom vsix archiver not so much. While the archiver could still effect, learning about it won't be of great importance in terms of your use of it. The only reason why that will be in the list is because for certain situations, it will be a better archiver to use than vsce, with saying that, it's not only faster than vsce but also less restrictive. The last point, depending on your situation, would of great benefit to you since you would now have an archiving option for your extension rather than trying to conform to vsce's requirements.

### Modular Function Building
Till recently, everything was built on a function per function basis. No consideration to any other feature or function found within the extension. The idea came to mind to instead adopt a different approach when coding new feautures, attempt to create seperate extension functions whenever and where that makes sense. 

Git being a great and easy example to go over, as before this change each git related function and build process was built on their own focusing on one thing meanwhile not exposing any functionality for any user to use. Converting almost all the code in its entirety in relation to github here are a few functions built and available for you to use as you see fit: 

- ocrmnavigator.git.diffCached
- ocrmnavigator.git.openRepo
- ocrmnavigator.git.openRepoAtFile
- ocrmnavigator.git.upgradeExtension
- ocrmnavigator.git.add
- ocrmnavigator.git.commit
- ocrmnavigator.git.diff
- ocrmnavigator.git.patch
- ocrmnavigator.git.pushTags
- ocrmnavigator.git.push

This enables you to build your configs and its individual items in all manners of ways. Essentially turning the extension into a CI/CD, just without the automation. With what it lakes in automation it shines in other areas such as total freedom, variety and so much more. And due to the level of asbsurdness, you will never see another extension like it.


### Automation, well the lack there of
Unless the benefit outweighs the cost of automation in such a vast amount, there will never be a single feature that will be introduced into this extension in relation to untriggered automation with the user removed entirely from the equation. As most automation, simply, does not need to be automated. Instead virtually... I've never actually thought about it from this point, but I would be comfortable stating 60%+ of what's currently automated, can simply switched to a triggered base activation. Ontop of that, there are so many features that just do not come close in terms, getting enough of a benefit to eat that cost.

Do I hate automation? No, I just believe 95% of current implementations built around it are shit and unneeded.

For example:
- icons library: I have created it so that all I have to do is literlly, drop an svg into a folder and click a line item in my devstack explorer pane and I do nothing else. It preps and builds all the icons, converts the icons over in order to be used in react apps, bumps the version patch, builds and compiles, scanning the current and newly created icons and then edits the readme automatically ensuring, whether its myself or a user, that the list stated on the npm listing is up to date and only lists icons that you can use, adds, commits, pushes to github, finally publishing to npm. I was able to make this such a painless and streamlined process, I have forgetten how many times I went to add a new icon, only to find out that it's already in there as an option to use.
- components library: it's at the point now, where unless I pay for ai which I will not, it won't be able to get any more automated then its current form. Everything from building, non-complicated components anyways, to creating objects for the inventory, all the different lists offered to functions in order to display content, creation of demos, there are a lot more in relation to the library but that will be in the next one. As I'm currently redesigning a lot right now in terms of that site, once that's done, unless I think of a new category to build like I had with the animation category, it will virtually be complete in terms of individual unique components to build. I don't beleive I will ever be done working on that project but ya, but again automated but the activation is user triggered.
- devstack, now this is where it gets stupid SO I hope I remember everything, probably won't though:
  - package.json: my package.json is over 40,000+ lines long... I'm not doing that manually, fuck that. Instead of dealing with that headache, I created package.dev.jsonc, which not only allows me to create comments and notes and whatever, this allows me to create static markers in a dynamically growing file. Ensuring that I do not have to guess where to input all automated generated content.
  - readme.md: up till the descision I made to try to not rely on the site anymore for docs, this file also had a dev counterpart, README.dev.md. Where the markdown pre-processor converted varaiables, updated the table of contents, updated the source map, converted human readable content to inline html because github cannot render certain use cases of tables and code sections which I had to find a solution for that issue. As the tables became too long and complicated to work with in a timely manner. Because think of it, as this extension covers the same functionality of 125+ extensions... I'm essentially writing documentation for 125+ extensions
  - vscode commands: as there is a manually created list, there is also a dynamically created list that scans your local instance for menu options
  - icons: anywhere you see data from the icon library, at build time it goes into that libraries folder and scans all the created icons and saving that data to a variable in order for the quick picks and context menus to insert into the editor
  - components library: while I currently have to fix the converters in there current state. When they are fixed, there are going over to that library also, scanning ALL 2700+ components and templates, writing them to a variable and then also converting the data and distributing it to the relevant functions and files in order for everything to work 
  - the build process: is allllll automated, as well as pushing to the marketplace, building the vsix archive. I do not do a single thing other than click a button 
  - essentially, any and all data that is derived from a source in order to provide it in some manner, is automated. If I didn't take this approach, fuck, I'd be in here every month updating something.
- the one ring to rule them all: to add fuel to the fire, I also hae a devstack line item that when triggered.... does ALL my personal projects, from building and compiling to pushing to their relevant sites to be published or standing them up ontop of all the converting, scanning and everything. 

Meanwhile, all of that and I am forgetting some points, will be getting redone now that I have the layout engine and when I properly configure that to my use cases. 
EVERYTHING will be a non-user triggered activation event, with ZERO cost in order to automate it. As there are no processes just constantly running in the background. 

That's why I beleive most of what's out there, doesn't need to be automated in the forms that they are. Almost all of them can be replaced by a well crafted triggered activation event. 

Whenever I see large amount of processes running in the background, that tells me that you don't know your user, you don't entirely understand the functions you are employing, among other things. Because if you did, you wouldn't need scans constantly running in the background eating resources, and eventually bringing whatever that is running to a unusable state because it's so slow. 

You can't tell me I'm wrong, look at vscode for example, every single user has experienced performance issues to the point of the user NEEDING to do something in relation to extensions, to get that performance back.

### Autorun Folder

### Package Managers

### Local VSCode Instance Scans ( producing lists for vscdoe commands )

### Naming Conventions - Functions && Settings

### Terminal Engine 

#### How every function executes

#### Concurrent & Chain

### Context

#### pro7

####