# BIFROST

> [!IMPORTANT]
> Currently in alpha testing...

Currently in testing, but after its creation it looks as if it will accomplish exactly what I was going for when I first thought of this idea, which was:
- a resource that caters to more than just a single platform
- create a plugin system in which any project can install and use, obviously as long as its platform compatible
- a search and discover system where you can find templates and plugins by either filtering results or search for individual plugins
Platform-agnostic project creator with extensible template system inspired by Remix Stacks.

- [USAGE](#usage)
- [INTERACTIVE MODE](#interactive-mode)
- [CREATING A NEW PROJECT](#creating-a-new-project)
- [CONFIG.BIFROST WIZARD](#config.bifrost-wizard)
- [SUBMIT TEMPLATE](#submit-template)
- [BIFROST-PLUGIN](#bifrost-plugin)
- [INSTALLING A PLUGIN](#installing-a-plugin)
- [LIST AVAILABLE PLUGINS TO INSTALL](#list-available-plugins-to-install)
- [PLUGIN WIZARD](#plugin-wizard)
- [SUBMIT PLUGIN](#submit-plugin)

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Features**

- 🌈 **Platform Agnostic**: Works with any framework (Remix, Next.js, Vite, etc.)
- 📦 **Multiple Package Managers**: Support for npm, pnpm, yarn, and bun
- 🎯 **Git-based Stacks**: Use any GitHub repository as a template
- 🚀 **Interactive CLI**: Guided setup with smart prompts
- ⚡ **Fast Setup**: Clone, configure, and install in seconds
- 🔄 **Auto Git Push**: Optionally push initial commit to GitHub

 
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Interactive Mode**


```bash
bunx @a5gard/bifrost
```

In interactive mode, the following prompts will display:
- Create a new project
- `config.bifrost` wizard
- Submit template to bifrost registry

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Create a new project**

Once you start to the `create a new project process` the follow prompts will guide you:

- What would you like to name your new project?
- Which platform would you like to use? <!-- show the list of platforms, `PLATFORMS` -->
- Do you prefer to use the platforms default install or would you like to opt for a template instead? <!-- show a list displaying two values one for each --> 
  - if templates was chosen, you will be presented with a list of templates relevant to the desired platform 
  - unless the platform has more than one default install, for example remix offers several default starters to choose from at this time that list will be presented for you to choose from
- Which package manager do you prefer?<!-- display a list of pkg mgrs -->
- The remaining questions will be displayed via a toggle item list
  - Would you like tailwind and its requirements to be installed and configured:
    - using the base tailwind config?
    - using the preset ngin?
  - Pre-install MIÐGARÐR UI components?
  - Pre-install @a5gard/baldr icons?
  - Would you like to auto install the projects libraries once the project has initialized?
  - Would you like to auto create and push the first commit to GitHub?


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **config.bifrost wizard**


```bash
bunx @a5gard/bifrost wizard
```

The wizard will help guide you through the process of the templates config file by going over the following questions:
- description
- repo ( if it doesn't sense the data by scanning your project, it will prompt you to push your current project and create a public repo )
- tags that you would like to associate with your template
- post install scripts that are required to run once the project has initialized, providing the npm scripts names in a csv format
- in a csv format, provide any and all plugins that you would like to include with your template to be installed and used with your template'

It will then create config.bifrost for you with the submitted data, and if no values are missing will prompt you, asking if you would like to submit your template at this time. The only requirements for submitting is for the repo to be public and that your template includes the bifrost config file

```json
// config.bifrost
{
  "name": "My Stack",
  "description": "A custom template for X platform",
  "platform": "remix",
  "github": "owner/repo",
  "tags": ["react", "typescript", "tailwind"],
  "postInstall": ["setup", "db:generate"],
  "plugins": ["owner/plugin1", "owner/plugin2"]
}
```

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Submit template**


As long as your project already has a public repo already in place, if not it will prompt you to do so at this time, and the required `config.bifrost`. If you don't currently have the config file, it will start the config wizard to help you create it.

```bash
bunx @a5gard/bifrost submit
```

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Command Flags**


| Flag | Alias | Description |
|------|-------|-------------|
| `--template` | `-s` | Stack to use (format: owner/repo) |
| `--pkg-mgr` | `-p` | Package manager (npm, pnpm, yarn, bun) |
| `--no-install` | | Skip dependency installation |
| `--help` | `-h` | Show help |
| `--version` | `-V` | Show version |
| `--list-templates` |  | List available templates listed within the registry, supplying a platform with the flag will filter the results only listing templates relevant to the desired platform |
| `--wizard` |  | Starts the config wizard |
| `--submit` |  | Submit your template to be saved in the registry |

```bash
bunx @a5gard/bifrost my-app --template owner/repo --pkg-mgr bun
bunx @a5gard/bifrost my-app -s remix-run/indie-template -p bun
bunx @a5gard/bifrost my-app --list-templates
```


### Stack Configuration (Optional)

Add a `config.bifrost` to your repository root for enhanced functionality:

```json
{
  "name": "My Stack",
  "description": "A custom template for X platform",
  "platform": "remix",
  "github": "owner/repo",
  "tags": ["react", "typescript", "tailwind"],
  "postInstall": ["setup", "db:generate"],
  "plugins": ["owner/plugin1", "owner/plugin2"]
}
```


> [!IMPORTANT]
> ## Built to Last
> 
> This resource has been architected with obsolescence by design—a self-sustaining ecosystem using a decentralized package system built entirely on free infrastructure.
> 
> **What this means for you:**
> 
> You don't have to worry about the library going down, shutting down, or experiencing service interruptions due to funding issues, infrastructure failures, or anything happening to me personally.
> 
> Since there are no operational costs:
> - If my finances collapse, your projects keep running
> - If I get hit by a bus tomorrow, you won't even notice
> - If I abandon the project entirely, everything continues working
> 
> Even if this entire project disappeared today, you'd still have:
> - All your templates and plugins (in your repos)
> - The ability to clone and use any community template (via GitHub)
> - Complete ownership of everything you've created
> 
> True decentralization means no single point of failure—including me.


 #bifrost



Platform-agnostic project creator with extensible template system inspired by Remix Stacks.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Features**


- 🌈 **Platform Agnostic**: Works with any framework (Remix, Next.js, Vite, etc.)
- 📦 **Multiple Package Managers**: Support for npm, pnpm, yarn, and bun
- 🎯 **Git-based Stacks**: Use any GitHub repository as a template
- 🚀 **Interactive CLI**: Guided setup with smart prompts
- ⚡ **Fast Setup**: Clone, configure, and install in seconds
- 🔄 **Auto Git Push**: Optionally push initial commit to GitHub

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Interactive Mode**

```bash
bunx create-bifrost
```

In interactive mode, the following prompts will display:
- What would you like to name your new project?
- Which platform would you like to use?
- Which package manager do you prefer?
- Would you like to have the install command run once the project has initialized?
- Would you like to auto create and push the first commit to GitHub?

### With Options

```bash
bunx create-bifrost my-app --template owner/repo --pkg-mgr bun
```

### Full Example

```bash
bunx create-bifrost my-app -s remix-run/indie-template -p bun
```

### Platform Templates

```bash
bunx create-bifrost my-app --list-templates
```

## Options

| Flag | Alias | Description |
|------|-------|-------------|
| `--template` | `-s` | Stack to use (format: owner/repo) |
| `--pkg-mgr` | `-p` | Package manager (npm, pnpm, yarn, bun) |
| `--no-install` | | Skip dependency installation |
| `--help` | `-h` | Show help |
| `--version` | `-V` | Show version |


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Creating Your Own Template**

Any GitHub repository can be used as a template. To make this process easier whenenver you create a project based off of a platforms base installer, a config file will be created for you in order to create and post your own template. If you want to create your own template based off of another, the original templates config will already be located within the root folder. All you have to do is edit the config in order meet your newly created projects use case needs.

```bash
bunx create-bifrost my-app --template name/repo
```

### Stack Configuration (Optional)

Add a `config.bifrost` to your repository root for enhanced functionality:

```json
{
  "name": "My Stack",
  "description": "A custom template for X platform",
  "platform": "remix",
  "github": "owner/repo",
  "tags": ["react", "typescript", "tailwind"],
  "postInstall": ["setup", "db:generate"],
  "plugins": ["owner/plugin1", "owner/plugin2"]
}
```
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Installing A Plugin**

Once your project has completed its installation process, you may now cd into the newly created directory and run

```bash
bunx bifrost-plugin
```

Entering interactive mode it will then obtain the list of available plugins to choose from the bifrost-plugin repo (owner `8an3`) from the file labeled `registry.bifrost`

or you may use the supplied method 

```bash
bunx bifrost-plugin otp-auth-plugin
```

Which will immediatly start the installation process, after scanning your projects config.bifrost to see if the platforms match for compatibility to ensure you are installing the correct plugin.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Creating your own plugin**

Plugins are to be made with their own repo so as it can host all the required files for the plugin. 
The repo is required to include a json config file labeled `plugin.bifrost` and a folder labeled `files` where it will host all the required files.
When installing a plugin it will prompt the user to either confirm the default supplied file location or the use can also edit the location to suite their use cases needs.

### plugin.bifrost

```json
{
  "name": "otp-auth-plugin",
  "description": "A custom one time password auth plugin for the remix platform",
  "platform": "remix",
  "github": "8an3/otp-auth-plugin",
  "tags": ["remix-run", "auth", "one-time-password"],
  "libraries": ["remix-auth-totp","remix-auth","@catalystsoftware/icons","@prisma/client","resend"],
  "files": [
        {
        "name": "email.tsx",
        "location": "app/components/catalyst-ui/utils/email.tsx"
        },
        {
        "name": "client-auth.tsx",
        "location": "app/components/catalyst-ui/utils/client-auth.tsx"
        },
        {
        "name": "auth-session.ts",
        "location": "app/components/catalyst-ui/utils/auth-session.ts"
        },
        {
        "name": "prisma.ts",
        "location": "app/components/catalyst-ui/utils/prisma.ts"
        },
        {
        "name": "login.tsx",
        "location": "app/routes/auth/login.tsx"
        },
        {
        "name": "lougout.tsx",
        "location": "app/routes/auth/lougout.tsx"
        },
        {
        "name": "signup.tsx",
        "location": "app/routes/auth/signup.tsx"
        },
        {
        "name": "magic-link.tsx",
        "location": "app/routes/auth/magic-link.tsx"
        },
        {
        "name": "verify.tsx",
        "location": "app/routes/auth/verify.tsx"
        },
    ],
    "configs":[
        {
            "targetFile": "prisma/schema.prisma",
            "configSource": "prisma-schema.txt",
            "insertType": "append" // or "replace", "merge"?
        }
    ]
}
```

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **Searching for / Posting Templates and Plugins**


Shortly a site will be available for use where you can search for templates and plugins.

Feature two tabs, both tabs will host a filtering section located to the left of the pages content and a search bar located at the top of each tabs section. Allowing you to filter by platform, tags, etc meanwhile the search bar will allow you to search for individual templates or plugins for you to use.

### Templates

Each template result will display:
- name
- description
- platform
- command line to install the template
- tags
- any plugins that are to be included with the templates installation 

### Plugins

Each plugin result will display
- name
- description
- platform
- command line to install the plugin
- tags
- required libraries
- required files

### Submitting

Whether its a template or plugin, you will have the ability to submit your own to be included with its respective registry, this step is not required or needed but will help in its overall discoverability.
All you have to do in order to submit is supply your templates or plugins config file once you start the submission process. The pages nav bar will host a `submit` button in order to start the process.

Upon submission the website will automatically update the relevant registry file and push the update to github to ensure the process is automated.
