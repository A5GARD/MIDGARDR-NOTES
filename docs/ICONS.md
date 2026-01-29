
# Icons Library

## File Ext Icons 

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


## Icons NPM Package

A React icon library designed for simplicity and accuracy with a sensible naming convention.

**Installation:**

```bash
npm install @catalystsoftware/icons
# or
pnpm add @catalystsoftware/icons
```

**Usage:**

```javascript
import { Message } from '@catalystsoftware/icons'
```

**Features:**
- Clean, logical naming convention
- Filled variants available
- Customizable colors
- Flexible sizing options
- Designed for React applications

![NPM Icon Library](https://raw.githubusercontent.com/8an3/midgardr-notes/main/icons/npm-icon.jpg?raw=true)


---

## Icons Quick Pick

Browse and insert icons from the @catalystsoftware/icons library directly in your editor


**Access:** Editor context menu → Catalyst → Icons

**Features:**
- Integrated search functionality
- Instant insertion at cursor position
- Complete library access
- Preview icons before insertion

**Naming Convention:**  
Icons follow a logical pattern: `[MainTheme][Container/Feature][Filled]`

**Example:** `MessageSquareFilled`, `UserCircle`, `SettingsGear`

![Icons Quick Pick](https://raw.githubusercontent.com/8an3/midgardr-notes/main/icons/icon-quickpic.jpg?raw=true)


---

[🡄 Return](https://github.com/8an3/DevStack)