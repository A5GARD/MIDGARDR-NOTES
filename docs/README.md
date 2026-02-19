<!-- BUT - you could also just add a button in your file explorer that runs vscode.commands.executeCommand('workbench.action.terminal.toggleTerminal') to show/hide the panel. -->
 
 <!-- 
Function                 - Suggested Color                        - Logic & Psychology
file or an icon that represents a file that just sits there with no functionality 
#84cc16
Create    #22C55E     - Green                                  - "Standard for ""New - "" ""Add - "" or ""Go."" It represents growth and initialization."
Load / Open #2563EB    - Blue or Grey                           - "A neutral ""process"" action. Blue is often used for information retrieval."
Save #3178C6           - Blue                                   - "Historically tied to the floppy disk icon and ""stability."" It feels secure."
Publish #9135FF        - Purple or Teal                         - "Distinct from ""Save."" It signals a transition from private to public."
Upload / Push / Sync #FC6D26    - Orange or Blue                         - "High-energy colors. In Git -  ""Push"" is an active movement of data."
Delete #FF3E00        - Red                                    - "The universal ""Stop"" or ""Danger"" signal. Use it sparingly to warn of data loss."
Download / Clone #3B82F6  - Indigo or Light Blue                   - "Pulling data ""down"" from the cloud; feels like a secondary utility."
Switch / Merge / Replace #F7DF1E - Yellow or Amber                        - "Signals a state change or ""Caution."" Merging requires attention."
Install                  - Deep Green or Teal                     - "Similar to ""Create - "" but with a sense of completion/finality." --->

<!-- #region HEADER -->

<div align="center">

![Z](https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/odin.png)

</div>
<p align="center"><h1 align="center">DevStack</h1></p>
<p align="center"><em>The Extension That Fixed VSCode</em></p>


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **TLDR;**
<br />

| 🚀 **FIRST-IN-CLASS** · <i>Exclusive Innovations</i> | 🏆 **BEST-IN-CLASS** · <i>Superior Workflow Tools</i> |
|:-------------------------|:-------------------------|
| **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/LOKI.md"><img src="https://img.shields.io/badge/LOKI%20AI: Operate AI outside the data set-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij4KPHBhdGggZD0iTTAgMCBDNC43ODA4OTg4NCAxLjkxMjM1OTU0IDYuNzA3MzQ3NiAzLjIzNjk2ODY5IDEwIDcgQzEwIDcuNjYgMTAgOC4zMiAxMCA5IEM3LjA4NDgyNzA4IDcuOTI1OTg4OTIgNS4yMjE4OTgyNCA3LjIyMTg5ODI0IDMgNSBDMi42NyAxMC42MSAyLjM0IDE2LjIyIDIgMjIgQzEuMzQgMjIgMC42OCAyMiAwIDIyIEMwIDE0Ljc0IDAgNy40OCAwIDAgWiAiIGZpbGw9IiMwMDAwMDAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDcsMSkiLz4KPC9zdmc+Cg=="></a>**<br>★ Shapeshifter - adapts prompts dynamically<br>★ Rule breaker - bypasses AI limitations and training constraints<br>★ Trickster - manipulates the system cleverly<br>★ Boundary crosser - transcends what the base model can do<br>★ Chaos agent - creates novel solutions outside training data | **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/LOKI.md"><img src="https://img.shields.io/badge/LOKI%20AI:  Deterministic AI Prompt Compiler-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij4KPHBhdGggZD0iTTAgMCBDNC43ODA4OTg4NCAxLjkxMjM1OTU0IDYuNzA3MzQ3NiAzLjIzNjk2ODY5IDEwIDcgQzEwIDcuNjYgMTAgOC4zMiAxMCA5IEM3LjA4NDgyNzA4IDcuOTI1OTg4OTIgNS4yMjE4OTgyNCA3LjIyMTg5ODI0IDMgNSBDMi42NyAxMC42MSAyLjM0IDE2LjIyIDIgMjIgQzEuMzQgMjIgMC42OCAyMiAwIDIyIEMwIDE0Ljc0IDAgNy40OCAwIDAgWiAiIGZpbGw9IiMwMDAwMDAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDcsMSkiLz4KPC9zdmc+Cg==" ></a>** <br>☆ Achieves unprecedented AI success rates through zero-touch context assembly<br>☆ Automatically gathers files, dependencies, and project structure—eliminating manual prompt engineering and copy-paste workflows entirely. |
|  **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md"><img src="https://img.shields.io/badge/THOR THOR Styling: Tailwind V4 Plug In%20-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij4KPHBhdGggZD0iTTAgMCBDMC42NiAwIDEuMzIgMCAyIDAgQzIuMjA2MjUgMC45MDc1IDIuNDEyNSAxLjgxNSAyLjYyNSAyLjc1IEM0LjMyMDQwNzkgNi43NTczMjc3NiA2LjI3NTQ5Nzg0IDcuODk0ODQ2NjEgMTAgMTAgQzguODkyNDIzNzggMTIuOTE5OTczNjcgOC4yMjE4NjQxNSAxMy44NzU1Mzk2MiA1LjQzNzUgMTUuNDM3NSBDMi43NDU2OTcxNSAxNi43OTA2MjcxMiAyLjc0NTY5NzE1IDE2Ljc5MDYyNzEyIDIuMTg3NSAxOS42ODc1IEMyLjEyNTYyNSAyMC40NTA2MjUgMi4wNjM3NSAyMS4yMTM3NSAyIDIyIEMxLjM0IDIyIDAuNjggMjIgMCAyMiBDMCAxNC43NCAwIDcuNDggMCAwIFogTTIgOCBDMiA5Ljk4IDIgMTEuOTYgMiAxNCBDMy4zMiAxMy4zNCA0LjY0IDEyLjY4IDYgMTIgQzYgMTEuMzQgNiAxMC42OCA2IDEwIEM0LjY4IDkuMzQgMy4zNiA4LjY4IDIgOCBaICIgZmlsbD0iIzAwMDAwMCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNywxKSIvPgo8L3N2Zz4K" ></a>** <br>☆ Don't want to upgrade from v3? Me neither, but that's ok... I got you<br>☆ Plug and play | **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md"><img src="https://img.shields.io/badge/THOR THOR%20Styling: Tailwind Preset Config Ngin-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij4KPHBhdGggZD0iTTAgMCBDMC42NiAwIDEuMzIgMCAyIDAgQzIuMjA2MjUgMC45MDc1IDIuNDEyNSAxLjgxNSAyLjYyNSAyLjc1IEM0LjMyMDQwNzkgNi43NTczMjc3NiA2LjI3NTQ5Nzg0IDcuODk0ODQ2NjEgMTAgMTAgQzguODkyNDIzNzggMTIuOTE5OTczNjcgOC4yMjE4NjQxNSAxMy44NzU1Mzk2MiA1LjQzNzUgMTUuNDM3NSBDMi43NDU2OTcxNSAxNi43OTA2MjcxMiAyLjc0NTY5NzE1IDE2Ljc5MDYyNzEyIDIuMTg3NSAxOS42ODc1IEMyLjEyNTYyNSAyMC40NTA2MjUgMi4wNjM3NSAyMS4yMTM3NSAyIDIyIEMxLjM0IDIyIDAuNjggMjIgMCAyMiBDMCAxNC43NCAwIDcuNDggMCAwIFogTTIgOCBDMiA5Ljk4IDIgMTEuOTYgMiAxNCBDMy4zMiAxMy4zNCA0LjY0IDEyLjY4IDYgMTIgQzYgMTEuMzQgNiAxMC42OCA2IDEwIEM0LjY4IDkuMzQgMy4zNiA4LjY4IDIgOCBaICIgZmlsbD0iIzAwMDAwMCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNywxKSIvPgo8L3N2Zz4K" ></a>**<br>★ By only modifying 3 variables, you have 18,000+ combinations in options in terms of not only how your site looks but also feels<br>★ Supply a preset, theme and font and whether it be sizing, colors, spacing, padding, typography... All factors change dynamically across your entire project. |
| <img src="https://img.shields.io/badge/Live VS Code Internals Inspector-0284c7?style=plastic"><br>★ The only UI-driven tool to expose VS Code's internal context and config APIs<br>★ Debug and manipulate workspace state in real-time without writing a single line of code. | **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/RÚNAR.md"><img src="https://img.shields.io/badge/RÚNAR: Snippet Development Studio%20-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBzdGFuZGFsb25lPSJubyI/Pgo8IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDIwMDEwOTA0Ly9FTiIKICJodHRwOi8vd3d3LnczLm9yZy9UUi8yMDAxL1JFQy1TVkctMjAwMTA5MDQvRFREL3N2ZzEwLmR0ZCI+CjxzdmcgdmVyc2lvbj0iMS4wIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiB3aWR0aD0iMjQuMDAwMDAwcHQiIGhlaWdodD0iMjQuMDAwMDAwcHQiIHZpZXdCb3g9IjAgMCAyNC4wMDAwMDAgMjQuMDAwMDAwIgogcHJlc2VydmVBc3BlY3RSYXRpbz0ieE1pZFlNaWQgbWVldCI+CjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuMDAwMDAwLDI0LjAwMDAwMCkgc2NhbGUoMC4xMDAwMDAsLTAuMTAwMDAwKSIKZmlsbD0iIzAwMDAwMCIgc3Ryb2tlPSJub25lIj4KPHBhdGggZD0iTTcwIDEyMCBjMCAtNjAgNCAtMTAwIDEwIC0xMDAgNiAwIDEwIDE3IDEwIDM4IGwwIDM3IDM0IC00MCBjMTkgLTIyCjM3IC0zOCA0MCAtMzUgMyAzIC0xMyAyNiAtMzQgNTIgbC00MCA0NiA0MSAyNyA0MSAyNyAtMzggMjQgYy02MiAzOCAtNjQgMzYKLTY0IC03NnogbTcwIDUwIGMwIC00IC0xMSAtMTIgLTI1IC0xOCAtMjQgLTExIC0yNSAtMTAgLTI1IDE4IDAgMjggMSAyOSAyNQoxOCAxNCAtNiAyNSAtMTQgMjUgLTE4eiIvPgo8cGF0aCBkPSJNMjE5IDE3MyBjLTEzIC0xNiAtMTIgLTE3IDQgLTQgMTYgMTMgMjEgMjEgMTMgMjEgLTIgMCAtMTAgLTggLTE3Ci0xN3oiLz4KPC9nPgo8L3N2Zz4K" ></a>**<br>☆ A full-featured web IDE for snippets with Monaco editor integration<br>☆ Build and share team snippets 10x faster than the native JSON editor. |
| **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BROKKR.md"><img src="https://img.shields.io/badge/BROKKR: Workspace Layouts%20-0284c7?style=plastic"></a>**<br>☆ Total environment restoration in one click<br>☆ Instantly reset your theme, UI visibility, terminals, tabs, and view focus for a perfect setup every time.<br>☆ Complexity breakdown, offering different levels of access to settings | **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/BIFRÖST: Command Palette on Steroids-0284c7?style=plastic&logo=data:image/png;base64,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" ></a>**<br>★ Access a library of 5,175+ searchable commands with deep descriptions and instant category filtering |
| **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/BIFRÖST:%20 Intelligent Command Ngin-0284c7?style=plastic&logo=data:image/png;base64,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"></a>**<br>★ Master 17+ execution patterns including sequential, concurrent, and mixed-mode grouping<br>★ Run PowerShell and WSL Bash side-by-side in unified, color-coded terminals.<br>★ Concurrently runs and displays persistent windows and linux terminal enviroments<br>★ Smart terminal management, determins whether a terminal window should be reused or not based on each triggered command that gets executed through the ngin | <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#L55"><img src="https://img.shields.io/badge/Visual Command Architecture-0284c7?style=plastic"></a><br>☆ A powerful tree view featuring 520+ icons and unlimited nesting. Find and execute complex workflows faster than the standard palette. |
| <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/Enterprise Config Scaling-0284c7?style=plastic" ></a><br>☆ Built for complexity<br>☆ Battle-tested across 45+ workspaces managing 20,000+ lines of configuration<br>☆  Seamless Global-to-Workspace merging. | <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md"><img src="https://img.shields.io/badge/Enterprise Grade Bookmarks-0284c7?style=plastic"></a><br>★ Global, shareable, and line-specific bookmarks with unlimited nested organization and integrated search. |
| <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MUNINN.md#L84"><img src="https://img.shields.io/badge/Auto Generated Prisma Schemas-0284c7?style=plastic"></a><br>★ Eliminate manual maintenance<br>★ Engine scans your codebase and automatically generates or updates your Prisma schemas on the fly. | <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#L145"><img src="https://img.shields.io/badge/VSCode Extension Dev Automation-0284c7?style=plastic"></a><br>☆ Skip the CI/CD overhead<br>☆ One-click local packaging and installation lets you test and ship extensions in seconds. |
| <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#L787"><img src="https://img.shields.io/badge/Context Aware Settings Toggles-0284c7?style=plastic"></a><br>☆ Dynamically generated UI toggles for every VS Code setting<br>☆ Manage your entire environment and all installed extensions with one-click simplicity. | <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md"><img src="https://img.shields.io/badge/Professional Clipboard History-0284c7?style=plastic"></a><br>★ A high-performance 100-item history with hover previews<br>★ Pro-level clipboard management built directly into your editor. |
| <a href="https://catalyst-software.vercel.app/asgard/midgardr/home/list">**<img src="https://img.shields.io/badge/ᛗ MIÐGARÐR UI: X-0284c7?style=plastic">**</a><br>★ Unlocking a whole new variant system in addtion to THOR variations<br>★ Ability to assign different DOM variants as if they were THOR variants <br>★ Utilizes the same API system as THOR variants<br>★ Cuts down on overall component files, instead of having any number of files that cover a component and all its forms of variants down to a single file | **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#odin"><img src="https://img.shields.io/badge/ODIN:%20Search Editor-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij4KPHBhdGggZD0iTTAgMCBDNy4xNzM5MTMwNCAyLjM5MTMwNDM1IDcuMTczOTEzMDQgMi4zOTEzMDQzNSAxMCA1IEMxMCA1LjY2IDEwIDYuMzIgMTAgNyBDNS4yNSA2LjEyNSA1LjI1IDYuMTI1IDMgNSBDMyA1Ljk5IDMgNi45OCAzIDggQzYuNDY1IDkuOTggNi40NjUgOS45OCAxMCAxMiBDMTAgMTIuOTkgMTAgMTMuOTggMTAgMTUgQzUuMjUgMTMuMTI1IDUuMjUgMTMuMTI1IDMgMTIgQzIuNjcgMTUuMyAyLjM0IDE4LjYgMiAyMiBDMS4zNCAyMiAwLjY4IDIyIDAgMjIgQzAgMTQuNzQgMCA3LjQ4IDAgMCBaICIgZmlsbD0iIzAwMDAwMCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNywxKSIvPgo8L3N2Zz4K" ></a>**<br>☆ VS Code's search editor reimagined with live find/replace across all results.<br>☆ Innovative remote editing: Edit matches directly in the search view and save changes to all files at once—no navigation required.<br>☆ Fuzzy search option<br>☆ Regex helper |
| **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BROKKR.md"><img src="https://img.shields.io/badge/BROKKR: UI Menu%20-0284c7?style=plastic" ></a>**<br>☆ Consolidates VSCode's fragmented UI customization landscape - No more hunting through nested submenus, scattered titlebar controls, command palette searches, or diving into JSON files<br>☆ 125+ unified options - Each displaying its current value and setting description, bringing together controls that Microsoft scattered across 4+ menu levels and multiple interfaces, while also exposing settings that previously had no UI outside manual JSON editing<br>☆ Single source of truth for UI manipulation - Designed to completely replace your current workflow for customizing VSCode's interface, accessible directly from the status bar<br>☆ First-in-class solution - While no other extension has attempted to solve VSCode's UI control fragmentation problem, this feature serves dual purpose: providing the convenience layer users need while simultaneously tracking UI element state changes through extension context to ensure the layout ngin maintains reliability and accuracy | <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/LAYOUT.md"><img src="https://img.shields.io/badge/Ultimate Settings.json Guide-0284c7?style=plastic"></a><br>★ The definitive deep-dive into VS Code's hidden configuration APIs and theme customization.<br>★ Reveals undocumented settings, solves critical performance bottlenecks, and explains the architecture behind this extension's unique capabilities. |
| **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md"><img src="https://img.shields.io/badge/FREYR & THOR THEME BUILDER: Unified Design System-0284c7?style=plastic" ></a>**<br>☆ The only tool that bridges Tailwind THOR (v3 & v4) and VSCode theming ecosystems with bidirectional intelligent automation<br>☆ Single preset theme choice automatically propagates across three systems<br>☆ Simultaneous real-time rendering of both VSCode UI recreation and semantic color highlighting AND web page enviroment to review tailwind styling, allowing users to see exactly how their theme behaves in actual editor context before export<br>☆ Custom-built popover displaying the entire color spectrum with pre-populated harmonious colors, replacing the tedious traditional color picker workflow where users blindly adjust HSL values by single degrees<br>☆ Outputs in four production-ready formats <br>☆ Automatically generates and pre-configures 20+ semantic token colors and 50+ token color scopes based on your theme choices, while still allowing granular individual customization. Solves the industry's biggest pain point where manual semantic token configuration requires deep understanding of VSCode's token system<br>☆ Industry-standard preset themes provide professional starting points, with every color individually customizable through both traditional color picker and the innovative color wheel system, supporting workflows from "quick professional theme in 5 minutes" to "pixel-perfect custom design system"<br>☆ Not competing with existing Tailwind theme generators or VSCode theme builders, but creating an entirely new class of unified design system tools that treat web and editor theming as the integrated workflow it should be  |  **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md"><img src="https://img.shields.io/badge/ᚠ FREYR: Theme Collection-0284c7?style=plastic"></a>**<br>☆ Best-in-class curated theme collection - 140+ professionally designed themes (70 base themes × 2 variants each) systematically built from color wheel theory and community-validated color palettes from popular design sites, ensuring every theme meets professional quality standards rather than arbitrary aesthetic choices<br>☆ Innovative dual-variant system - Each theme ships in two versions: fully themed variant with complete semantic token and syntax highlighting customization for immersive experiences, and default variant pairing your workbench colors with VSCode's default syntax highlighting. Solves the industry-wide problem where users love a theme's UI but hate its syntax colors and are forced to choose different themes or manually override settings<br>☆ Scientifically designed for consistency - Unlike marketplace theme packs that rely on subjective aesthetics, every theme is anchored to either color wheelharmonies or battle-tested community palettes, resulting in a collection where each theme is genuinely usable rather than filler variants to inflate numbers<br>☆ Complete token coverage - Every theme includes comprehensive semanticTokenColors (20+ tokens) and tokenColors (50+ scopes) with language-specific optimizations, ensuring consistent, intentional highlighting across all major languages rather than falling back to VSCode defaults<br>☆ Accessibility considerations - Includes themes specifically designed for users suffering from headaches, eye soreness, and fatigue from prolonged computer use, addressing a medical need most theme creators ignore<br>☆ Quality over quantity at scale - While offering 140+ options, maintains such high quality standards that the creator genuinely prefers any single theme from this collection over literally any VSCode marketplace offering, indicating a quality bar rarely achieved in large theme packs where most entries are throwaway variations |
|| **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#themes"><img src="https://img.shields.io/badge/ᛊ SAGA: To Do, Notes, Reminders and Post Its-0284c7?style=plastic" ></a>**<br>★ Reliable GitHub as a source of true, 0 rejected pushes within the past year<br>★ Interactive VSCode UI, clickable to do line items allowing to un/check without having to open the file with priority system<br>★ Innovative UI ie, tab based copy button<br>★ Compatibility, uses md file type<br>★ Autosync, pushes on each save event<br>★ Cross-platform, accompanied web app with offline capabilties<br>★ Utilizes VSCodes toast/notification system for reminders  |
|| **<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#themes"><img src="https://img.shields.io/badge/ᛗ MIÐGARÐR UI-0284c7?style=plastic" ></a>**<br>★ Single command library install that also installs and configures tailwind and postcss<br>★ 2500+ components<br>★ providing a UX/DX that is unprecedented in the extention/ui library ecosystem<br>★ in app functionality to insert usage example at cursor<br>★ full docuemntation provided entirely in the editor while you code<br>★ each component created with ease of use in mind<br>★ each component designed and created to allow users to quickly and easily add their own THOR variant flavours<br>★ Each component, while already providing a default barely stylized variant, hosts a wide range of pre-configured CVA variations<br>★ extensions unqiue sync with library for premium users |
 
<div align="center"><img src="https://img.shields.io/badge/DevStack-0284c7?style=plastic" ></br>Best-in-Class Multi-Purpose VSCode Extension: This entry was just too large to fit into the above table </div> 

|  |  |
|:-------------------------|:-------------------------|
| **Scope & Integration Density**<br>★ Consolidated 100+ standalone extensions worth of functionality into a single, cohesive system<br>★ The integration is architectural, not just feature-dumping - tools interact intelligently (LOKI + BIFRÖST, THOR + MIÐGARÐR, etc.)<br>★ Zero bloat is backed by proven scale (45+ workspaces, 20,000+ config lines) | **True Innovation**:  Unique UI implementations across several features<br>**★ LOKI AI:** - "Deterministic AI Prompt Compiler" that operates outside the training dataset is genuinely novel -Addresses the #1 pain point developers face with AI tools (inconsistent outputs) - The ability to work outside of its training data set<br>**★ BIFRÖST Command System:** - 17+ execution patterns with mixed-mode concurrent/sequential terminals - Cross-platform (PowerShell + WSL Bash) unified management - The auto-port engine and intelligent terminal reuse solve real enterprise problems<br>**★ THOR THOR/Tailwind:** - 18,000+ dynamic configurations from 3 variables is exceptional - Tailwind v4 plugin system while maintaining v3 compatibility shows deep understanding of user friction  |
| **Enterprise-Grade Architecture** | |
| Configuration Management:<br>★ Battle-tested at 20,000+ lines of config across 45+ workspaces<br>★ Global-to-Workspace intelligent merging<br>★ Remote resource management with profiles. <br> | Developer Experience: <br>★ Zero-touch context assembly (LOKI) eliminates manual prompt engineering <br>★ Monaco-level snippet editor (RÚNAR/SKÁLD) vs native JSON editing <br>★ Workspace layouts that restore entire environments in one click |
| **Problem-Solution Mapping. Every feature solves a documented pain point:**<br>★ "The terminal is a wall of 500 lines..." → Log to Lens (TÝR)<br>★ "I have to log into AWS Secrets Manager..." → API Secret Grabber (HERMÓÐR)<br>★ "Copy-paste loop between terminal and config..." → Tunnel Launcher (NEMESIS)  | **Depth Over Breadth. Unlike competitors that offer surface-level features**<br>★ MUNINN: Auto-generated Prisma schemas + CRUD resolvers<br>★ ODIN: Search editor with remote editing (change files without opening them)<br>★ HUGINN: Full Remix v1→v2 migration + monorepo conversion<br>★ MIÐGARÐR: 2,600+ components with in-editor autocomplete and signature help|

## Competitive Position vs. Other Multi-Purpose Extensions

| Them:  | DevStack:   |
|:-------------------------|:-------------------------|
| Task runners, snippets, themes, maybe some Git integration  | A complete devstack operating system inside VSCode |
| Tools  | Workflows (chains, concurrent execution, context-aware automation) |
| Manual configuration  |  Intelligent defaults + one-click setup (THOR, HUGINN scaffolding) |

## Unique Points Of Interest 

★ LOKI - No competitor has deterministic AI prompt compilation
<br>★ Cross-kernel terminal management - PowerShell + WSL in unified UI
<br>★ Workspace-aware everything - Configs, snippets, bookmarks, layouts all context-intelligent
<br>★ 18,000+ THOR configurations from 3 variables for web apps - Unmatched design system automation
<br>★ Remote editing in search results - Change files without opening them (ODIN)

| They offer:  | DevStack:   |
|:-------------------------|:-------------------------|
| Task runners, snippets, themes, maybe some Git integration  | A complete devstack operating system inside VSCode |
| Tools  | Workflows (chains, concurrent execution, context-aware automation) |
| Manual configuration  |  Intelligent defaults + one-click setup (THOR, HUGINN scaffolding) |

## What Elevates This to "Best-in-Class" 

1. Cohesive Ecosystem
<br>★ Features aren't siloed - they compound (LOKI contexts + BIFRÖST chains + BROKKR layouts)
<br>★ Norse mythology naming creates memorability and discoverability

2. Professional Tooling Quality
<br>★ RÚNAR/SKÁLD: Monaco editor for snippets (not textarea)
<br>★ VALHALLA: SQLite viewer with magic byte detection (not extension matching)
<br>★ Custom VSIX archiver: Has its own packaging because native tools can be limiting

3. Scale Validation
<br>★ "Battle-tested across 45+ workspaces" = Real-world proof
<br>★ "Zero rejected pushes in past year" (SAGA) = Reliability
<br>★ "20,000+ lines of config managed" = Enterprise-grade

4. Bleeding Edge + Stable Foundation
<br>★ Open access to features and tools while they are being developed and tested
<br>★ Enables the ability to continued access to reliable features while updates for them are a work in progress



<br><br>



<!-- #endregion -->
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **TOC**

<!-- #region TOC -->

> [!NOTE]
> ## The VSCode You Wish Microsoft Built
>
> **VSCode is good enough that you don't want to learn a new IDE, but frustrating enough that you constantly wish it worked better.** DevStack is what happens when a developer gets so fed up with those limitations that they rebuild the entire experience—while keeping it technically "just an extension."
>
> **Here's what that means:**
> - Still VSCode, so you can use it at work without approval
> - Doesn't feel like VSCode, because nearly every core feature has been replaced or rebuilt
> - 150+ extensions worth of power in a single install—without the performance death spiral
> - Zero "which extension conflicts with which" debugging sessions
> - Actually context-aware: your workspace dictates your environment, not the other way around
>
> **You're not installing an extension. You're escaping VSCode's limitations while still running VSCode.** It's the loophole you didn't know existed.
>
> If you've ever thought "I wish VSCode worked like [JetBrains/Cursor/literally anything else]" but couldn't actually switch—this is your answer.
>
> If your new to coding, and are unsure as to what this means exactly. It's as if, I took a BMW M3 motor ( vscode application ), and then built an entire car around that engine. It's built on a great platform that BMW is known for but your not actually driving a BMW.
>
> If you're just installing DevStack for the first time, skip ahead to [Top 7 Features to Try First](#top-7-features-to-try-first)

<pre style="max-width: 800px; white-space: pre-wrap; overflow-wrap: break-word; background-color: transparent; line-height: 1.4;">
/DEVSTACK_SYSTEM_ROOT/  
├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/OVERVIEW.md">OVERVIEW</a> 
├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ONBAORDING.md">ONBOARDING</a> 
├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/USAGE.md">GETTING STARTED & USAGE</a> 
├── <a href="#license">LICENSE</a> 
├── <a href="#acknowledgments">ACKNOWLEDGMENTS</a>
│
├── <img src="https://img.shields.io/badge/❕%20NOTE%20-6b21a8?style=plastic"> .................................... Badge legend
<!-- CATEGORY -->│   ├── <a href="#category"><img src="https://img.shields.io/badge/📂%20Category%20-475569?style=plastic"></a> ............................. May be its own feature and / or an umbrella for others
<!-- FEATURE -->│   ├── <a href="#works"><img src="https://img.shields.io/badge/📄%20Feature%20-0284c7?style=plastic"></a> .............................. Completed and tested
<!-- WORKS NO DOCS -->│   ├── <a href="#works-no-docs"><img src="https://img.shields.io/badge/✓%20Passed%20Tests%20(No%20Docs)-059669?style=plastic"></a> ................... Passed tests, but currently no docs 
<!-- In Testing -->│   ├── <a href="#implemented"><img src="https://img.shields.io/badge/♣%20In%20Testing-3B82F6?style=plastic"></a> ............................. Implemented, not tested, no docs  
<!-- UNTESTED -->│   ├── <a href="#untested"><img src="https://img.shields.io/badge/✗%20Untested-EF4444?style=plastic"></a> .............................. No docs, not tested  
<!-- IN DEV -->│   ├── <a href="#in-development"><img src="https://img.shields.io/badge/♠%20In%20Development-86198f?style=plastic"></a> ......................... In development  
<!-- PLANNED -->│   ├── <a href="#planned"><img src="https://img.shields.io/badge/♦%20Planned-ca8a04?style=plastic"></a> ............................... Feature has been decided upon  
<!-- PLANNED feature update -->│   ├── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> ..................................... An update to a feature has been planned  
<!-- PLANNED feature update -->│   │    ├── This feature is already up and running, but this new update would be adding to 
<!-- PLANNED feature update -->│   │    └── the already in place feature set and increasing its capabilities
<!-- MAYBE -->│   ├── <a href="#maybe"><img src="https://img.shields.io/badge/♥%20Maybe-F97316?style=plastic"></a> ................................ Thinking about it adding it, on the fence  
<!-- CURRENTLY DOWN -->│   └── <a href="#down"><img src="https://img.shields.io/badge/↓%20Currently%20Down-DC2626?style=plastic"></a> .......................... Feature is currently down
│ 
<!-- BIFROST -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/BIFRÖST%20/%20-0284c7?style=plastic&logo=data:image/png;base64,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"></a> ................................. Terminal and Multi Kernel Ngin
│   ├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#item-types">Item Types</a> ........................... VFS item types
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#file">`file`</a> ........................... Providing shortcuts to any file in any location 
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#md">`md`</a> ............................. Same as above, but for md
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#fileatline">`fileAtLine`</a> ..................... Instead opens the file at a specific line number
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#folder">`folder`</a> ......................... To house virtual file items within for organization
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#url">`url`</a> ............................ When executed, opens that url in your default browser
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#command">`command`</a> ........................ Executes vscode command
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#chain">`chain`</a> .......................... Executes any item type in a sequential firing order
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#concurrent">`concurrent`</a> ..................... Executes all commands, at once
│   │   │   └── Now uses node enviroment for both windows and bash shell enviroments
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#cmmdchain">`cmmdChain`</a> ...................... A chain of commands consisting of only vscode commands
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#conditionalchain">`conditionalChain`</a> ............... Depending on your checks, can execute or not in any form 
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#powershellcommand">`powershellCommand`</a> .............. Executes powershell commands
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#debiancmd">`debianCMD`</a> ...................... Executes baash commands in WSL's Debian enviroment
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#snippet">`snippet`</a> ........................ Copy snippet body to clipboard
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#copyvalue">`copyValue`</a> ...................... Copy value to clipboard
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#settingstoggle">`settingsToggle`</a> ................. Toggle workspace or global settings.json key:value pair
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#search">`search`</a> ......................... Searches, executed whenever you need with a click 
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#apicall">`apiCall`</a> ........................ Trigger Pre-made HTTP API requests at any time 
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#tasks">`tasks`</a> .......................... Auto generates within the explorer for easy access
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#npmscripts">`npmScripts`</a> ..................... Same as above but with your packages scripts
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#label">`label`</a> .......................... Visual divider used to break up an area
│   │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/♠%20Conditional-86198f?style=plastic"></a> .......................... new item type.
│   │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#menu"><img src="https://img.shields.io/badge/📄%20menu-3B82F6?style=plastic"></a> ............................. There are docs but right this second, its untested
│   │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#dependency-manager"><img src="https://img.shields.io/badge/♦%20Dependency%20Manager-ca8a04?style=plastic"></a> .................. Install/uninstall/update multiple npm packages in one click 
│   │   │    ├── with predefined sets (ie "React setup" installs react, react-dom, types in one go 
│   │   │    └── vs typing each npm install command)
│   │   └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#layout">`layout`</a> ......................... Taking complete control, of vscode and its interface
│   │        ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BROKKR.md"><img src="https://img.shields.io/badge/BROKKR%20-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPCFET0NUWVBFIHN2ZyBQVUJMSUMgIi0vL1czQy8vRFREIFNWRyAxLjEvL0VOIiAiaHR0cDovL3d3dy53My5vcmcvR3JhcGhpY3MvU1ZHLzEuMS9EVEQvc3ZnMTEuZHRkIj4KPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZlcnNpb249IjEuMSIgd2lkdGg9IjE5cHgiIGhlaWdodD0iMjRweCIgc3R5bGU9InNoYXBlLXJlbmRlcmluZzpnZW9tZXRyaWNQcmVjaXNpb247IHRleHQtcmVuZGVyaW5nOmdlb21ldHJpY1ByZWNpc2lvbjsgaW1hZ2UtcmVuZGVyaW5nOm9wdGltaXplUXVhbGl0eTsgZmlsbC1ydWxlOmV2ZW5vZGQ7IGNsaXAtcnVsZTpldmVub2RkIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayI+CjxnPjxwYXRoIHN0eWxlPSJvcGFjaXR5OjAuNjAxIiBmaWxsPSIjMDAwMDAwIiBkPSJNIDguNSwyLjUgQyAxMS42MjMxLDcuMzIyMTYgMTQuMjg5NywxMi40ODg4IDE2LjUsMThDIDE1Ljk3NDcsMTguNjkyNCAxNS4zMDgxLDE5LjE5MjQgMTQuNSwxOS41QyAxMS4zMDA5LDEzLjQ5NTYgNy42MzQyNiwxMy40OTU2IDMuNSwxOS41QyAyLjUsMTkuMTY2NyAxLjgzMzMzLDE4LjUgMS41LDE3LjVDIDQuMTIwNzIsMTIuNTk0MSA2LjQ1NDA1LDcuNTk0MDkgOC41LDIuNSBaIE0gOC41LDguNSBDIDEwLjczODgsMTAuMDAxMiAxMC43Mzg4LDExLjMzNDUgOC41LDEyLjVDIDcuNzA4NCwxMS4zMDAyIDcuNzA4NCw5Ljk2NjkgOC41LDguNSBaIi8+PC9nPgo8L3N2Zz4K&logoColor=fff"></a> WS Layout Ngin</a> . Total environment restoration in one click. Instantly reset 
│   │        │   └──  theme, UI visibility, terminals, tabs, view focus and more
<!-- BROKKR -->│   │        ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BROKKR.md"><img src="https://img.shields.io/badge/BROKKR%20V2-86198f?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPCFET0NUWVBFIHN2ZyBQVUJMSUMgIi0vL1czQy8vRFREIFNWRyAxLjEvL0VOIiAiaHR0cDovL3d3dy53My5vcmcvR3JhcGhpY3MvU1ZHLzEuMS9EVEQvc3ZnMTEuZHRkIj4KPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZlcnNpb249IjEuMSIgd2lkdGg9IjE5cHgiIGhlaWdodD0iMjRweCIgc3R5bGU9InNoYXBlLXJlbmRlcmluZzpnZW9tZXRyaWNQcmVjaXNpb247IHRleHQtcmVuZGVyaW5nOmdlb21ldHJpY1ByZWNpc2lvbjsgaW1hZ2UtcmVuZGVyaW5nOm9wdGltaXplUXVhbGl0eTsgZmlsbC1ydWxlOmV2ZW5vZGQ7IGNsaXAtcnVsZTpldmVub2RkIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayI+CjxnPjxwYXRoIHN0eWxlPSJvcGFjaXR5OjAuNjAxIiBmaWxsPSIjMDAwMDAwIiBkPSJNIDguNSwyLjUgQyAxMS42MjMxLDcuMzIyMTYgMTQuMjg5NywxMi40ODg4IDE2LjUsMThDIDE1Ljk3NDcsMTguNjkyNCAxNS4zMDgxLDE5LjE5MjQgMTQuNSwxOS41QyAxMS4zMDA5LDEzLjQ5NTYgNy42MzQyNiwxMy40OTU2IDMuNSwxOS41QyAyLjUsMTkuMTY2NyAxLjgzMzMzLDE4LjUgMS41LDE3LjVDIDQuMTIwNzIsMTIuNTk0MSA2LjQ1NDA1LDcuNTk0MDkgOC41LDIuNSBaIE0gOC41LDguNSBDIDEwLjczODgsMTAuMDAxMiAxMC43Mzg4LDExLjMzNDUgOC41LDEyLjVDIDcuNzA4NCwxMS4zMDAyIDcuNzA4NCw5Ljk2NjkgOC41LDguNSBaIi8+PC9nPgo8L3N2Zz4K&logoColor=fff"></a> Global, Profile and Workspace context intelligent 
<!-- BROKKR -->│   │        ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BROKKR.md">BROKKR Viewer</a> .................. Quickly change current layout
<!-- BROKKR -->│   │        └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BROKKR.md">BROKKR Menu</a> .................... Consolidated UI manipulation
│   │     
<!-- AUTO GENERATED ITEMS -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#auto-generated-items">Auto-Generated Items</a> ................. Automatically generated VFS items
<!-- Virtual Filing System -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md">Virtual Filing System</a> ................ Core VFS Engine 
<!-- Files & Navigation -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#files--navigation">Files & Navigation</a> ................... File management and navigation
<!-- Commands & Automation -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#commands--automation">Commands & Automation</a> ................ Command execution and automation workflows
<!-- Terminal Commands -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#terminal-commands">Terminal Commands</a> .................... Terminal command integration
<!-- Utilities -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#utilities">Utilities</a> ............................ Utility functions and helpers
<!-- Project Agnostic Setup -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#project-agnostic-setup">Project Agnostic Setup</a> ............... Framework-agnostic configuration 
<!-- move vfs item -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md">📄 Move Item</a> ............................ Move items with ease 
<!-- copy workspace folder -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#copy-workspace-folder"><img src="https://img.shields.io/badge/♦%20Copy%20workspace%20folder-ca8a04?style=plastic"></a> ..................... Provides a list of folders contained within other configs, 
│   │    └──  once clicked pastes it into the current configs file
│   │     
<!-- AUTOPORT NGIN -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/♠%20Backup To Github-86198f?style=plastic"></a> ......................... Saves a backup to a github repo that includes
│   │   ├── all workspace configs and your global config. I don't know why I thought of this  
│   │   ├── because its not really a necessity by any means. But more of an offsite
│   │   ├── back up, to protect against unforeseen issues, like your computer failing.
│   │   ├── As of now, if that were to happen there is currently no means to restore
│   │   ├── your configs or anything else that pertains to this extension. Which is why I have
│   │   ├── already started and have plans to continue moving the storage of features to github
│   │   ├── such as the snippets. But again, this extension does not NEED this type of feature
│   │   └── and is more of an insurance policy.
<!-- AUTOPORT NGIN -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/♠%20Auto-Port%20Ngin-86198f?style=plastic"></a> .......................... Provide the entire powershell command 
│   │   ├── replacing the port number with ${PORT}  
│   │   ├── so wheenver you have a project that takes up a lot of running servies on ports, instead of assigning
│   │   ├── with possible collission, it auto assigned ports, and auto creates new terminals to run them in,
│   │   └── unless args.concurrent: true
<!-- CHANGELOG NGIN -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/♠%20Changelog%20Ngin-86198f?style=plastic"></a> .......................... Parse commits since last release
│   │   ├── Generate changelog markdown, Group by type (feat/fix/breaking), Update version numbers
│   │   └── also plan on doing a readme variant as well
<!-- FAKER NGIN -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/♠%20Faker%20Ngin-86198f?style=plastic"></a> .............................. Grabs your workspaces schema file and automatically 
│   │   ├── creates a file that generates
│   │   ├── data for all schema declarations that can be called in your seed file
│   │   ├── Ensures that the automated mock data generation stays seperate from your projects code 
│   │   └── instead of implementing it into it
<!-- ARTIFACT CACHE MGR -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/♠%20Arftifact%20Cache%20Mgr-86198f?style=plastic"></a> ........................ A package manager cache available in any workspace  
│   │   ├── Architecture
│   │   │    ├── projects.cache
│   │   │    ├── modules.cache
│   │   │    └── extensionStorage
│   │   │        └── node-modules-cache
│   │   │            ├── react@18.2.0/
│   │   │            └── react@18.3.1/
│   │   └── hijacks install process
│   │         ├── scanning local registry and use local matches first before downloading any other libraries 
│   │         ├── installing them into the registry to be used in your project. places all new modules in ext 
│   │         ├── folder and registry. Once installation has been completed triggers background process to 
│   │         ├── scan all other projects leveraging the system and matching the registy with the current state
│   │         ├── of each projects package data, ensuring nothing gets stale and libraries that are no longer in use
│   │         └── are removed from your file system
│   │        
│   ├── 📂 CONFIGURATION_AND_MORE/
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#complete-example">Complete Example</a> ................. Production configuration walkthrough
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#usage--previews">Usage & Previews</a> ................. Examples and previews
│   │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#extended-usage-preview"><img src="https://img.shields.io/badge/♠%20Extended%20Usage%20Preview-86198f?style=plastic"></a> ................ Recorded session proving zero performance losses
│   │   │    └── despite having 100+ extensions worth of functions.
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#getting-started-w/-chains">Getting Started w/ Chains</a> ........ Chain automation guide
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG_EXAMPLES.md">Config Items Examples</a> ............ Production configuration walkthrough
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#extension-configuration">Extension Configuration</a> .......... Extension settings overview
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#configuration-settings">Configuration Settings</a> ........... Core extension settings
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#core-settings">Core Settings</a> .................... Core extension settings
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#code-snapshot-settings">Code Snapshot Settings</a> ........... Core extension settings
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#github-integration">GitHub Integration</a> ............... Single click multi function operations
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#build--automation-settings">Build & Automation Settings</a> ...... The lack of non-automation
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#ui--interface-settings">UI & Interface Settings</a> .......... Core extension settings
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#feature-toggles">Feature Toggles</a> .................. Feature flags and toggles 
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#copy-path">Copy Path</a> ........................ Path copying utilities
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#reveal-in-explorer">Reveal In Explorer</a> ............... File explorer integration
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#search">Search</a> ........................... Search functionality for config items
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#edit-json-config">JSON Config Editor</a> ............... Edit .json configs directly
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#share-config">Share Config</a> ..................... Bulk sharing
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#share-config">Import / Export Config</a> ........... Allows backups, and more
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#view-config-example">View Config Example</a> .............. Configuration examples
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#default-apps">Default Apps</a> ..................... App configurations
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#default-apps">ESLint & Prettier Configs</a> ........ App configurations
│   │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#remote-resource-mgmt"><img src="https://img.shields.io/badge/♠%20Remote%20Resource%20Mgmt-86198f?style=plastic"></a> ................ Profiles for configs: save/download/edit </span>
│   │   └── 📄<a href="#architecture-notes">Architecture Notes</a> ................ Breaking down the inner workings of the extension
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#environment-variable-integration">Env Var Integration</a> .......... using .env vars
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#modular-function-building">Modular Func. Building</a> ....... Exposing more functions to use
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#the-philosophy-of-automation">Automation Principles</a> ........ How it came to be 150+ extensions
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#the-autorun-system">The Autorun System</a> ........... Help with build processes
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#dynamic-package-manager-detection">Dynamic Package Manager</a> ...... Scan for your package mgr at execution time
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#intelligent-terminal-command-engine">Terminal & Command Ngin</a> ...... The breakdown
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#concurrent-and-chain">Concurrent And Chain</a> ......... What can be acheived
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#autonomous-maintenance">Autonomous Maintenance</a> ....... Removing the dev from the equation
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#naming-conventions">Naming Conventions</a> ........... So as to not have to include docs, for every single thing
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#settings-migration">Settings & Migration</a> ......... 
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#pro7">pro7</a> ......................... Password protected that can be pushed 
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#local-encryption">Local Encryption</a> ............. 
│   │        ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#context">Context</a> ...................... 
│   │        └── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md#vsix-archiver">VSIX Archiver</a> ................ Custom less restrictive archiving tool
│   │  
│   ├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CUSTOM_FUNCTIONS.md">CUSTOM_FUNCTION_BREAKDOWNS</a>/
│   │   └── 📄 Order 1 through # ............... Step by step breakdown on executing order #
│   │
│   └── 📂 SIDEBARS_AND_VIEWS/
│       │   └── All status bar menus and functionality has been replaced by a sidebar view feature
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">Clipboard History Pro</a> ........... Provides a history of your clipboard use
│       │   └── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> Fuzzy search while increasing the amount of the total history
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">Bookmarks</a> ....................... Bookmark anything, anywhere
│       │   └── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> Fuzzy search while increasing the amount of the total amount of bookmarks
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">BALDR Icons</a> ..................... React icons, inserts at cursor / copies to clipboard
│       │   └── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> Fuzzy search 
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">MIÐGARÐR UI</a> ..................... Copies to clipboard one of 2500+ components
│       │   └── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> Fuzzy search 
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">DevStack</a> ........................ Main sidebar containing vscode and devstack functions 
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">Custom Search</a> ................... Replacing vscodes default search
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">Errors</a> .......................... Replacing vscodes default error view in the panel
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">BROKKR Menu</a> ..................... For all your UI needs
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">BROKKR Editor</a> ................... Allows quick edit to your current layout config
│       │   └── works surprising well, and personlly gets way more use out of it than I first thought
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">To Do</a> ........................... To do list that uses github as a source of truth
│       │   ├── While technically notes, reminders and post its will at first be covered under to do
│       │   ├── I have found I enjoy using them much more when they are split up, you can do this
│       │   └── clicking on each of the title panes and dragging them over to the activity bar.
│       │   └── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> Fuzzy search 
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">Notes</a> ........................... Notes that uses github as a source of truth
│       │   └── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> Fuzzy search 
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">Reminders</a> ....................... Reminders that uses github as a source of truth
│       │   └── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> Fuzzy search 
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">Post its</a> ........................ A scratch pad, if you will for notes, saves locally
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">FREYR: Color Wheel</a> .............. Provides a in app color wheel and eye dropper 
│       │   ├── to capture colors. The eye dropper itself is not coded into the extensions codebase.
│       │   ├── Instead, when you trigger the eye dropper it sends an http request to the partnering
│       │   ├── site, which then triggers the eye dropper. Whenever you capture a color it relays
│       │   ├── the data back to the vscode instance for use within your code. The end result
│       │   ├── being a ux in which it feels as if the eye dropper is infact from vscode.
│       │   ├── This is due to vscodes sandbox, if this process was not implemented the eye dropper
│       │   └── would cease to exist the second your cursor leaves vscode.
│       └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md">HEIMDALLR</a> ....................... Devoted to github cli wrapper and all things projects
│           ├── List of features that has merged into this sidebar:
│           ├── @a5gard/asgard
│           ├── github cli wrapper
│           ├── @a5gard/bifrost
│           ├── @a5gard/bifrost-plugin
│           ├── @a5gard/baldr - main npm library still exists but can now be installed via sidebar
│           ├── @a5gard/midgardr-cli - same as previous
│           └── and more...
│
├── 📂 ASGARD/
<!-- LOKI -->│   ├──  <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/LOKI.md"><img src="https://img.shields.io/badge/LOKI%20/-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij4KPHBhdGggZD0iTTAgMCBDMC42NiAwIDEuMzIgMCAyIDAgQzIuMjA2MjUgMC45MDc1IDIuNDEyNSAxLjgxNSAyLjYyNSAyLjc1IEM0LjMyMDQwNzkgNi43NTczMjc3NiA2LjI3NTQ5Nzg0IDcuODk0ODQ2NjEgMTAgMTAgQzguODkyNDIzNzggMTIuOTE5OTczNjcgOC4yMjE4NjQxNSAxMy44NzU1Mzk2MiA1LjQzNzUgMTUuNDM3NSBDMi43NDU2OTcxNSAxNi43OTA2MjcxMiAyLjc0NTY5NzE1IDE2Ljc5MDYyNzEyIDIuMTg3NSAxOS42ODc1IEMyLjEyNTYyNSAyMC40NTA2MjUgMi4wNjM3NSAyMS4yMTM3NSAyIDIyIEMxLjM0IDIyIDAuNjggMjIgMCAyMiBDMCAxNC43NCAwIDcuNDggMCAwIFogTTIgOCBDMiA5Ljk4IDIgMTEuOTYgMiAxNCBDMy4zMiAxMy4zNCA0LjY0IDEyLjY4IDYgMTIgQzYgMTEuMzQgNiAxMC42OCA2IDEwIEM0LjY4IDkuMzQgMy4zNiA4LjY4IDIgOCBaICIgZmlsbD0iIzAwMDAwMCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNywxKSIvPgo8L3N2Zz4K"></a> .............................. AI
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/LOKI.md">Deterministic AI Ngin Compiler</a> .. Removing 99% of problems you face as a dev when working
│   │   │    └── with prompts
│   │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/LOKI.md"><img src="https://img.shields.io/badge/✓%20LOKI%20Prompt-059669?style=plastic"></a> ....................... `A Deterministic AI Engine Compiler` prompt 
│   │   │    └──  and creating a DX that cannot be found anywhere else
│   │   └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/LOKI.md"><img src="https://img.shields.io/badge/✓%20LOKI%20Limitless-059669?style=plastic"></a> ...................... Working outside of the data set 
│   │   └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/LOKI.md">Documenation Builder</a> ............... I do not currently know how to come up with a solution 
│   │       └── for this at this time, since AI truly does not shine in this dept
│   │
<!-- =============================== THOR =============================== -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md"><img src="https://img.shields.io/badge/THOR%20/-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij4KPHBhdGggZD0iTTAgMCBDMC42NiAwIDEuMzIgMCAyIDAgQzIuMjA2MjUgMC45MDc1IDIuNDEyNSAxLjgxNSAyLjYyNSAyLjc1IEM0LjMyMDQwNzkgNi43NTczMjc3NiA2LjI3NTQ5Nzg0IDcuODk0ODQ2NjEgMTAgMTAgQzguODkyNDIzNzggMTIuOTE5OTczNjcgOC4yMjE4NjQxNSAxMy44NzU1Mzk2MiA1LjQzNzUgMTUuNDM3NSBDMi43NDU2OTcxNSAxNi43OTA2MjcxMiAyLjc0NTY5NzE1IDE2Ljc5MDYyNzEyIDIuMTg3NSAxOS42ODc1IEMyLjEyNTYyNSAyMC40NTA2MjUgMi4wNjM3NSAyMS4yMTM3NSAyIDIyIEMxLjM0IDIyIDAuNjggMjIgMCAyMiBDMCAxNC43NCAwIDcuNDggMCAwIFogTTIgOCBDMiA5Ljk4IDIgMTEuOTYgMiAxNCBDMy4zMiAxMy4zNCA0LjY0IDEyLjY4IDYgMTIgQzYgMTEuMzQgNiAxMC42OCA2IDEwIEM0LjY4IDkuMzQgMy4zNiA4LjY4IDIgOCBaICIgZmlsbD0iIzAwMDAwMCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNywxKSIvPgo8L3N2Zz4K"></a> .............................. THOR and Tailwind
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md">THOR</a> ............................. Put as simply as I can, recreating tailwind but thinking of the
│   │   │    ├── user first. ie, one click installation and configuration of a basic set up 
│   │   │    └── in order to get the user started.
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#tailwind.config.js">tailwind.config.js</a> .............. Creates a basic config file
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#tailwind.config-preset-ngin">tailwind.config Preset Ngin</a> ..... 46,060+ configurations available
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#tailwind.css">tailwind.css</a> .................... Pre-configured THOR file
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#postcss.config.js">postcss.config.js</a> ............... Basic postcss file
│   │   └── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">PLUGINS/</a> ....................... Tailwind Plugin Ngin
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Tailwind V4 Plug-in</a> 
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Neumorphism</a> 
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Spotlight Effect</a> 
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Text Gradients</a> 
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Animations</a> 
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Animated Gradient Borders</a> 
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Matrix/Rain Effect</a> 
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Flip Card</a> 
│   │        ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">Glassmorphism</a> 
│   │        └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/THOR.md#plugins">And more...</a> 
│   │
<!-- =============================== ICONS =============================== -->│   ├── <a href="https://catalyst-software.vercel.app/asgard/midgardr/home/Icons"><img src="https://img.shields.io/badge/📂%20BADLR%20/-0284c7?style=plastic"></a> .............................. React icon library
│   │   ├── 📄 <a href="https://www.npmjs.com/package/@a5gard/baldr">Icons NPM Package</a> ............... Package integration
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ICONS.md">Icons Quick Pick</a> ................ Icon selection tool
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ICONS.md">Icons Sidebar</a> ................... Copies icon to clipboard
│   │   └── 📄 <a href="https://catalyst-software.vercel.app/asgard/midgardr/home/Icons">Icons</a> ........................... Rendered icons provided via library
│   │ 
<!-- MIÐGARÐR CATALYST UI -->│   └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md"><img src="https://img.shields.io/badge/📂%20MIÐGARÐR SDK%20/-0284c7?style=plastic"></a> ........................... React UI components library
│       ├── <img src="https://img.shields.io/badge/❕%20NOTE%20-6b21a8?style=plastic"> Hosts features that are found in the extension and the ui site
│       ├── 📂 VSCode Extension
│       │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#hephaestus-ui">MIÐGARÐR UI</a> ................. Component library core
│       │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#editor-context-insert">Editor Context Insert</a> ....... Context menu component insertion
│       │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#quick-pick-insert">Quick Pick Insert</a> ........... Quick pick component insertion
│       │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#automated-installation">Automated Installation</a> ...... Install library through extension
│       │   │    └── 📄 <a href="https://www.npmjs.com/package/@a5gard/migardr-ui">NPM Listing</a> ............ Docs outlining the library
│       │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#in-editor-comp-autocomplete">In Editor Comp Autocomplete</a> ...... Type '<' followed by the start of the components name 
│       │   │   └── `Bu...` → suggests Button with full docs
│       │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#smart-prop-autocomplete">Smart Prop Autocomplete</a> ......... Shows props with type-aware snippets 
│       │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#signature-help">Signature Help</a> ................. Live tooltip showing all props as you type inside a 
│       │   │   ├── component's props - providing you with the available parameters/props for each  
│       │   │   └── component as you type 
│       │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#hover-documentation">Hover Documentation</a> ............ Hover over component for full docs and examples  
│       │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#auto-import">Auto import</a> ................... Quick fix to add missing imports  
│       │   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#go-to-definition">Go To Definition</a> ................ Jump to component source  
│       │   └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#missing-import-warnings"><img src="https://img.shields.io/badge/📄%20Missing%20import%20warnings%20-0284c7?style=plastic"></a> .......... Diagnostic warnings for imported components 
│       │
<!-- TOOL SUITE -->│       └── <a href="https://catalyst-software.vercel.app/asgard/midgardr/home/list"><img src="https://img.shields.io/badge/📂%20TOOL_SUITE%20/%20-0284c7?style=plastic"></a> ...................... All the tools we use, just in one place
|           |      └── All tools are available via clicking on the home pages hero or sidebar
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Theme Builder</a> ............... Not your standard theme builder
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Color Wheel</a> ................. Compact UI, entire wheel fits within browser
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Color Converter</a> ............. Standard color converter
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">X Tester</a> .................... Test components featured in the new category
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">playground</a> .................. React, tailwind live playground
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Icons</a> ....................... Displays react icons feature in Baldr
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Typography Tester</a> ........... Live typography manipulator
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Layout Generator</a> ............ Generate layouts for your apps pages
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">MD Reference</a> ................ Very expanded upon md reference sheet
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">VSCode Cmd Reference</a> ........ Contains every currently available cmd, with desc
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Components Reel</a> ............. Move reel of components
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Code Carousel</a> ............... Same as above but with its code
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">ENCODER_DECODER_LAB/</a> ........ Featuring several encoding/decoding types
│           |    ├── 📄 PNG to Base64 
│           |    ├── 📄 JPG to Base64 
│           |    ├── 📄 WEBP to Base64 
│           |    ├── 📄 PDF to Base64 
│           |    ├── 📄 Base64 to PNG 
│           |    ├── 📄 Base64 to JPG 
│           |    ├── 📄 Base64 to WEBP 
│           |    ├── 📄 Base64 to PDF 
│           |    ├── 📄 CSV to JSON 
│           |    ├── 📄 PNG to SVG 
│           |    ├── 📄 JPG to SVG 
│           |    ├── 📄 WEBP to SVG 
│           |    └── 📄 MP4 to MP3 
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Tailwind Converter</a> .......... convert v3 - v4 tailwind configs
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Apollo</a> 
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Loki</a> 
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Regex Tester</a> ................ Test and build regex strings
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">JSON Formatter & Validator</a> .. Standard web json validator and formatter
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">API Response Mocker</a> ......... Create mock api responses
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Lorem Ipsum Generator</a> ....... Generators text based on given parameters
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Cron Expression Builder</a> ..... Standard web cron builder
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">UUID Hash Generator</a> ......... Provides you with random hashes to use
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Code Diff Viewer</a> ............ Syntax highlighting diff viewer
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Flexbox Sandbox</a> ............. Test different flexbox configurations in a live env
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Grid Sandbox</a> ................ Same as previous but with grid
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">QR Code Generator</a> ........... QR's created via provided text, image, etc
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Responsive Preview</a> .......... Quick check on your pages responsiveness
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Accessibility Checker</a> ....... Checks your codes current accessibility
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Animation Builder</a> ........... Live env to quickly build animations
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Chart Playground</a> ............ A fast chart builder, outputs configs and code
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">MD Badge Builder</a> ............ Live builder for custom md badges
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Spinner Generator</a> ........... Terminals and spinners
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Terinal Menu Generator</a> ...... More terminals
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Gradients</a> ................... Gradient generator
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">v4 to v3</a> .................... v4 to v3 tailwind theme converter
│           ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md">Mathmatical Color Picker</a> .... Perfect themes, with as little as 4 colors
<!-- MONACO EDITO SKALDR -->│           └── <img src="https://img.shields.io/badge/📂%20SKÁLD%20/%20-0284c7?style=plastic"></a> ...................... Monaco-level editor
│                ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MIÐGARÐR-SDK.md#auto-import">Documentation</a> 
│                ├── <a href="https://catalyst-software.vercel.app/asgard/misgardr/skald">Editor</a>  
│                └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Feature Set</a>  
│                     ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Readme Generator</a> ...... Feature-rich readme builder 
│                     ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Readme Templates</a> ...... Includes several pre-made templates to start from
│                     ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Remote Access</a> ......... Connect remotely to workspace MD files
│                     ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Local Settings</a> ........ Locally saved editor settings
│                     ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">MD Reference</a> .......... In Editor MD Reference Sheet, 200+ references
│                     └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">PRE_MADE_ASSETS/</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">File Trees</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Progress Bars</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">ASCII Tables</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Spinners</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Terminal Dashboards</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Code Block Previews</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Terminal Menus</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Terminal Logs</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Git Branch Viz</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Status Indicators</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Notification Boxes</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Output Separators</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Nested Data</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Activity Timeline</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Terminal Dashboards</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Box Drawing</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Badges and Logos</a> 
│                          ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Terminal Menus</a> 
│                          └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SKÁLD.md">Special Chars</a> 
<!-- SAGA - TODO NOTES AND REMINDERS  -->│
├── <a href="https:m//github.com/8an3/midgardr-notes/blob/main/docs/HEIMDALLR.md"><img src="https://img.shields.io/badge/📄%20SAGA%20%20-059669?style=plastic"></a> ..................................... To dos, notes, reminders and post it notes
│    └── Recently merged, 2-3 of its least used functions not working
<!-- HEIMDALLR -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/.md"><img src="https://img.shields.io/badge/✗%20HEIMDALLR-EF4444?style=plastic"></a> ................................. React performance functions designed to help
<!-- HEIMDALLR: HÖFUÐ -->│    │  └──  around several areas. Queuing, batching, throttling and rate limiting. 
<!-- HEIMDALLR: HÖFUÐ -->│    └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#export-index-ngin">HÖFUÐ</a> ............................... Intellisense Schema Ngin
<!-- EXPORT INDEX CREATER -->├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#export-index-ngin">Export Index Creator</a> ..................... Export index creator
<!-- NAMED EXPORT INDEX CREATER -->├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CONFIG.md#named-export-index-ngin">Named Export Index Creator</a> ............... Named export index creator
<!-- LEFT OFF NOTE -->├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/WORKSPACE_CONTEXT.md#left-off-note">Left Off Note</a> ............................ Session note tracking
<!-- HERCALES BATCH RENAME -->├── <a href="#down"><img src="https://img.shields.io/badge/📄%20HERACLES-0284c7?style=plastic"></a> ................................. Batch Rename - Bulk renaming
<!-- FILE NESTING -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/UTILS.md#file-nesting"><img src="https://img.shields.io/badge/✗%20File%20Nesting-EF4444?style=plastic"></a> ................................. Nesting configuration
<!-- CUSTOM VSIX -->├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ARCHIVE.md#vsix-archiver">VSIX Archiver</a> ............................ Custom extension packaging 
<!-- CUSTOM VSIX -->│    ├── <img src="https://img.shields.io/badge/♦%20-ca8a04?style=plastic"> Adding the ability to configure the archiver to also copy certain files over to 
<!-- CUSTOM VSIX -->│    └── specfified locations after the compilation process has completed
<!-- PUSH VSIX -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ARCHIVE.md#vsix-publisher"><img src="https://img.shields.io/badge/📄%20Custom%20.vsix%20publisher-0284c7?style=plastic"></a> ........................ Accompanying the above archiver
<!-- Region Folding -->├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/UTILS.md#region-folding">Region Folding</a> ........................... Fold/toggle region folding
<!-- RATATOSKR -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/UTILS.md#ratatoskr"><img src="https://img.shields.io/badge/🌲%20RATATOSKR%20-0284c7?style=plastic"></a> ................................ File tree builder & virtualizer 
<!-- SVG TO WOFF -->├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/UTILS.md#svg-to-woff">SVG To WOFF Converter</a> .................... Convert entire folders into useable woff font file
│
<!-- MARKDOWN -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MARKDOWN.md">MARKDOWN</a>/ 
<!-- MD Viewer/Renderer -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MARKDOWN.md#md-viewer/renderer">MD Viewer/Renderer</a> ................... Standard Markdown viewing
<!-- MD Viewer In VS Code -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MARKDOWN.md#md-viewer-in-vs-code">MD Viewer In VS Code</a> ................. Native VS Code integration
<!-- Convert MD to Safe String -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MARKDOWN.md#convert-md-to-safe-string">Convert MD to Safe String</a> ............ Markdown to safe inline string
<!-- Markdown Cheat Sheet -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MARKDOWN.md#markdown-cheat-sheet">Markdown Cheat Sheet</a> ................. Markdown reference
<!-- Markdown Pre-Processor -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MARKDOWN.md#markdown-pre-processor">Markdown Pre-Processor</a> ............... Converting variables, table structures, toc's
<!-- RÚNAR - SNIPPETS - CODE SNAPSHOT -->│
├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/RÚNAR.md"><img src="https://img.shields.io/badge/RÚNAR%20/%20-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBzdGFuZGFsb25lPSJubyI/Pgo8IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDIwMDEwOTA0Ly9FTiIKICJodHRwOi8vd3d3LnczLm9yZy9UUi8yMDAxL1JFQy1TVkctMjAwMTA5MDQvRFREL3N2ZzEwLmR0ZCI+CjxzdmcgdmVyc2lvbj0iMS4wIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiB3aWR0aD0iMjQuMDAwMDAwcHQiIGhlaWdodD0iMjQuMDAwMDAwcHQiIHZpZXdCb3g9IjAgMCAyNC4wMDAwMDAgMjQuMDAwMDAwIgogcHJlc2VydmVBc3BlY3RSYXRpbz0ieE1pZFlNaWQgbWVldCI+CjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuMDAwMDAwLDI0LjAwMDAwMCkgc2NhbGUoMC4xMDAwMDAsLTAuMTAwMDAwKSIKZmlsbD0iIzAwMDAwMCIgc3Ryb2tlPSJub25lIj4KPHBhdGggZD0iTTcwIDEyMCBjMCAtNjAgNCAtMTAwIDEwIC0xMDAgNiAwIDEwIDE3IDEwIDM4IGwwIDM3IDM0IC00MCBjMTkgLTIyCjM3IC0zOCA0MCAtMzUgMyAzIC0xMyAyNiAtMzQgNTIgbC00MCA0NiA0MSAyNyA0MSAyNyAtMzggMjQgYy02MiAzOCAtNjQgMzYKLTY0IC03NnogbTcwIDUwIGMwIC00IC0xMSAtMTIgLTI1IC0xOCAtMjQgLTExIC0yNSAtMTAgLTI1IDE4IDAgMjggMSAyOSAyNQoxOCAxNCAtNiAyNSAtMTQgMjUgLTE4eiIvPgo8cGF0aCBkPSJNMjE5IDE3MyBjLTEzIC0xNiAtMTIgLTE3IDQgLTQgMTYgMTMgMjEgMjEgMTMgMjEgLTIgMCAtMTAgLTggLTE3Ci0xN3oiLz4KPC9nPgo8L3N2Zz4K"></a> .................................. Snippets Suite
<!-- CODE SNAPSHOT -->│   ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/RÚNAR.md"><img src="https://img.shields.io/badge/✓%20Code%20Snapshot-059669?style=plastic"></a> .......................... Snapshot to terminal window 
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/RÚNAR.md#workspace-context">Workspace Context</a> .................... Context-aware code snippets
<!-- DEVARCHIVE -->│   ├── 📄 <a href="#planned"><img src="https://img.shields.io/badge/♦%20DevArchive-ca8a04?style=plastic"></a> .......................... Perserving knowledge for now, for always
<!-- SNIPPETS SUITE -->│   └── 📄 <a href="https://catalyst-software.vercel.app/asgard/midgardr/runar">Snippets Studio</a> ...................... Create / edit snippets. 
│        ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/RÚNAR.md#visit-documentation">Visit documentation</a> 
│        ├── <a href="https://catalyst-software.vercel.app/asgard/midgardr/runar">Link to Snippets Editor</a> 
│        ├── <a href="https://catalyst-software.vercel.app/asgard/midgardr/runar">Snippet Profiles</a> 
│        ├── <a href="https://catalyst-software.vercel.app/asgard/midgardr/runar">Native Feature Set</a> 
│        └── <a href="https://catalyst-software.vercel.app/asgard/midgardr/runar">Remote Access</a> 
│
<!-- REMIX RUN - HUGINN -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md">HUGINN</a>/ ..................................  remix-run utilities
│   ├── 📂 PROJECT_UTILS/
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#npx-create-remixv2">npx create-remixv2</a> ............... Scaffolding engine
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#v1-->-v2-conversion">V1 -> V2 Conversion</a> .............. Routing migration
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#monorepo-conversion">Monorepo Conversion</a> .............. Single app to monorepo
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#create-single-app">Create Single App</a> ................ React Router setup
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#platform-conversion">Platform Conversion</a> .............. Convert to Platform X
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#create-monorepo">Create Monorepo</a> .................. Monorepo scaffolding
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#build--deploy">Build & Deploy</a> ................... Automation workflow
│   │   └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#rr-folder-routing">RR Folder Routing</a> ................ React Router routing logic
│   │
│   ├── 📂 AUTH_UTILITIES/
│   │   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#install-auth">Install Auth</a> ..................... Authentication setup
│   │   └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#install-otp">Install OTP</a> ...................... One-time password setup
│   │
│   └── 📂 ROUTE_UTILITIES/
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#automatic-action">Automatic Action</a> ................. Remix action generator
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#context-utils">Context Utils</a> .................... Components/Functions
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#browser-integration">Browser Integration</a> .............. Open route file in browser
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#route-file-creator">Route File Creator</a> ............... Create route files
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#test-generator">Test Generator</a> ................... Tests for routes/actions
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#code-insertion">Code Insertion</a> ................... Remix Run insert code
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#error-boundary">Error Boundary</a> ................... Error boundary generator
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#meta-function">Meta Function</a> .................... Meta function utility
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#links-function">Links Function</a> ................... Links function utility
│       ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#preview-route">Preview Route</a> .................... Preview route URL
│       └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HUGINN.md#action-object">Action Object</a> .................... Create action object
│
<!-- PRISMA - MUNINN -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MUNINN.md">MUNINN</a>/ .................................. Prisma utilities
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MUNINN.md#best-practice-guide">Best Practice Guide</a> .................. Prisma best practices
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MUNINN.md#include-object">Include Object</a> ....................... Create include object
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MUNINN.md#schema-navigation">Schema Navigation</a> .................... Click to schema object
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MUNINN.md#crud-resolver-gen">CRUD Resolver Gen</a> .................... Resolvers / REST endpoints
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MUNINN.md#auto-create-schema">Auto Create Schema</a> ................... Automatic schema generation
│   └── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/MUNINN.md#visualizer"><img src="https://img.shields.io/badge/✗%20Visualizer-EF4444?style=plastic"></a> ............................... Schema relations visualization 
│
<!-- SHADCN -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SHADCN.md">SHADCN_UI</a>/
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SHADCN.md#add-components">Add Components</a> ....................... Component addition
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SHADCN.md#install-w/-config">Install w/ Config</a> .................... Component install with configuration
│   └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SHADCN.md#insert-components">Insert Components</a> .................... Component insertion
│
<!-- VOLUNDR -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md">VÖLUNDR</a>/ ................................. cleanup / refactoring / automation
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md#trailing-commas">Trailing Commas</a> ...................... Remove trailing commas
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md#bragi---comment-killer">BRAGI - Comment Killer</a> ............... Remove all comments
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md#console.log-killer">Console.log Killer</a> ................... Remove all console.log
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md#unused-imports">Unused Imports</a> ....................... Remove unused imports
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md#inline-imports">Inline Imports</a> ....................... Inline imports utility
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md#organize-objects-by-value-property">Organize Objects by Value Property</a> ... Organizes objects by value property
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md#json-validator">JSON Validator</a> ....................... Formatting and validation
│   └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VÖLUNDR.md#format-json">Format JSON</a> .......................... Custom formatter
│
<!-- ========================= ODIN ========================= -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#odin"><img src="https://img.shields.io/badge/ODIN%20/%20-0284c7?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij4KPHBhdGggZD0iTTAgMCBDNy4xNzM5MTMwNCAyLjM5MTMwNDM1IDcuMTczOTEzMDQgMi4zOTEzMDQzNSAxMCA1IEMxMCA1LjY2IDEwIDYuMzIgMTAgNyBDNS4yNSA2LjEyNSA1LjI1IDYuMTI1IDMgNSBDMyA1Ljk5IDMgNi45OCAzIDggQzYuNDY1IDkuOTggNi40NjUgOS45OCAxMCAxMiBDMTAgMTIuOTkgMTAgMTMuOTggMTAgMTUgQzUuMjUgMTMuMTI1IDUuMjUgMTMuMTI1IDMgMTIgQzIuNjcgMTUuMyAyLjM0IDE4LjYgMiAyMiBDMS4zNCAyMiAwLjY4IDIyIDAgMjIgQzAgMTQuNzQgMCA3LjQ4IDAgMCBaICIgZmlsbD0iIzAwMDAwMCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNywxKSIvPgo8L3N2Zz4K"></a> .................................... Search & Discovery
<!-- ========================= SEARCH EDITOR ========================= -->│     ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#search-editor">Search Editor</a> ....................... Bespoke search, expanding on vscodes capabilities
│     │    ├── 📄 Remote Editing ................. Make file changes without navigating to the file
│     │    ├── 📄 Configurable Searches .......... Create file tree items that trigger preconfigured searchs at will
│     │    ├── 📄 Regex History & Helper  
│     │    └── 📄 Fuzzy Search 
<!-- ========================= SEARCH SIDEBAR ========================= -->│     ├── <img src="https://img.shields.io/badge/♦%20Text Grabber-ca8a04?style=plastic"> ........................... Copies text to clipboard via manual screen grab
│     │    ├── I want this so bad, but I have seem huge concerns about, exactly how it
│     │    ├── it will function on the backend. As every time I have read on these types
│     │    ├── features, they do not align with anything in regards to the requirements
│     │    ├── needed for a feature to be added into this extension, which means my hopes
│     │    ├── for this are really low. But hey, I've been amazed at the level of laziness before
│     │    └── and lets hope, this falls under one of those times
<!-- ========================= SEARCH SIDEBAR ========================= -->│     ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#file-search-jumper">Search Sidebar</a> ...................... Essentially replaces vscodes default search
<!-- FILE SEARCH JUMPER -->│     ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#file-search-jumper">File Explorer</a> ....................... Finally... no longer have to use the default
<!-- FILE SEARCH JUMPER -->│     ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#file-search-jumper">File Search Jumper</a> .................. Ultra-fast file hopping
<!-- GITHUB TAG NAVIGATOR -->│     ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#github-tag-navigator"><img src="https://img.shields.io/badge/♦%20GitHub%20Tag%20Navigator-ca8a04?style=plastic"></a> ..................... Better UX design nav repos, vers, commits, etc
<!-- FILE LINE JUMPER -->│     ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#file-line-jumper">File Line Jumper</a> .................... Jump to specific coordinates
<!-- DEEP LINK -->│     ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ODIN.md#dependency-deep-link">Dependency "Deep Link"</a> .............. (packageSearch) Jump into node_modules/source
<!-- DEEP LINK -->│     ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md#DEVSTACK-MENU">File and Data Recovery</a> .............. featuring 3 functions to recovery data in vscode
<!-- DEEP LINK -->│     └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SIDEBARS.md#DEVSTACK-MENU"><img src="https://img.shields.io/badge/♦%20Data And File Recovery Sidebar-ca8a04?style=plastic"></a> ........... With the previous bringing some hidden features 
<!-- DEEP LINK -->│         └── to light, one or two of those functions were never meant to be used by users
<!-- DEEP LINK -->│         └── or so it would seem due to how vscode had implemented them for use. To not only 
<!-- DEEP LINK -->│         └── make it easier to use, creating a sidebar devoted to this would let users of all
<!-- DEEP LINK -->│         └── skill levels benefit from this. 
<!-- SHORTCUTS -->├── <details style="display: inline;">│<summary style="cursor: pointer; outline: none; list-style: none; display: inline-block;"><a href="https://github.com/8an3/midgardr-notes/blob/main/docs/SHORTCUTS.md"><img src="https://img.shields.io/badge/⚡%20SHORTCUT%20MAP-0284c7?style=plastic" style="vertical-align: -6px; margin-top: 1px; margin-bottom: -px;" ></a> .............................. ALT + KEY </summary><div style="margin-top: -30px; line-height: 1.4;"> 
│     ├── 📄 [ALT + S] Odin: Search Editor ........ Better-than-native global find
│     ├── 📄 [ALT + D] DevStack QP ................ Main Quick Pick Command Palette
│     ├── 📄 [ALT + I] Icons ...................... Zap: 525+ search-ready icons
│     ├── 📄 [ALT + U] Catalyst UI QP ............. Zap: 2600+ components at cursor
│     ├── 📄 [ALT + S] Context Snippets ........... Context-aware code injection
│     ├── 📄 [ALT + R] Insert region .............. Surgical code blocking
│     ├── 📄 [ALT + E] Insert endregion ........... Close region block
│     ├── 📄 [ALT + W] Wrap w/ region ............. Surround selection with logic
│     ├── 📄 [ALT + Q] Web UI ..................... Launch External Catalyst Dashboard
│     ├── 📄 [ALT + H] History .................... Session & Command history
│     ├── 📄 [ALT + B] Bookmarks .................. Enterprise line-level bookmarks
│     ├── 📄 [ALT + G] GitHub Menu ................ Deep-link & Repo management
│     ├── 📄 [ALT + P] Open Package.json .......... Direct jump to core manifest
│     └── 📄 [ALT + M] Open Readme ................ Direct jump to documentation</div></details>│
<!-- REMIX STACKS -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/CREATE-BIFROST.md"><img src="https://img.shields.io/badge/%20BIFROST-EF4444?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBzdGFuZGFsb25lPSJubyI/Pgo8IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDIwMDEwOTA0Ly9FTiIKICJodHRwOi8vd3d3LnczLm9yZy9UUi8yMDAxL1JFQy1TVkctMjAwMTA5MDQvRFREL3N2ZzEwLmR0ZCI+CjxzdmcgdmVyc2lvbj0iMS4wIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiB3aWR0aD0iMTIuMDAwMDAwcHQiIGhlaWdodD0iMjQuMDAwMDAwcHQiIHZpZXdCb3g9IjAgMCAxMi4wMDAwMDAgMjQuMDAwMDAwIgogcHJlc2VydmVBc3BlY3RSYXRpbz0ieE1pZFlNaWQgbWVldCI+CjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuMDAwMDAwLDI0LjAwMDAwMCkgc2NhbGUoMC4xMDAwMDAsLTAuMTAwMDAwKSIKZmlsbD0iIzAwMDAwMCIgc3Ryb2tlPSJub25lIj4KPHBhdGggZD0iTTggMjM1IGMtNCAtNCA0IC0zMCAxOCAtNTggbDI2IC01MCAtMjUgLTU4IGMtMTQgLTMzIC0yMiAtNjEgLTE3Ci02NCA0IC0yIDE3IDE5IDI5IDQ4IGwyMiA1MiAyMSAtNDcgYzExIC0yNyAyNCAtNDggMjkgLTQ4IDkgMCAtMSAzMiAtMjYgODAKLTE0IDI3IC0xMyAzMyA5IDg0IDE0IDMxIDIxIDU4IDE2IDYxIC00IDMgLTE2IC0xNSAtMjYgLTQwIC05IC0yNSAtMTkgLTQ1Ci0yMyAtNDUgLTMgMCAtMTUgMjEgLTI2IDQ2IC0xMSAyNSAtMjMgNDMgLTI3IDM5eiIvPgo8L2c+Cjwvc3ZnPgo="></a> ................................... Think of remix-stacks, but platform agnostic. 
<!-- REMIX STACKS -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFROST.md"><img src="https://img.shields.io/badge/%20BIFROST%20plugin-EF4444?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBzdGFuZGFsb25lPSJubyI/Pgo8IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDIwMDEwOTA0Ly9FTiIKICJodHRwOi8vd3d3LnczLm9yZy9UUi8yMDAxL1JFQy1TVkctMjAwMTA5MDQvRFREL3N2ZzEwLmR0ZCI+CjxzdmcgdmVyc2lvbj0iMS4wIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiB3aWR0aD0iMTIuMDAwMDAwcHQiIGhlaWdodD0iMjQuMDAwMDAwcHQiIHZpZXdCb3g9IjAgMCAxMi4wMDAwMDAgMjQuMDAwMDAwIgogcHJlc2VydmVBc3BlY3RSYXRpbz0ieE1pZFlNaWQgbWVldCI+CjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuMDAwMDAwLDI0LjAwMDAwMCkgc2NhbGUoMC4xMDAwMDAsLTAuMTAwMDAwKSIKZmlsbD0iIzAwMDAwMCIgc3Ryb2tlPSJub25lIj4KPHBhdGggZD0iTTggMjM1IGMtNCAtNCA0IC0zMCAxOCAtNTggbDI2IC01MCAtMjUgLTU4IGMtMTQgLTMzIC0yMiAtNjEgLTE3Ci02NCA0IC0yIDE3IDE5IDI5IDQ4IGwyMiA1MiAyMSAtNDcgYzExIC0yNyAyNCAtNDggMjkgLTQ4IDkgMCAtMSAzMiAtMjYgODAKLTE0IDI3IC0xMyAzMyA5IDg0IDE0IDMxIDIxIDU4IDE2IDYxIC00IDMgLTE2IC0xNSAtMjYgLTQwIC05IC0yNSAtMTkgLTQ1Ci0yMyAtNDUgLTMgMCAtMTUgMjEgLTI2IDQ2IC0xMSAyNSAtMjMgNDMgLTI3IDM5eiIvPgo8L2c+Cjwvc3ZnPgo="></a> .............................. Plugin system for apps
│  
<!-- VEDRFOLNIR -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/VEÐRFÖLNIR-86198f?style=plastic&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAgAAAAYCAYAAADH2bwQAAAA4mVYSWZJSSoACAAAAAoAAAEEAAEAAAAIAAAAAQEEAAEAAAAYAAAAAgEDAAMAAACGAAAAEgEDAAEAAAABAAAAGgEFAAEAAACMAAAAGwEFAAEAAACUAAAAKAEDAAEAAAACAAAAMQECAAsAAACcAAAAMgECABQAAACoAAAAaYcEAAEAAAC8AAAAAAAAAAgACAAIACwBAAABAAAALAEAAAEAAABHSU1QIDMuMC42AAAyMDI2OjAxOjE3IDA2OjQ1OjM5AAIAEJACAAcAAADaAAAAAaADAAEAAAABAAAAAAAAAC0wNTowMAAAX9fYBQAAAYVpQ0NQSUNDIHByb2ZpbGUAAHicfZG9S8NQFMVPU0XRiohFRBwyVCe7VBHHUsUiWChthVYdTF76BU0akhQXR8G14ODHYtXBxVlXB1dBEPwA8Q8QJ0UXKfG+pNAixguP9+O8ew7v3QcIjQpTza4ooGqWkYrHxGxuVex5hQ9D6McIIhIz9UR6MQPP+rqnbqq7MM/y7vuzBpS8yQCfSBxlumERbxDPblo6533iICtJCvE58ZRBFyR+5Lrs8hvnosMCzwwamdQ8cZBYLHaw3MGsZKjEM8QhRdUoX8i6rHDe4qxWaqx1T/7CQF5bSXOd1jjiWEICSYiQUUMZFVgI066RYiJF5zEP/5jjT5JLJlcZjBwLqEKF5PjB/+D3bM3CdMRNCsSA7hfb/pgAenaBZt22v49tu3kC+J+BK63trzaAuU/S620tdAQMbgMX121N3gMud4DRJ10yJEfy0xIKBeD9jL4pBwzfAn1r7txa5zh9ADI0q+Ub4OAQmCxS9rrHu3s75/ZvT2t+P77hcsVEHzaAAAAACXBIWXMAAC4jAAAuIwF4pT92AAAAB3RJTUUH6gERCy0pwAOmbAAAAyNJREFUKBUBGAPn/AAAAAD/AAAA/wAAAJMAAAADAAAAAAAAAAAAAAAAAAAAAAAAAAD/AAAA9wAAAP8AAACwAAAACgAAAAAAAAAAAAAAAAAAAAD/AAAAmgAAAIAAAAD/AAAAygAAABcAAAAAAAAAAAAAAAD/AAAAmQAAAAAAAABlAAAA+wAAAN4AAAAoAAAAAAAAAAD/AAAAmQAAAAAAAAAAAAAAUAAAAPUAAADsAAAAOwAAAAD/AAAAmQAAAAAAAAAAAAAAAAAAAGEAAAD/AAAAtAAAAAD/AAAAmQAAAAAAAAAAAAAAYAAAAPQAAAD1AAAAVgAAAAD/AAAAmQAAAAkAAACZAAAA/wAAANcAAAAtAAAAAAAAAAD/AAAAvQAAANUAAAD/AAAAoAAAAAsAAAAAAAAAAAAAAAD/AAAA/wAAAPQAAABgAAAAAAAAAAAAAAAAAAAAAAAAAAD/AAAA3AAAACoAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD/AAAAmQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAANYOKaFEGdfWAAAAAElFTkSuQmCC&logoColor=fff"></a> ................................ Resource, hardware & process information 
│    ├── providing information on resources, ports used, etc, a HWInfo for your vscode, if you will. 
│    ├── List views of currently running processes, even background ones, provding info on resource usage
│    ├── port numbers used, quick kill, quick restart buttons.
│    └── Gauges displaying usages for cpu, memory, storage
│ 
<!-- URDER SNAPSHOT NGIN -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/BIFRÖST.md"><img src="https://img.shields.io/badge/URÐR-86198f?style=plastic&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBzdGFuZGFsb25lPSJubyI/Pgo8IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDIwMDEwOTA0Ly9FTiIKICJodHRwOi8vd3d3LnczLm9yZy9UUi8yMDAxL1JFQy1TVkctMjAwMTA5MDQvRFREL3N2ZzEwLmR0ZCI+CjxzdmcgdmVyc2lvbj0iMS4wIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiB3aWR0aD0iMTQuMDAwMDAwcHQiIGhlaWdodD0iMjQuMDAwMDAwcHQiIHZpZXdCb3g9IjAgMCAxNC4wMDAwMDAgMjQuMDAwMDAwIgogcHJlc2VydmVBc3BlY3RSYXRpbz0ieE1pZFlNaWQgbWVldCI+CjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuMDAwMDAwLDI0LjAwMDAwMCkgc2NhbGUoMC4xMDAwMDAsLTAuMTAwMDAwKSIKZmlsbD0iIzAwMDAwMCIgc3Ryb2tlPSJub25lIj4KPHBhdGggZD0iTTcgMjMzIGMtMTMgLTEyIC04IC0yMzMgNCAtMjMzIDggMCAxMCAyOSA2IDEwMCAtMyA1NSAtMyAxMDAgLTIgMTAwCjIgMCAyNyAtNDUgNTYgLTk5IDI5IC01NSA1NiAtOTggNjAgLTk1IDQgMiAtMjAgNTUgLTUzIDExNyAtNjkgMTI5IC02MyAxMTkKLTcxIDExMHoiLz4KPC9nPgo8L3N2Zz4K"></a> ..................................... Snapshot Engine will be deleted, and re-made from the ground up 
│    ├── UI snapshot, that will work cohesively with atlas
│    └── workspace snapshot, taking a snapshot of current file and folder structure and contents
│        └── with rollback function
<!-- FREYR -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md">FREYR</a>/ .................................... VSCode styling
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#blacked-out">Blacked Out</a> ........................... Pre-made black theme 
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#blued-out">Blued Out</a> ............................. Pre-made blue dark mode theme 
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#window-differentiator">Window Differentiator</a> ................. Styling differentiation
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#theme-reset">Theme Reset</a> ........................... Reset window styling
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#themes">Registered Themes</a> ..................... Dark styled themes, 140+ and counting
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#color-wheel">Color Wheel</a> ........................... In app access to the entire color wheel 
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#color-picker">Color Picker</a> .......................... Bespoke DX minded color picker 
│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#themes">File Icon theme</a> ....................... Using providers colored icons
│   ├── 📄 <a href="#planned"><img src="https://img.shields.io/badge/♦%20VSCode Tailwind-ca8a04?style=plastic"></a> ....................... The idea behind this is, using tailwind classnames
│   │    └── in vscode webviews and such without react and without tailwind
│   └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/FREYR.md#themes">Product Icon theme</a> .................... 250+ icons, can be used with config items
│   
<!-- VIDARR -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/AUTOMATION_EVENTS.md">VIÐARR/</a> ................................... Automation events
<!-- AUTO FOLD REGIONS -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/AUTOMATION_EVENTS.md#auto-fold-regions">Auto Fold Regions</a> ..................... Settings-based folding
<!-- FORCED EDIOR GROUPS -->│   └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/AUTOMATION_EVENTS.md#forced-editor-groups">Forced Editor Groups</a> .................. Specific group opening
│
<!-- REGEX-->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/REGEX.md">REGEX</a>/
│    ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/REGEX.md#regex-utilities">Regex Utilities</a> ...................... Advanced Regex Lab & tools
│    └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/REGEX.md#regex-cheatsheet">Regex Cheatsheet</a> ..................... Reference guide
│
<!-- GITHUB-->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/GITHUB.md">HEIMDALLR</a>/ ............................... GitHub
│    ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/GITHUB.md#open-repo-in-browser">Open Github Repo</a> ..................... Open via context menu
│    ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/GITHUB.md#open-repo-at-file">Open GH Repo At File & Line #</a> ........ Opens repo at desired file and line via context menu
│    ├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/GITHUB.md#github-wrapper"><img src="https://img.shields.io/badge/✗%20Github CLI Wrapper Merging into DevStack-EF4444?style=plastic"></a> ........ CLI wrapper, replaces naming convention and single commands only
│    └── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/GITHUB.md#open-repo-at-file">Merging BIFROST NPM Library</a> .......... Once the GH CLI wrapper as been fully merged,
│        ├── then I might as well put bifrost on the chopping block as well as it makes more 
│        ├── to add it to devstack, then not doing so. Platform agnostic installer with full plugin
│        └── system that will allow any user on any platform share through a single source.
│
<!-- TYR -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/TYR.md">TÝR</a>/ ...................................... Port, process and error utilties
<!-- PORT REPEAR -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/TYR.md#portreaper">portReaper</a> ............................ Zombie process killer
<!-- AUTO REAPER -->│   ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/TYR.md#auto-reaper">Auto Reaper</a> ........................... Automatic cleanup
<!-- LOG TO LENS -->│   └── <details style="display: inline;"><summary style="cursor: pointer; outline: none; list-style: none; display: inline-block;"><a href="https://github.com/8an3/midgardr-notes/blob/main/docs/TYR.md#log-to-lens"><img src="https://img.shields.io/badge/♦%20Log%20to%20Lens-ca8a04?style=plastic" style="vertical-align: -6px; margin-top: 1px; margin-bottom: -px;" ></a> .............................. (errorParser) The Pain: Your build failed or your    </summary><div style="margin-top: -15px; line-height: 1.4;"> 
│        ├── test crashed. The terminal is a wall of 500 lines of red text. You have to scroll up, 
│        ├── find the file path in the stack trace, copy it, Ctrl+P, and paste the path to fix the
│        ├── bug. Scans the last output of the integrated terminal for file paths and line numbers.
│        └── It then populates the Navigator with "Jump to Last Error" items. </div></details>│ 
<!-- HERMÓÐR -->├── 📂 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HERMÓÐR.md">HERMÓÐR</a>/
<!-- PRO5 ARCHIVER -->│    ├── 📄<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/ARCHIVE.md#pro7"> Pro7 Archiver</a> ......................... Password protected archive for secrets
<!-- ENV CONTEXT SWAPPER -->│    ├── 📄 <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/UTILS.md#.env-context-swapper">.env Context Swapper</a> .................. (envProfile) Switch environment profiles
<!-- API SECRET GRABBER -->│    └── <details style="display: inline;"><summary style="cursor: pointer; outline: none; list-style: none; display: inline-block;"><a href="https://github.com/8an3/midgardr-notes/blob/main/docs/HERMÓÐR.md"><img src="https://img.shields.io/badge/♦%20API%20Secret%20Grabber-ca8a04?style=plastic" style="vertical-align: -6px; margin-top: 1px; margin-bottom: -px;" ></a> ......................... (vaultFetch) You need a staging/prod API   </summary><div style="margin-top: -15px; line-height: 1.4;"> 
│         ├── key that isn't in your local .env for security reasons. You have to log into AWS 
│         ├── Secrets Manager, 1Password, or  your company Wiki, find the key, and copy it.  A type 
│         ├── that fetches a value from a CLI-based vault (like gh secret, aws secretsmanager, or a 
│         ├── local encrypted file). It executes the CLI fetch and uses your existing copyToClipboard
│         └── logic to put the secret in your hand instantly. </div></details>│ 
<!-- NEMISIS -->├── <a href="https://github.com/8an3/midgardr-notes/blob/main/docs/NEMESIS.md"><img src="https://img.shields.io/badge/📂%20NEMESIS%20/-475569?style=plastic" style="vertical-align: middle; padding-bottom: 2px;"></a>
<!-- CREATE INCOMING TUNNEL -->│     └── <details style="display: inline;"><summary style="cursor: pointer; outline: none; list-style: none; display: inline-block;"><a href="https://github.com/8an3/midgardr-notes/blob/main/docs/NEMESIS.md"><img src="https://img.shields.io/badge/♦%20Create%20Incoming%20Tunnel-ca8a04?style=plastic" style="vertical-align: -6px; margin-top: 1px; margin-bottom: -px;" ></a> .................... The Pain: working on a mobile  </summary><div style="margin-top: -15px; line-height: 1.4;"> 
│          └── Detects SQLite by magic bytes (SQLite format 3\0), Not by extension
│              ├── app or an external API that needs to see your local server. You have to open a  
│              ├── separate terminal, remember your ngrok or localtonet command, copy the new URL, 
│              ├── and paste it into your config. It automates the "copy-paste" loop between the 
│              ├── terminal and your code. A specialized command  that launches a tunnel (like ngrok 
│              ├── http 3000), captures the generated URL, and automatically updates a specific 
│              └── line in your config.ts or .env with the new public URL. The Fix: A tunnelLauncher type.</div></details>│ 
<!-- VALHALLA -->└── <img src="https://img.shields.io/badge/📂%20VALHALLA:%20Database%20&%20Storage%20-475569?style=plastic" style="vertical-align: middle; padding-bottom: 2px;">
<!-- SQLITE3 -->      ├──<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VALHALLA.md"><img src="https://img.shields.io/badge/✗%20React Application%20Layer%20Data%20Store-EF4444?style=plastic"></a> .............. React state management
<!-- SQLITE3 -->      ├──<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VALHALLA.md"><img src="https://img.shields.io/badge/✗%20Application%20Layer%20Data%20Store-EF4444?style=plastic"></a> .................. Non-React state management, replicating the 
      │    └── above manager but for use in apps that don't use react 
<!-- SQLITE3 -->      ├──<a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VALHALLA.md"><img src="https://img.shields.io/badge/✗%20Server and Client%20Layer%20Data%20Store-EF4444?style=plastic"></a> .............. Like tanstack and mbx combined 
<!-- SQLITE3 -->      └── <details style="display: inline;"><summary style="cursor: pointer; outline: none; list-style: none; display: inline-block;"><a href="https://github.com/8an3/midgardr-notes/blob/main/docs/VALHALLA.md"><img src="https://img.shields.io/badge/✗%20Sqlite3-EF4444?style=plastic" style="vertical-align: -6px; margin-top: 1px; margin-bottom: -px;" ></a> ................................. Opens editor / viewer in your vscode editor group </summary><div style="margin-top: -15px; line-height: 1.4;"> 
          └── Detects SQLite by magic bytes (SQLite format 3\0), Not by extension
                ├── Opens .vscdb, .random, .whatever
                ├── Built-in presets for common files:
                │    ├── VS Code state.vscdb
                │    ├── Chrome History/Cookies
                │    ├── Firefox places.sqlite
                │    └── etc.
                ├── Instead of a Webview that you have to "Open with...," use the Custom Editor API so that 
                │    └── clicking a .sqlite or .db file opens your UI immediately.
                ├── Keyboard First: Implement Vim-like or Excel-like navigation (arrow keys to move, Ctrl+N 
                │    └── for new row, Del to mark for deletion). 
                ├── Schema Visualizer (ERD): Automatically generate an Entity Relationship Diagram. 
                ├── Notebook Support: Integrate with VS Code's Native Notebooks
                ├── Direct Export to Code: A button that takes a table or query result and generates the code to
                │    └── access it in Python (Pandas), JavaScript (Drizzle/Prisma), or Rust.
                ├── WASM-based Performance: Use a fast WASM build of SQLite
                ├── Transaction Log & Undo: VS Code users expect Ctrl+Z to work.
                └── Extensions Support: Allow users to load SQLite extensions</div></details> 
</pre>

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Top 7 Features to Try First**

> [!NOTE]
>
> There are a ton of features, which is awesome but since you are just installing this I wanted to provide a list of features to try out first. 
>
> These features will be the most impactful to your overall user experience with vscode because they changed mine, so much so that the idea of switching IDE's is no longer a thought that comes to mind anymore. After the list I'll explain why each one made it on there and what you could expect from them.
>
> > **★☆ If You're New to Development - Start Here First: ☆★**
> > 
> > Before diving into the main features, two recent additions will save you countless hours of frustration:
> > 
> > **1. Heimdallr (GitHub Without the Pain)**  
> > Found in the sidebar as "Heimdallr"—replaces GitHub's confusing terminology and multi-step workflows with single-click operations. Creating a new project and pushing to GitHub? Instead of 3-7 terminal commands plus opening your browser, click "Create Project" once. Done.
> > 
> > **2. Bifröst (Platform Installer)**  
> > Also in the Heimdallr tab—a platform-agnostic installer that sets up entire React projects (Remix, Next, etc.) with all dependencies configured and ready to go. No more "wait, did I install this library?" or "why isn't this working?" It scaffolds everything and opens a new VSCode instance with your project ready.
>
> 1. 𐌀 Atlas: Layout Engine
> 2. ᚱ RÚNAR: Snippet Development Studio
> 3. ᚦ THOR: Tailwind and css, specifically the tailwind.config preset ngin
> 4. ᛒ BIFRÖST: Terminal and Multi Kernel Ngin
> 5. Workspace contexts, despite technically being under the Bifrost umbrella... this in of itself would be its own extension, if it were anyone else building it
> 6. MIÐGARÐR UI: formerly known as catalyst ui
> 6. Odin: Search Editor
>
> I know a couple of those items, do encompass a lot but I'll narrow it down. 
> 
> **𐌀 Atlas:** The only reason why atlas is at the top, is because of the overall reach of its impactfulness it has. Where as all the items do deserve the number one spot, they really do, but I was looking at from the perspective of how many people would each of these feature impact in a positive way, and I beleive the layout engine would be the most impactful to your user experience.
>
> Atlas allows you to easily change your theme, set settings, configuration of editor groups, files open, complete control over your vscode UI, configure shortcuts and more... All the while doing so on a workspace by workspace basis. With workspace contexts you can have one default per workspace, ontop of however many non default layouts you would like. Everytime I open a workspace, I have a complete customized layout, settings configuration, shortcut configuration, theme and so much more. This truly changes of how you would think of vscode, one second your in a layout devoted to front end dev, a couple seconds later your in an entire different enviroment specialized in working on bugs and errors, next min your layout configuration is perfect for back end devs, then you thought of something in which... you now have to open another workspace, upon opening your default layout triggers and opens the workspace in the perfect working enviroment that uses a completely different platform, language, backend and more.
>
> **ᚱ RÚNAR:** Personally... I hated snippets when I first tried them... so much I simply just didn't use that vscode feature at all. This feature turned my experience with snippets on its head as you have a monoca editor to view and edit snippets. Accomponied with a command search so you can scroll and or search for snippets with fuzzy search. Before it took atleast 10 minutes, probably more to be honest to create a single snippet, now with the features in place you can do it in under 10 secs.
>
> **ᚦ THOR:** The tailwind.config preset ngin grants access to 18,000 configurations that control your projects font, theme and preset which adjusts things like padding, margins and etc. Best part about it is, you just paste it into your config file, and only have to adjust 3 variables... thats it, your done.
>
> **ᛒ BIFRÖST:** In terms of impactfulness... personally this has had an even larger impact with me more than anything else, the only reason it didn't beat atlas is because the terminal and multi kernel ngin, while being the best feature in the extension, in order to get the MOST out of it... it does take a while to see just how impactful it truly is. This is due to the fact that, at first you will see a noticeable difference... if you continue working on it, its the steady increase over time that you don't notice till, one day you actually have to type out a command and your sitting there... what was it again? How did I forget that command, I've used it a thousand times in the past... only to come to the realization of just how long its been since you actually had to type it out. While the layout engine, configure it once and your spoiled, the terminal ngin... it's like turning into a spoiled brat over time and not notice it till, it becomes extremely apparent. I'm not kidding when I say this, but there have been times, where I had to manually do something that the ngin does for me, not only do I immediatly get annoyed but I'm sitting there sighing saying to myself, why does it feel like I just went back 10+ years in time in having to do this mannually... god... lol, when npm put out that new requirement for manually pushing packages... I was not in a good mood that day, till I found a way to automate that process again. Which is exposed to you as a user to use as well.
>
> **Workspace contexts:** I know I touched on this already but having everything work cohesively to the point where you can't even discern the line of the switching between contexts. Having a completely different list of items available for each and every workspace, and automatically to top it off. I don't know of a single other extension that does it as well as this one does. I'm not saying that to boost my own ego, because it was a bitch to get perfect. When I say perfect... it's perfect, there are no troubleshooters, even though this extension does not feature a single one throughout all of its features. Every single extension that I have seen attempt to do a good job with context switching between workspaces... all of them have troubleshooters. The best part is, just how many features is able to take advantage of this, really does make is so that it does belong in its own extension.
>
> **MIÐGARÐR UI:** 2500+ components, one command installs the library, tailwind, postcss all the while configuring everything for you, features that make it so you never have to leave vscode... for a single thing in order to use any one component. I'll leave it at that, because there is a lot to unpack with this one if that interested you enough, navigate to its documentation after reading this.
>
> **Odin:** search, I'll admit... you might have to be a bit more on the nerdy side in order to truly appreciate this one, after all... it is just a search function, lol. Buttttt, it does come with some nice features. Using a custom editor you can open as many as you want, all the while each one continues in its current state that isn't effected by any other instance. When browsing your search results, each result is a text area... because you can remote edit any one file, or in any number you need to, once you hit save all... it pushes all the edits you made to their files making it so you never have to navigate to a file in order to change a line or two... or 10. Fuzzy searching, expanded upon regex with pre configured strings to use, and theres even more. All from a simple search function, although the remote editing I have no shame in admiting that I nerd over that feature the most.
>
> Do with that as you will, as I know looking at the list the first time can be overwhelming and I wanted to help you focus down on just a couple of features to start with... and grow from there. The best way to look at this extension is to not think of it as one massive extension and think of it as if vscode received a large update. 
> 
> Yes there are more feautres then you will know what to do with... who cares... they will sit there in the background waiting till you finally have a need to use it, just like so many other default features that ship with vscode.


<br> <br> 
<!-- #endregion -->


<!-- #region LICENSE -->

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **LICENSE**
<br> 

This project is protected under the MIT License. For more details, refer to the [LICENSE](https://raw.githubusercontent.com/8an3/DevStack/blob/main/LICENSE.md) file. 

---

<!-- #endregion  -->

<!-- #region ACKNOWLEDGMENTS -->

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **ACKNOWLEDGMENTS**
<br> 

<div align="center">

![Dotted Map](https://img.shields.io/badge/-dotted--map-000?style=plastic)
![cva](https://img.shields.io/badge/-cva-000?style=plastic)
![y-codemirror](https://img.shields.io/badge/-y--codemirror-000?style=plastic)
![Little Date](https://img.shields.io/badge/-little--date-000?style=plastic)
![KaTeX](https://img.shields.io/badge/-KaTeX-000?style=plastic&logo=katex&logoColor=white)
![Input OTP](https://img.shields.io/badge/-input--otp-000?style=plastic)
![Remark](https://img.shields.io/badge/-Remark-000?style=plastic)
![SerialPort](https://img.shields.io/badge/-SerialPort-000?style=plastic)
![SVG Dotted Map](https://img.shields.io/badge/-SVG%20Dotted%20Map-000?style=plastic)
![Three Globe](https://img.shields.io/badge/-Three%20Globe-000?style=plastic&logo=threedotjs&logoColor=white)
[![THREEDOTJS][THREEDOTJS]](#)

</div>


<div align="center">

![Lexical](https://img.shields.io/badge/-@lexical-000?style=plastic)
![ZXing](https://img.shields.io/badge/-@zxing/library-000?style=plastic)
![Fuse.js](https://img.shields.io/badge/-Fuse.js-000?style=plastic)
![AI SDK](https://img.shields.io/badge/-@ai--sdk-000?style=plastic)
![Three.js](https://img.shields.io/badge/-Three.js-000?style=plastic&logo=threedotjs&logoColor=white)
![Remix Auth](https://img.shields.io/badge/-Remix%20Auth-000?style=plastic&logo=remix&logoColor=white)
[![TAILWINDCSS][TAILWINDCSS]](#)
![Embla](https://img.shields.io/badge/-Embla-000?style=plastic)
![clsx](https://img.shields.io/badge/-clsx-000?style=plastic)
![⌘K](https://img.shields.io/badge/-⌘K-000?style=plastic)
[![GitHub][GitHub]](#)

</div>
<div align="center">

![QR Code](https://img.shields.io/badge/-QR%20Code-000?style=plastic&logo=qrcode&logoColor=white)
![CodeSandbox](https://img.shields.io/badge/-CodeSandbox-000?style=plastic&logo=codesandbox&logoColor=white)
![RADIXUI](https://img.shields.io/badge/-Radix_UI-161618?style=plastic&logo=radixui&logoColor=white)
[![Vercel][Vercel]](#)
[![SHADCN][SHADCN]](#)
[![Remix][Remix]](#)
[![SWR][SWR]](#)
![Catalyst Icons](https://img.shields.io/badge/-Catalyst%20Icons-000?style=plastic&logo=react&logoColor=3b82f6)
![Catalyst THOR](https://img.shields.io/badge/-Catalyst%20CSS-000?style=plastic&logo=zap&logoColor=3b82f6)
![Catalyst UI](https://img.shields.io/badge/-Catalyst%20UI-000?style=plastic&logo=react&logoColor=3b82f6)
</div>

<div align="center">



![React Day Picker](https://img.shields.io/badge/-React%20Day%20Picker-61DAFB?style=plastic&logo=react&logoColor=black)
![React Dropzone](https://img.shields.io/badge/-React%20Dropzone-61DAFB?style=plastic&logo=react&logoColor=black)
![Rehype](https://img.shields.io/badge/-Rehype-2F74C0?style=plastic)
![Node HID](https://img.shields.io/badge/-Node%20HID-339933?style=plastic&logo=node.js&logoColor=white)
![PDF-LIB](https://img.shields.io/badge/-PDF--LIB-E74C3C?style=plastic)
![React Aria](https://img.shields.io/badge/-React%20Aria-61DAFB?style=plastic&logo=react&logoColor=black)
![dnd-kit](https://img.shields.io/badge/-dnd--kit-FF6B6B?style=plastic)
[![POSTCSS][POSTCSS]](#)


</div>

<!-- #endregion -->

<!-- #region COLORED BADGES FULL -->

<div align="center">

![Framer Motion](https://img.shields.io/badge/-Framer%20Motion-0055FF?style=plastic&logo=framer&logoColor=white)
![Monaco](https://img.shields.io/badge/-Monaco-007ACC?style=plastic&logo=microsoft&logoColor=white)
![Headless Tree](https://img.shields.io/badge/-@headless--tree-38B2AC?style=plastic)
![Framer Motion](https://img.shields.io/badge/-Framer%20Motion-0055FF?style=plastic&logo=framer&logoColor=white)
![Yjs](https://img.shields.io/badge/-@yjs-007ACC?style=plastic)
![Scena](https://img.shields.io/badge/-@scena/react--guides-4A90E2?style=plastic)
![JSZip](https://img.shields.io/badge/-JSZip-E34F26?style=plastic)
![PDF-LIB](https://img.shields.io/badge/-PDF--LIB-E74C3C?style=plastic)
</div>

<div align="center">

![Shiki](https://img.shields.io/badge/-Shiki-5E81AC?style=plastic)
![React Fast Marquee](https://img.shields.io/badge/-React%20Fast%20Marquee-61DAFB?style=plastic&logo=react&logoColor=black)
[![CODEMIRROR][CODEMIRROR]](#)
[![AXIOS][AXIOS]](#)
[![D3][D3]](#)
![Rehype](https://img.shields.io/badge/-Rehype-2F74C0?style=plastic)
![Node HID](https://img.shields.io/badge/-Node%20HID-339933?style=plastic&logo=node.js&logoColor=white)
![React Resizable Panels](https://img.shields.io/badge/-React%20Resizable%20Panels-61DAFB?style=plastic&logo=react&logoColor=black)

</div>
<div align="center">

[![Visual Studio Code][Visual Studio Code]](#)
[![Postgres][Postgres]](#)
[![pnpm][pnpm]](#)
[![PowerShell][PowerShell]](#)
[![JavaScript][JavaScript]](#)
[![TypeScript][TypeScript]](#)
![Recharts](https://img.shields.io/badge/-Recharts-FF6384?style=plastic&logo=recharts&logoColor=white)

</div>

<!-- #endregion -->

[**Return**](#-toc)
 
<!-- #region MY BADHES -->
[CODESANDBOX]:https://img.shields.io/badge/-CodeSandbox-151515?style=plastic&logo=codesandbox&logoColor=white
[SHADCN]: https://img.shields.io/badge/-shadcn/ui-000000?style=plastic&logo=shadcnui&logoColor=white
[CODEMIRROR]: https://img.shields.io/badge/-CodeMirror-D30707?style=plastic&logo=codemirror&logoColor=white
[RADIXUI]: ""
[AXIOS]: https://img.shields.io/badge/-Axios-5A29E4?style=plastic&logo=axios&logoColor=white
[D3]: https://img.shields.io/badge/-D3.js-F9A03C?style=plastic&logo=d3dotjs&logoColor=white"
[SWR]: https://img.shields.io/badge/-SWR-000000?style=plastic&logo=swr&logoColor=white"
[POSTCSS]: https://img.shields.io/badge/-PostCSS-DD3A0A?style=plastic&logo=postcss&logoColor=white
[GitHub]: https://img.shields.io/badge/github-%23121011.png?style=for-the-badge&logo=github&logoColor=white 
[TAILWINDCSS]: https://img.shields.io/badge/tailwindcss-0F172A?&logo=tailwindcss
[THREEDOTJS]:https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white
[Vercel]: https://img.shields.io/badge/Vercel-%23000000.png?logo=vercel&logoColor=white
[Visual Studio Code]:https://raw.githubusercontent.com/8an3/midgardr-notes/main/vscodeBadge.png 
[Postgres]: https://img.shields.io/badge/Postgres-%23316192.png?logo=postgresql&logoColor=white
[Remix]: https://img.shields.io/badge/Remix-000?logo=remix&logoColor=fff
[pnpm]: https://img.shields.io/badge/pnpm-F69220?logo=pnpm&logoColor=fff
[TypeScript]: https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=fff
[PowerShell]: https://custom-icon-badges.demolab.com/badge/PowerShell-5391FE?logo=powershell-white&logoColor=fff
[JavaScript]: https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=000
<!-- #endregion -->

<!-- #region OTHER BADHES -->

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.png?style=for-the-badge
[contributors-url]: https://raw.githubusercontent.com/github_username/repo_name/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.png?style=for-the-badge
[forks-url]: https://raw.githubusercontent.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.png?style=for-the-badge
[stars-url]: https://raw.githubusercontent.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.png?style=for-the-badge
[issues-url]: https://raw.githubusercontent.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.png?style=for-the-badge
[license-url]: https://raw.githubusercontent.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.png?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png
<!-- Shields.io badges. You can a comprehensive list with many more badges at: https://raw.githubusercontent.com/inttter/md-badges -->
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 

<!-- #endregion -->











