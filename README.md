Step 1: Set Up a Golang Project

mkdir my_golang_project
cd my_golang_project
go mod init example.com/my_golang_project

Step 2: Configure the Debug Environment

1. In the the Run view, click "create a launch.json file"
2. Choose Go: Launch Package from the debug configuration drop-down menu. VS Code will create a launch.json file in a .vscode folder in your workspace (project root folder) or in your user settings or workspace settings.

Step 3: Set a Breakpoint and Start Debugging

1. Choose your file
2. You can set a breakpoint by clicking in the gutter to the left of the line number.

Step 4: Start Debugging

1. Click on the "Run and Debug"
2. Select "Go: Launch"
   ❗❗ When you start debugging for the first time or if the dlv executable on your system is too old to support DAP, the Go extension may ask to install or update Delve. Follow the instructions to install it, and then start the debugging session again.
install pkg: go install github.com/go-delve/delve/cmd/dlv@latest
update pkg dlv:
 - Buka Command Palette (Ctrl+Shift+P atau Cmd+Shift+P).
 - Ketik dan pilih perintah: Go: Install/Update Tools.
 - Cari dan pilih dlv (Delve).
 - Klik OK untuk menginstalnya. VS Code akan mencoba menginstal atau memperbarui Delve menggunakan versi Go yang Anda miliki saat ini.

Step 5: Debugging in Action

❗❗You can now examine variable values, step through the code, and understand the program's flow during runtime.

The available commands are:
Continue / Pause F5
Step Over (aka next in Delve) F10
Step Into (aka step in Delve) F11
Step Out (aka stepout in Delve) Shift+F11 or ⇧F11
Restart (currently this is "Stop + Start") Ctrl+Shift+F5 or ⇧⌘F5
Stop (terminate the debugee. Available in Launch request) Shift+F5 or ⇧F5
