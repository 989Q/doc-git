## Installation Guide: Go for macOS

### Installation

To install the project, follow these steps:

1. Ensure you have Go installed on your machine. If not, you can download and install it from https://go.dev/dl/.

### Command not found: go on Mac after installing Go

[Command not found go — on Mac after installing Go](https://stackoverflow.com/questions/34708207/command-not-found-go-on-mac-after-installing-go)

If you encounter the error zsh: command not found: go after installing Go, follow these steps to resolve it:

### Solution

To resolve the "command not found: go" issue, you need to add the Go binary path to your shell profile configuration. Follow these steps:

1. Open your ~/.zshrc file using a text editor.

2. Add the following lines at the end of the file:
```
export PATH=$PATH:/usr/local/go/bin
export PATH=$PATH:$GOPATH/bin
```

3. Source your ~/.zshrc file to apply the changes:
```bash
. ~/.zshrc
```

Now, when you run the `go version` command, it should work without any issues.
