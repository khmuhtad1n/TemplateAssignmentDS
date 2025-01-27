# Modern Web Project Template

A streamlined template for web development with Tailwind CSS and webpack by KhMuhtadin.

## Features

- 🎨 **Tailwind CSS** - Utility-first CSS framework
- 📦 **Webpack** - JavaScript module bundler
- 🔄 **Hot Reload** - Live preview changes

## Getting Started

### Prerequisites

1. Install Node.js:
   - Download from [nodejs.org](https://nodejs.org)
   - Verify installation: `node --version`

### Step-by-Step Setup

1. **Create Project Directory**

```bash
mkdir my-project
cd my-project
```

2. **Initialize Project**

```bash
git clone [repository-url] .
# or download and extract the template to your folder
```

3. **Install Dependencies**

```bash
npm install
```

4. **Create Required Files**

Create these files in your project:

`src/input.css`:

```css
@import "tailwindcss";
```

`src/main.js`:

```javascript
// Your JavaScript code here
console.log("Hello World!");
```

`dist/index.html`:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Project</title>
    <link href="./dist/output.css" rel="stylesheet" />
  </head>
  <body>
    <h1 class="text-3xl font-bold">Hello world!</h1>
    <script src="main.js"></script>
  </body>
</html>
```

5. **Start Development**

```bash
npm run dev
```

6. **Open Your Project**

- Open `dist/index.html` in your browser
- Edit `src/main.js` for JavaScript
- Changes will reload automatically

## Project Structure

```
project-root/
├── dist/           # Production files
│   ├── index.html  # Your HTML file
│   └── output.css  # Generated CSS
├── src/            # Source files
│   ├── input.css   # Tailwind directives
│   └── main.js     # JavaScript code
└── package.json    # Project config
```

## Package.json

```json
{
  "name": "web template by khmuhtadin",
  "version": "1.0.0",
  "type": "module",
  "description": "",
  "main": "index.html",
  "scripts": {
    "tw:run": "npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css --watch",
    "bundle:dev": "npx webpack ./src/main.js --watch",
    "dev": "concurrently \"npm run tw:run\" \"npm run bundle:dev\""
  },
  "keywords": [],
  "author": "",
  "devDependencies": {
    "@tailwindcss/cli": "^4.0.0",
    "buffer": "^6.0.3",
    "concurrently": "^9.1.2",
    "prettier": "^3.4.2",
    "prettier-plugin-tailwindcss": "^0.6.11",
    "tailwindcss": "^4.0.0",
    "webpack": "^5.97.1",
    "webpack-cli": "^6.0.1"
  }
}
```

## Troubleshooting

Common issues and solutions:

1. **npm install fails**

   - Check your Node.js version
   - Clear npm cache: `npm cache clean --force`
   - Delete node_modules and try again

2. **Tailwind not working**

   - Verify `input.css` has the correct directives
   - Check if `output.css` is being generated
   - Ensure your HTML links to the correct CSS file
   - By default, Tailwind intellisense didnt give any suggestion. add this to setting.json to make it run

   ```json
   {
     "tailwindCSS.includeLanguages": {
       "html": "html",
       "javascript": "javascript",
       "css": "css"
     },
     "editor.quickSuggestions": {
       "strings": true
     },
     "files.associations": {
       "*.css": "tailwindcss"
     }
   }
   ```

3. **Webpack errors**
   - Check if `main.js` exists in the correct location
   - Verify webpack is installed correctly
   - Check console for specific error messages

---

Made when i cant sleep by KhMuhtadin

```

```
