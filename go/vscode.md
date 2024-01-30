# Setting up Visual Studio Code for Go Code Formatting on Save

If you're struggling to configure Visual Studio Code (VSCode) to automatically format your Golang code on save, you're not alone. This guide aims to provide a reliable solution to ensure a seamless coding experience.

## Problem Overview

After exploring various solutions on [Stack Overflow](https://stackoverflow.com/questions/35571033/how-to-set-vscode-format-golang-code-on-save), none of them seem to work for me. My environment includes Go version 1.17.1, VSCode version 1.60.1, and I'm using Linux Pop!_os.

## Solution

Upon thorough research, I found the official documentation for Go support in VSCode, which provides a straightforward solution. Check it out [here](https://code.visualstudio.com/docs/languages/go#_formatting).

## Configuration

To implement this solution, update your `settings.json` file in VSCode with the following configurations:

```json
"[go]": {
    "editor.insertSpaces": true,
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "golang.go"
},
```

### Note:

Make sure you have the necessary Go extensions installed in VSCode. To check, open a `.go` file, and at the bottom left, you should see the Go version. If there's an exclamation icon, click on it and install the suggested extensions.

---

Feel free to adjust the wording or formatting to better fit your style and preferences.
