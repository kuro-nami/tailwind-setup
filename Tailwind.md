## How to setup Tailwind CSS (Make sure you have downloaded latest version of node.js: https://nodejs.org/en)

Step 1: Create folder with name "src" and add index.html and script.js and input.css files to it.
(Make sure PostCSS Language Support Extension and Tailwind CSS Intellisense Extension are enabled, if they are not downloaded, download them.)

Step 2: Open Terminal (Ctrl+`) and paste the following command and press enter (you will have to wait a few seconds for it to install packages):

```
npm install -D tailwindcss
```

Step 3: Now paste this line and press enter in the terminal:

```
npx tailwindcss init
```

Step 2: Go in tailwind.config.js file change the content: [ ] line to include this:

```
content: ["./src/**/*.{html,js}"],
```

Step 3: Go to input.css and paste this. If it shows error, make sure PostCSS Language Support Extension is enabled:

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Step 4: Paste the following command into terminal and press Enter:

```
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

Step 5: Paste this in head of index.html:

```
<link href="/dist/output.css" rel="stylesheet">
```

Step 6: Now paste this in package.json file:

```
  "scripts": {
    "run": "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch"
  },
```

Step 7: Now you can start using Tailwind CSS.

### Warning: Make sure that you do not make any changes to the .json files and dont change their location aswell as tailwind.config.js file's location or your tailwind might stop working.
