## EasyEdit

Required build dependacies

- - npm
- - vite
- - file-saver
- - html2canvas
- - jspdf
- - mermaid
- - react
- - react-dom
- - react-markdown
- - remark-gfm
- - electron

<img src="./screenshots/sample001.png" alt="Example" width="500" height="300">

## Run the project

```
$ npm start
```

## Important package.json

```
{
  "name": "easyedit",
  "private": true,
  "version": "1.0.0",
  "type": "module",
  "scripts": {
    "start": "concurrently \"vite\" \"wait-on http://localhost:3000 && electron .\"",
    "build": "vite build",
    "electron:build": "electron-builder"
  },
  "main": "main.cjs",
  "build": {
    "appId": "easyedit.wagemaker.uk",
    "files": [
      "dist/**/*",
      "main.js",
      "preload.js"
    ],
    "directories": {
      "buildResources": "assets"
    }
  },
  "author": "Ricardo Wagemaker <wagemra@gmail.com>",
  "license": "MIT",
  "dependencies": {
    "file-saver": "^2.0.5",
    "html2canvas": "^1.4.1",
    "jspdf": "^2.5.2",
    "lodash.debounce": "^4.0.8",
    "mermaid": "^11.4.0",
    "react": "^18.3.1",
    "react-dom": "^18.3.1",
    "react-markdown": "^9.0.1",
    "rehype-raw": "^7.0.0",
    "remark-gfm": "^4.0.0"
  },
  "devDependencies": {
    "@eslint/js": "^9.13.0",
    "@types/file-saver": "^2.0.7",
    "@types/lodash.debounce": "^4.0.9",
    "@types/node": "^22.8.1",
    "@types/react": "^18.3.11",
    "@types/react-dom": "^18.3.1",
    "@vitejs/plugin-react-swc": "^3.5.0",
    "concurrently": "^9.1.0",
    "electron": "^33.2.0",
    "electron-builder": "^25.1.8",
    "eslint": "^9.13.0",
    "eslint-plugin-react-hooks": "^5.0.0",
    "eslint-plugin-react-refresh": "^0.4.13",
    "globals": "^15.11.0",
    "vite": "^5.4.9",
    "wait-on": "^8.0.1"
  }
}
```

## Mermeid example

```mermaid
flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
```