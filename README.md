# Setup

- `npm init`
- `git init`
- `npm i -D typescript parcel prettier @types/react @types/react-dom`
- `npm i react react dom`
- `touch .gitignore`

```
dist
.parcel-cache
node_modules
```

- `touch ./src/index.html`

```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
  </head>
  <body>
    <div id="app"></div>
    <script type="module" src="index.tsx"></script>
  </body>
</html>

```

- `touch ./src/index.tsx`

```
import { createRoot } from "react-dom/client";
import { App } from "./App";
import React from "react";

const container = document.getElementById("app");
if (!container) throw new Error("No container");
const root = createRoot(container);
root.render(<App />);
```

- `touch ./src/App.tsx`

```
import React from "react";

export const App = () => {
  return (
    <div>
      <h1>Hello World</h1>
    </div>
  );
};
```

- add `"start": "parcel ./src/index.html"` to package.json
- add `"format": "prettier --write ."` to package.json
- `touch ./vscode/settings.json`

```
{
  "editor.tabSize": 2,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnPaste": true,
  "editor.formatOnSave": true
}
```
