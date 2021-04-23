# JavaScript -Set up

* Download Node.js
![](https://i.imgur.com/4a5mfoK.png)

* VS Code Extension (擴充)

    * [Chinese (Traditional) Language Pack](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-zh-hant)
    * [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)
    * [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
    * [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
    * [Babel JavaScript](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel)
    * [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)

* Update VS Code Settings

`Manage -> Settings -> Open Settings (JSON) -> add the following code`


```json=
{  
    "previewServer.port": 8081,
    "editor.fontSize": 18,
    "window.zoomLevel": 1,
    "git.ignoreWindowsGit27Warning": true,
    "workbench.iconTheme": "vscode-icons",
    "editor.formatOnSave": true,
    "[javascript]": {
      "editor.formatOnSave": false
    },
    "prettier.disableLanguages": ["js"],
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    },
    "eslint.alwaysShowStatus": true,
    "files.autoSave": "afterDelay"
  }
```




* Create a new project
![](https://i.imgur.com/kdHEZOJ.png)

`* npm init -y`
`* npm i -D eslint eslint-config-prettier eslint-plugin-prettier prettier`

* add settings file - `.eslintrc`  & `.prettierrc` and add the following codes

```json=
{
  "env": {
    "browser": true,
    "es6": true,
    "node": true
  },
  "extends": ["prettier", "eslint:recommended"],
  "plugins": ["prettier"],
  "parserOptions": {
    "ecmaVersion": 2020
  },
  "rules": {
    "prettier/prettier": "error"
  }
}
```
```json=
{
  "singleQuote": true,
  "trailingComma": "es5",
  "semi": false,
  "endOfLine": "auto"
}
```
add `index.html` & `index.js`

> makes sure to allow ESLint & Prettier
> ![](https://i.imgur.com/dK5gB5T.png)
