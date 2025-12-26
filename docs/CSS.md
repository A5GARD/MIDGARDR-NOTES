# CSS++

> [!WARNING] Currently in testing
> Despite currently still in the testing phase, you are more than welcome to try it out.
> Initial and secondary tests were successful in remix-run and react-router platforms
> As this isn't platform dependant, any platform you currently use tailwind in should be able to use this without issue

>I don't know why I did this, I was just installing tailwind v4 and was having a small issue and asked myself, "I wonder if I could make this...". Then my dumb ass did, and here we are. Since I went through the trouble of making this, took it a couple steps further making it a virtually 0 config setup in order to run. Only thing needed is to have a css file with, "@css++;" at the top of the file and import it into the app in whatever fashion your app calls for, along with one post css requirement that I could not get rid of.

## Features

✨ **JIT Compilation** - Only generates CSS for classes you actually use  
🎨 **Arbitrary Values** - Use any value with bracket notation: `w-[123px]`, `bg-[#ff0000]`, `text-[hsl(120_100%_50%)]`, `border-[rgb(0_0_255)]`  
⚡ **Lightning Fast** - Compiles in milliseconds  
👀 **Auto Watch Mode** - Automatically watches files in development  
🎯 **Config-Based** - Customize everything via `css.config.js`  **Not required**
🔥 **Zero Dependencies** - Minimal footprint  

## Installation

```bash
npm install @catalystsoftware/css-plus-plus --save-dev
pnpm install @catalystsoftware/css-plus-plus --save-dev
```

### app/styles/styles.css
```text
@css++;
```

#### postcss.config.js 

The one and only config I couldn't get rid of, since its due to a postcss requirement

```javascript
export default {
  plugins: {
    '@catalystsoftware/css-plus-plus/postcss': {},
  },
};

```

>Initial testing successful, did not have autoprefixer, postcss, or anything else style related installed. Just the single line css file and postcss-config.js with the above export, and ran perfectly. Will be conducting more thorough testing shortly.

### styles.css
To apply your own theme:
```css
@css++;

@layer css++ {
  :root {
    --background: #020817;
    --background-secondary: #111827;
    --foreground: #e2e8f0;
    --card: #020817;
    --card-foreground: #e2e8f0;
    --popover: #020817;
    --popover-foreground: #e2e8f0;
    --primary: #3b82f6;
    --primary-foreground: #111827;
    --secondary: #1e293b;
    --secondary-foreground: #e2e8f0;
    --muted: #1e293b;
    --muted-foreground: #94a3b8;
    --accent: #1e293b;
    --accent-foreground: #e2e8f0;
    --destructive: #7f1d1d;
    --destructive-foreground: #e2e8f0;
    --border: #1e293b;
    --input: #1e293b;
    --ring: #2563eb;
    --chart-1: #3b82f6;
    --chart-2: #10b981;
    --chart-3: #f59e0b;
    --chart-4: #a855f7;
    --chart-5: #ec4899;
    --radius: 0.0rem;
    --sidebar: 221 39% 11%;
    --sidebar-foreground: 220 20% 95%;
    --sidebar-primary: 217 91% 60%;
    --sidebar-primary-foreground: 220 20% 98%;
    --sidebar-accent: 220 30% 20%;
    --sidebar-accent-foreground: 220 20% 95%;
    --sidebar-border: 220 20% 25%;
    --sidebar-ring: 217 91% 60%;
    --special: 227 21% 8%;
    --special-muted-background: 240 10% 4%;
    --special-border: 240 4% 16%;
    --special-foreground: 240 5% 84%;
    --special-muted-foreground: 240 4% 46%;
  }

  .dark {
    /* Optional: Dark mode overrides */
    --background: #0a0a0a;
    --foreground: #ededed;
  }
}

/* User's custom styles below */
.my-custom-class {
  background: var(--primary);
  color: var(--foreground);
}
```

### Config Paths ( Not required )
- css.config.js
- css.config.mjs
- css.config.cjs
- csspp.config.js
- csspp.config.mjs
- csspp.config.cjs

# Quick Start - < 60 Seconds

## For Remix Projects

```bash
# 1. Import CSS (app/root.tsx)
import styles from "~/styles/generated.css?url";

export const links = () => [
  { rel: "stylesheet", href: styles },
];

# 2. Done! Run dev server
npm run dev
```

**That's it!** CSS++ automatically:
- ✅ Creates `dist/generated.css`
- ✅ Watches for changes
- ✅ Hot-reloads instantly

---

## For Next.js Projects

```bash
# 1. Import in layout (app/layout.tsx)
import './styles/generated.css';

# 2. Done! Run dev server
npm run dev
```

---

## For Vite Projects

```bash
# 1. Import in main (src/main.js)
import './generated.css';

# 2. Done!
npm run dev
```

---

## For Any Project (Manual)

```bash
# 1. Add script (package.json)
{
  "scripts": {
    "dev": "css++ & your-dev-command"
  }
}

# 2. Create config (css.config.js) - OPTIONAL!
export default {
  content: ["./src/**/*.{js,jsx,ts,tsx}"],
  output: "./dist/output.css",
};

# 3. Import CSS in HTML
<link rel="stylesheet" href="/dist/output.css">

# 4. Done!
npm run dev
```

---

## Zero Config Mode

**No config file needed!** CSS++ uses smart defaults:

```javascript
// Automatic defaults
const defaultConfig = {
    darkMode: ["class"],
    content: [
        "./app/**/{**,.client,.server}/**/*.{js,jsx,ts,tsx}", // Remix
        "./src/**/*.{html,js,jsx,ts,tsx}", // Vite/CRA
        "./components/**/*.{js,jsx,ts,tsx}",
        "./pages/**/*.{js,jsx,ts,tsx}", // Next.js
    ],
    output: "./dist/generated.css",
    theme: {
        extend: {
            fontFamily: {
                sans: [
                    'Inter',
                    'ui-sans-serif',
                    'system-ui',
                    'sans-serif',
                    'Apple Color Emoji',
                    'Segoe UI Emoji',
                    'Segoe UI Symbol',
                    'Noto Color Emoji'
                ]
            },
            borderRadius: {
                lg: 'var(--radius)',
                md: 'calc(var(--radius) - 2px)',
                sm: 'calc(var(--radius) - 4px)'
            },
            colors: {
                border: "var(--border)",
                input: "var(--input)",
                ring: "var(--ring)",
                background: "var(--background)",
                foreground: "var(--foreground)",
                primary: {
                    DEFAULT: "var(--primary)",
                    foreground: "var(--primary-foreground)",
                },
                secondary: {
                    DEFAULT: "var(--secondary)",
                    foreground: "var(--secondary-foreground)",
                },
                destructive: {
                    DEFAULT: "var(--destructive)",
                    foreground: "var(--destructive-foreground)",
                },
                muted: {
                    DEFAULT: "var(--muted)",
                    foreground: "var(--muted-foreground)",
                },
                accent: {
                    DEFAULT: "var(--accent)",
                    foreground: "var(--accent-foreground)",
                },
                popover: {
                    DEFAULT: "var(--popover)",
                    foreground: "var(--popover-foreground)",
                },
                card: {
                    DEFAULT: "var(--card)",
                    foreground: "var(--card-foreground)",
                },
                sidebar: {
                    DEFAULT: "var(--sidebar)",
                    foreground: "var(--sidebar-foreground)",
                    primary: "var(--sidebar-primary)",
                    "primary-foreground": "var(--sidebar-primary-foreground)",
                    accent: "var(--sidebar-accent)",
                    "accent-foreground": "var(--sidebar-accent-foreground)",
                    border: "var(--sidebar-border)",
                    ring: "var(--sidebar-ring)",
                },
                chart: {
                    "1": "var(--chart-1)",
                    "2": "var(--chart-2)",
                    "3": "var(--chart-3)",
                    "4": "var(--chart-4)",
                    "5": "var(--chart-5)",
                },
                special: {
                    DEFAULT: "var(--special)",
                    "muted-background": "var(--special-muted-background)",
                    border: "var(--special-border)",
                    foreground: "var(--special-foreground)",
                    "muted-foreground": "var(--special-muted-foreground)",
                },
            },
            backgroundColor: {
                background: "var(--background)",
            },
            keyframes: {
                "accordion-down": {
                    from: { height: "0" },
                    to: { height: "var(--radix-accordion-content-height)" },
                },
                "accordion-up": {
                    from: { height: "var(--radix-accordion-content-height)" },
                    to: { height: "0" },
                },
                "caret-blink": {
                    "0%,70%,100%": { opacity: "1" },
                    "20%,50%": { opacity: "0" },
                },
                float: {
                    '0%, 100%': { transform: 'translateY(0px) scale(1)' },
                    '50%': { transform: 'translateY(-20px) scale(1.05)' },
                },
                "pulse-glow": {
                    '0%, 100%': { opacity: "0.3", transform: 'scale(1)' },
                    '50%': { opacity: "0.6", transform: 'scale(1.1)' },
                },
                shimmer: {
                    '0%': { backgroundPosition: '-200% 0' },
                    '100%': { backgroundPosition: '200% 0' },
                },
                "spin-slow": {
                    "0%": { transform: "rotate(0deg)" },
                    "100%": { transform: "rotate(360deg)" },
                },
                "spin-slower": {
                    "0%": { transform: "rotate(0deg)" },
                    "100%": { transform: "rotate(-360deg)" },
                },
                "matrix-fade": {
                    "0%, 100%": { opacity: "0" },
                    "50%": { opacity: "1" },
                },
                click: {
                    "0%, 100%": { transform: "scale(1)" },
                    "50%": { transform: "scale(0.95)" },
                },
            },
            animation: {
                "accordion-down": "accordion-down 0.2s ease-out",
                "accordion-up": "accordion-up 0.2s ease-out",
                "caret-blink": "caret-blink 1.25s ease-out infinite",
                "float": "float 6s ease-in-out infinite",
                "pulse-glow": "pulse-glow 4s ease-in-out infinite",
                "shimmer": "shimmer 2s infinite",
                "spin-slow": "spin-slow 3s linear infinite",
                "spin-slower": "spin-slower 6s linear infinite",
                matrix: "matrix-fade 0.5s ease-in-out infinite",
                click: "click 0.3s ease-in-out",
            },
            typography: {
                DEFAULT: {
                    css: {
                        h1: {
                            fontSize: "1.875rem",
                            fontWeight: "700",
                            lineHeight: "1.25",
                            letterSpacing: "-0.025em",
                            textAlign: "center",
                            "@media (min-width: 1024px)": { lineHeight: "1.1" },
                        },
                        h2: {
                            marginTop: "0.75rem",
                            color: "var(--muted-foreground)",
                            fontWeight: "300",
                            textAlign: "center",
                        },
                        h3: {
                            fontWeight: "600",
                            marginBottom: "1rem",
                            marginTop: "1rem",
                        },
                        h4: {
                            fontSize: "1.25rem",
                            fontWeight: "600",
                            marginBottom: "0.75rem",
                            marginTop: "0.75rem",
                        },
                        h5: {
                            fontSize: "1.125rem",
                            fontWeight: "500",
                            marginBottom: "0.5rem",
                            marginTop: "0.5rem",
                        },
                        p: {
                            textWrap: "balance",
                            fontWeight: "300",
                            color: "var(--foreground)",
                            fontSize: "0.875rem",
                        },
                    },
                },
            }
        },
    },
};
```

---

## Usage Examples

```jsx
// Sizes
<div className="w-[300px] h-[200px]" />

// Colors
<div className="bg-[#ff0000] text-[rgb(255,255,255)] border-[hsl(120_100%_50%)]" />

// Spacing
<div className="p-[2rem] m-[10px] gap-[1.5rem]" />

// Borders
<div className="rounded-[16px] border-[2px]" />

// Everything!
<div className="
  w-[350px] 
  h-[75vh] 
  bg-[linear-gradient(to_right,#ff0000,#00ff00)]
  shadow-[0_4px_20px_rgba(0,0,0,0.1)]
  rotate-[45deg]
" />
```

---

## With CSS Variables

```css
/* global.css */
:root {
  --primary: #3b82f6;
  --radius: 0.5rem;
}
```

```jsx
<div className="bg-[var(--primary)] rounded-[var(--radius)]" />
```

---

## Custom Animations

**css.config.js**:
```javascript
export default {
  theme: {
    extend: {
      keyframes: {
        fadeIn: {
          "0%": { opacity: "0" },
          "100%": { opacity: "1" },
        },
      },
      animation: {
        "fade-in": "fadeIn 0.3s ease-in",
      },
    },
  },
};
```

**Usage**:
```jsx
<div className="animate-fade-in" />
```

---

## FAQ

**Q: Do I need a config file?**  
A: No! Works out of the box.

**Q: Does it auto-watch?**  
A: Yes! In development mode.

**Q: Works with TypeScript?**  
A: Yes! Scans `.ts` and `.tsx` files.

**Q: Works with CSS-in-JS?**  
A: Yes! Detects classes in `className={}`.

**Q: Production builds?**  
A: Set `NODE_ENV=production` for minified output.

**Q: File size?**  
A: Only generates CSS you use (~5KB typical).

---


