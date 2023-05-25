# VSCode-C-Configs

My personal VSCode **C language** configurations to make debuging and launching **C projects** easier with  **VSCode**


# Supported OS

My configurations supports the 3 main systems: (Windows, GNU/Linux, MacOS X)
| OS |Features  |
|--|--|
|Windows  | Support compiling, debuging and external window launching |
|MacOS|Support compiling, debuging but unable to support automatic external window opening due to a limitation of the version of `lldb`|
|GNU/Linux| Support compiling, debuging and external window launching |

# Usage
copy the two files (tasks.json and launch.json) from the your specific OS folder ("/Windows", "/MacOS" or "/Linux") to your ".vscode" folder


## Customizing compiler configs

Feel free to custom your compiler configuration by passing arguments to your linker as you want:
**Default value:**
from tasks.json:
```json
   "args":  [

"-fdiagnostics-color=always",

"-g",

"${file}",

"-o",

"${fileDirname}\\${fileBasenameNoExtension}.exe"

],
```
**Custom value:** example: Let's add an option to compile a project with ncurses TUI
from tasks.json:
```json
   "args":  [

"-fdiagnostics-color=always",

"-g",

"${file}",

"-o",

"${fileDirname}\\${fileBasenameNoExtension}.exe",
"-lncurses"

],
```
