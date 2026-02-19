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