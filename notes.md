# Visual Studio Code Efficiency Guide for Python/ML Developers

## Basics: Opening, Saving, and Navigation

### Opening Files and Folders
- **Open File**: Press **Ctrl+O** to open a file chooser and select a file to edit. *Example:* Hit **Ctrl+O**, type or pick `data_preprocess.py`, then **Enter** to open it.  
- **Open Folder**: Press **Ctrl+K** then **Ctrl+O** (sequentially) to open a project folder in VS Code. *Example:* Use this to open your ML project directory via keyboard without using the mouse.  
- **Quick Open**: Press **Ctrl+P** to quickly open any file by name (fuzzy search). *Example:* **Ctrl+P**, type “`train`” to find `train_model.py`, then **Enter** to open it instantly.

### Saving Work
- **Save File**: Press **Ctrl+S** to save the current file. *Example:* After writing code, hit **Ctrl+S** to persist changes to disk.  
- **Save All**: Press **Ctrl+K S** (hold **Ctrl**, press **K**, then **S**) to save all open files. Useful when working on multiple notebooks or scripts.  
- **Auto-Save**: VS Code can auto-save files on edit. Toggle it via **File > Auto Save** or by setting `"files.autoSave": "afterDelay"` in your settings (no direct default shortcut). *Example:* Enable Auto Save to avoid needing manual saves during experimentation.

### Command Palette Mastery
- **Command Palette**: Press **Ctrl+Shift+P** (or **F1**) to open the Command Palette, where you can run any VS Code command by name. *Example:* **Ctrl+Shift+P**, type “`Python: Select Interpreter`” to quickly switch Python versions.  
- The Command Palette is your keyboard control center – from installing extensions to running tasks, just press **Ctrl+Shift+P**, start typing a command, and hit **Enter** to execute.

### Basic Navigation and Tabs
- **Switch Tabs**: Use **Ctrl+PageUp/PageDown** to cycle through open editor tabs. *Example:* Quickly switch between `model.py` and `utils.py` with **Ctrl+PageDown**.  
- **Close Tab**: Press **Ctrl+W** to close the current file tab ([Helpful shortcuts for VSCode · GitHub](https://gist.github.com/d168e301429c0305c49d97907796c72d#:~:text=Close%20File)). Use **Ctrl+K W** to close **all** tabs. *Example:* Close a finished notebook with **Ctrl+W** without touching the mouse.  
- **Go to Line**: Press **Ctrl+G** and enter a line number to jump to that line in the editor. *Example:* **Ctrl+G**, then “`42`” jumps to line 42, useful when an error message points to a specific line.

### Searching Text 
- **Find in File**: Press **Ctrl+F** and type a query to search within the current file. VS Code highlights matches as you type. Press **Enter** to jump to the next match, **Shift+Enter** for previous. *Example:* **Ctrl+F**, search “`def train`” to locate the function definition in your script.  
- **Find and Replace**: Press **Ctrl+H** to find text and replace it (use with caution). Toggle replace mode in the find widget to substitute text, e.g., replace all occurrences of a variable name.  
- **Find in Project**: Press **Ctrl+Shift+F** to search across all files in your folder/workspace ([Basic editing](https://code.visualstudio.com/docs/editor/codebasics#:~:text=match%20at%20L576%20VS%20Code,a%20file%20to%20see%20a)). Results show in a panel grouped by file. *Example:* **Ctrl+Shift+F**, search “`plt.plot(`” to find where Matplotlib plotting is done across your codebase.

## Editing Essentials

### Writing and Editing Code
- **Undo/Redo**: Press **Ctrl+Z** to undo the last edit, and **Ctrl+Y** (or **Ctrl+Shift+Z**) to redo an undone change. *Example:* Undo a mistaken code deletion with **Ctrl+Z**.  
- **Cut/Copy Line**: Without selecting any text, **Ctrl+X** cuts the entire current line, and **Ctrl+C** copies the line. *Example:* Press **Ctrl+C** on a line to duplicate it, then **Ctrl+V** to paste a second copy.  
- **Delete Line**: Press **Ctrl+Shift+K** to delete the current line entirely. *Example:* Quickly remove a debug `print` by placing the cursor on that line and hitting **Ctrl+Shift+K**.  
- **Move Lines**: Use **Alt+↑/↓** to move the current line or selection up or down. *Example:* Reorder two lines of code by pressing **Alt+↑** to swap the line upward.  
- **Duplicate Lines**: Press **Shift+Alt+↓** (or ↑) to copy the current line downward or upward. *Example:* Quickly copy a list item or code block by pressing **Shift+Alt+↓** to avoid copy-paste.  
- **Indent/Outdent**: Press **Tab** to indent (increase indent) and **Shift+Tab** to outdent (decrease indent) the current line or selection. *Example:* In a Python function, select multiple lines and press **Tab** to indent them under an `if` block.

### Commenting Code
- **Toggle Line Comment**: Press **Ctrl+/** to comment or uncomment the current line. This adds `#` in Python. *Example:* Disable a line of code (e.g., a print statement) by toggling **Ctrl+/** on that line.  
- **Toggle Block Comment**: Press **Shift+Alt+A** to comment/uncomment a block of code (for languages with block comments). *Example:* Use **Shift+Alt+A** in a JSON or C file to wrap selected lines in a block comment. (In Python, this inserts triple quotes for docstring-style commenting.)

### Sidebar and Panels (Keyboard-Only)
- **Toggle Explorer**: Press **Ctrl+B** to show or hide the sidebar (Explorer view). *Example:* **Ctrl+B** to hide the file tree and gain more coding space, **Ctrl+B** again to bring it back.  
- **Focus Explorer**: Press **Ctrl+Shift+E** to focus the File Explorer pane. Then use arrow keys to navigate files, **Enter** to open the selected file. *Example:* Quickly switch files by **Ctrl+Shift+E**, arrow to the file, **Enter**.  
- **Toggle Terminal Panel**: Press **Ctrl+`** (backtick) to open or hide the integrated Terminal *Example:* Pop open a terminal with **Ctrl+`**, run `pytest`, then **Ctrl+`** to hide it and return to coding.  
- **Toggle Bottom Panel**: Press **Ctrl+J** to show/hide the bottom panel (which holds Terminal, Problems, etc.). *Example:* **Ctrl+J** to hide the panel after checking error messages, for a cleaner view.  
- **Cycle Editor/Panel Focus**: Use **F6** to cycle focus between editor, side bar, bottom panel, etc. *Example:* After opening the terminal, press **F6** to jump back to the editor without the mouse.

## Code Intelligence and Refactoring

### IntelliSense and Auto-Completion
- **Trigger Suggestions**: Press **Ctrl+Space** to manually trigger IntelliSense suggestions at the cursor. VS Code (with Python extension) shows code completions, method signatures, etc. *Example:* In a blank line, type `np.` and press **Ctrl+Space** to see NumPy attributes and methods.  
- **Parameter Hints**: Press **Ctrl+Shift+Space** when inside function parentheses to show parameter info. *Example:* After typing `plt.imshow(`, hit **Ctrl+Shift+Space** to view the parameters for `imshow`.  
- *(IntelliSense is usually automatic as you type; these shortcuts ensure you don’t need the mouse to get code help.)*

### Go to Definition and References
- **Go to Definition**: With the cursor on a function or class, press **F12** to jump to its definition. *Example:* On a call to `train_model()`, press **F12** to open the file and line where `train_model` is defined.  
- **Peek Definition**: Press **Alt+F12** to view a definition in a small popup *without leaving your current file*. *Example:* Use **Alt+F12** on `np.argmax` to peek at its definition in-line, so you can read docs while staying in your code.  
- **Find References**: Press **Shift+F12** to find all usages of a symbol in your project. *Example:* Place cursor on a variable `learning_rate` and hit **Shift+F12** to list every location it’s used (great for understanding code impact).

### Refactoring and Quick Fixes
- **Rename Symbol**: Press **F2** to rename all instances of a symbol (variable, function, etc.) across your code. *Example:* Rename variable `x` to `features` by placing cursor on `x`, pressing **F2**, typing `features`, and **Enter** – all occurrences update at once.  
- **Quick Fix / Code Actions**: Press **Ctrl+.** (Ctrl+Period) when you see a lightbulb suggestion or error squiggle. This opens context actions like auto-importing a missing module or correcting code. *Example:* If you use an undeclared function, press **Ctrl+.** to get a suggestion to import it from the right library.
- **Format Document**: Press **Shift+Alt+F** to format the entire file according to code style (with a formatter like Black or autopep8). *Example:* Messy code? Hit **Shift+Alt+F** to auto-format your Python script into PEP8 style. (Ensure you have a Python formatter configured.)  
- **Organize Imports**: Some language servers allow organizing imports via **Shift+Alt+O** (or through a Quick Fix). *Example:* Remove unused imports and sort them by triggering **Ctrl+.** on an import statement and choosing “Organize Imports” (available when using the Python extension).

### Navigating Problems and Errors
- **View Problems**: Press **Ctrl+Shift+M** to open the Problems panel listing errors and warnings. *Example:* After running a linter, use **Ctrl+Shift+M** to see all issues at once.  
- **Next/Previous Error**: Press **F8** to jump to the next error or warning in your code, **Shift+F8** for the previous. *Example:* Iterate through Pylint errors one by one by hitting **F8** repeatedly – VS Code opens the file at each error line for you.

## Advanced Editing Techniques

*Using **multiple cursors** to edit code simultaneously. VS Code highlights each cursor and edits all positions at once. Here three cursors add a suffix to variable names in parallel.*

### Multi-Cursor Editing
- **Add Cursors (Line)**: Press **Ctrl+Alt+Down/Up** to add a new cursor below or above the current one. *Example:* Place additional cursors on successive lines (e.g., on lines 10–15) by hitting **Ctrl+Alt+Down** repeatedly, then type `# TODO:` to insert that comment on all those lines at once.  
- **Add Cursor (Next Match)**: Press **Ctrl+D** to select the next occurrence of the current word and add a cursor there. *Example:* With cursor on a variable `epoch`, press **Ctrl+D** repeatedly to multi-select the next instances of “epoch” and edit them together (great for quick renaming).  
- **Select All Occurrences**: Press **Ctrl+Shift+L** to select *all* occurrences of the current selection and add cursors to each. *Example:* Select the word `loss` and hit **Ctrl+Shift+L** to place cursors on every `loss` in the file, then type `val_loss` to change them all simultaneously.  
- **Column (Box) Selection**: Hold **Shift+Alt** and press arrow keys to create a rectangular selection. *Example:* Place cursor at the start of a column of text, then **Shift+Alt+Down** four times to select a vertical block — now you can edit or add to multiple lines in that column. (This is useful for editing tables or adding prefixes to multiple lines.)

### Snippets Usage
- **Insert Snippet**: Snippets are code templates for common patterns (loops, function definitions, etc.). They appear in IntelliSense suggestions and can be triggered by pressing **Tab** after typing a prefix. *Example:* In a Python file, type `for` and press **Tab** – this expands into a for-loop snippet like `for ${1:element} in ${2:iterable}:` with placeholders. Fill in the placeholders and press **Tab** to jump between them.  
- **Browse Snippets**: Open the Command Palette (**Ctrl+Shift+P**) and run **“Insert Snippet”** to see available snippets. *Example:* Choose a snippet for a Python class definition to scaffold a new class quickly.  
- **Custom Snippets**: You can create your own snippets via **File > Preferences > User Snippets** (opens a JSON for snippet definitions). Define a prefix and body for code you often write. *Example:* Create a `trainloop` snippet that inserts your usual training loop code with one short trigger.

### Emmet for Rapid Editing *(HTML/CSS only)* 
- *(If you work with HTML/CSS inside VS Code, Emmet abbreviations let you generate markup with shortcuts. For Python/ML code, Emmet isn’t applicable, so it’s omitted here.)*

## UI Layout and Focus

### Split Editors and Groups
- **Split Editor**: Press **Ctrl+\\** to split the current editor into two side-by-side views. *Example:* Open `model.py`, then press **Ctrl+\\** to create a new pane and use **Ctrl+P** to open `utils.py` in it, allowing you to see both files at once.  
- **Open to the Side**: From the Command Palette, run **“View: Split Editor Right”** (no default keybinding) to open the current file in a new vertical group. You can also use **Ctrl+K F12** when on a symbol to open its definition to the side.  
- **Switch Editor Group**: Press **Ctrl+1**, **Ctrl+2**, ... to focus the first, second, etc., editor group. *Example:* After splitting, press **Ctrl+1** to go to the left code pane, **Ctrl+2** for the right pane.  
- **Move File Between Groups**: Press **Ctrl+K** then **Ctrl+←/→** to move the current file to the left or right group. *Example:* If you opened something in the wrong pane, use this chord to move it without dragging.  
- **Even More Splits**: You can split multiple times (vertical and horizontal). For three or more editors, use **View > Editor Layout** commands (accessible via Command Palette) to arrange grid layouts. *Keep navigation efficient by memorizing group focus keys (Ctrl+#).*

### Zen Mode and Full Screen Focus
  *VS Code **Zen Mode**: no distractions – the code editor takes the full screen, hiding sidebars, panels, and status bars. Perfect for focusing on complex algorithms or debugging output.*

- **Toggle Zen Mode**: Press **Ctrl+K Z** to enter Zen Mode (distraction-free full screen). This hides all UI except the editor canvas. *Example:* When concentrating on writing a new training loop, use **Ctrl+K Z** to maximize focus; press **Esc** twice to exit Zen Mode and restore the interface.  
- **Toggle Full Screen**: Press **F11** for full screen (similar to Zen but keeps the top menu bar). *Example:* Presenting code or working on a small screen – **F11** gives you a bit more real estate.  
- **Zen Tips**: Even in Zen Mode, all your shortcuts still work. Use **Ctrl+Shift+P** to open files or **Ctrl+`** for the terminal without leaving the mode.

### Task Runner (Build/Run Tasks)
- **Run Task**: Press **Ctrl+Shift+B** to run the default build task (if configured). In Python/ML, you might configure a task to run tests or lint. *Example:* Set up a task for `pytest` and trigger it with **Ctrl+Shift+B** instead of typing the command each time.  
- **Configure Tasks**: Use Command Palette **“Tasks: Configure Task”** to create automated tasks (like training, data processing scripts, etc.) that you can run with a keystroke. This leverages `tasks.json` in the `.vscode` folder.  
- *(Tasks are an advanced feature to automate workflows. For quick one-off runs, the integrated terminal is usually sufficient.)*

## Running Code and Debugging

### Integrated Terminal Workflow
- **Open Integrated Terminal**: Press **Ctrl+`** to toggle the terminal panel within VS Code. *Example:* **Ctrl+`** opens a terminal at your project root; run `python train.py` to start training your model, then use **Ctrl+`** to hide the terminal and check your code while it runs.  
- **Create New Terminal**: Press **Ctrl+Shift+`** to open a new terminal instance (useful if you need a separate shell for, say, running `tensorboard` alongside training).  
- **Terminal Navigation**: Use **Ctrl+PageUp/PageDown** to switch between multiple terminal tabs (or the dropdown). All standard shell keyboard shortcuts work here, and you can split terminals with the split button or via **Ctrl+Shift+5** (default split command).  
- **Run Selection/Line**: In a Python file, select code and press **Shift+Enter** to run the selection in the Python Terminal or REPL (if using the Python extension’s interactive mode). *Example:* Highlight a loop and **Shift+Enter** to execute it on the fly in an interactive window, to quickly test a snippet.

### Setting Breakpoints
- **Toggle Breakpoint**: With the cursor on a line, press **F9** to set or remove a breakpoint. *Example:* On the line `model.fit(...)`, press **F9** to insert a breakpoint (a red dot) – the debugger will pause execution here. Press **F9** again on that line to remove the breakpoin.  
- You can manage breakpoints in the Breakpoints side panel (enable/disable them, etc.) entirely with keyboard: use **Ctrl+Shift+P** and “**View: Debug Panel**”, then navigate with Tab/arrow keys.

### Launching and Controlling the Debugger
- **Start Debugging**: Press **F5** to launch the debugger with the last used configuration. If no debugger config exists, VS Code will attempt to debug the active file (for Python, it will run it with the Python extension’s debug engine). *Example:* Open `train.py` and hit **F5** to start debugging it; if prompted, select “Python File” as the debug configuration.  
- **Run without Debugging**: Press **Ctrl+F5** to run the file normally (without breakpoints). *Example:* Useful when you want to quickly execute the script without pausing, but still within VS Code’s run console.  
- **Step Over (F10)**: When paused at a breakpoint, press **F10** to execute the current line and move to the next line, *without entering* any function calls on that line. *Example:* If the current line calls `load_data()`, **F10** will run it completely and stop on the next line in the current function.  
- **Step Into (F11)**: Press **F11** to dive into the function call on the current line. *Example:* On a line calling `train_epoch()`, **F11** will jump into the first line of `train_epoch` function so you can debug inside it.  
- **Step Out (Shift+F11)**: Press **Shift+F11** to leave the current function and return to the caller, finishing execution of the remaining lines in the function. *Example:* If you stepped into a deep function but now want to go back up, **Shift+F11** will run the rest of it and pause after the call.  
- **Continue (F5)**: Once paused, pressing **F5** again will resume the program until the next breakpoint (or program end).  
- **Debug Console**: While stopped at a breakpoint, press **Ctrl+Shift+Y** to focus the Debug Console (or click inside it) to evaluate expressions or print variable values. *Example:* At a breakpoint, type `model.weights` in the Debug Console and press Enter to inspect the weights.  
- **Stop Debugging**: Press **Shift+F5** to stop the debug session entirely. *Example:* If the program is stuck or you’re done debugging, **Shift+F5** ends it and resets the debugger.

### Watching Variables and Using the Debugger UI
- **View Variables/Call Stack**: While debugging, press **Ctrl+Shift+D** to ensure the Debug view is open (if not already). Use arrow keys to navigate the VARIABLES, WATCH, CALL STACK, and BREAKPOINTS sections. You can expand objects with arrow keys as well.  
- **Add to Watch**: Focus a variable in the VARIABLES section, then press **Enter** to add it to WATCH (or use **Alt+Click** via keyboard by focusing and pressing **Menu/Context** key to open context menu, then arrow to “Add to Watch”). *Example:* Add `loss` to watch to see how it changes each iteration.  
- **Repl (Debug Console)**: Use the Debug Console to run arbitrary Python while paused. It’s automatically focused on stop; if not, press **Ctrl+Shift+Y**. This is useful for inspecting `len(data)` or calling functions on the fly.

*(With these keyboard techniques, you can perform full debugging sessions—setting breakpoints, stepping through code, inspecting variables—without taking your hands off the keyboard.)*

## Essential Extensions for Python/Machine Learning

Leverage VS Code’s extension ecosystem to supercharge your Python, ML, and DL workflow. Install extensions via the **Extensions panel** (**Ctrl+Shift+X**) or the Command Palette (use “Extensions: Install” command). Here are must-haves:

### Python (Microsoft) & Pylance
- **Python**: Official extension providing rich Python support: linting, IntelliSense, debugging, code navigation, testing, Jupyter Notebook support, and more. It auto-installs Pylance for language intelligence. *Example:* With the Python extension, you get error highlighting and autocomplete in a PyTorch script, and you can run/debug with ease.  
- **Pylance**: Advanced language server for Python by Microsoft, offering fast, context-aware IntelliSense and type checking. *Features:* auto-import suggestions, type hints, code completion and refactoring tools. *Example:* As you type `np.array(`, Pylance shows parameter info and flags type mismatches, making coding faster and safer.

### Jupyter
- **Jupyter**: Provides full Jupyter Notebook integration in VS Code. Edit and run `.ipynb` notebooks or use **Jupyter: Create Interactive Window** to run cells in a Python script interactively. It supports Plotly, matplotlib inline plots, and more. *Example:* Open a Jupyter notebook within VS Code to tweak your pandas data analysis, run cells with **Ctrl+Enter**, and see outputs directly in the editor. No need to switch to a browser.  
- **Jupyter Notebook Renderers** (optional): Enhances Jupyter by rendering complex outputs (like Plotly, Bokeh, or TensorFlow plots) inside VS Code. *Example:* View interactive Vega charts or 3D plots within VS Code notebooks.

### GitLens (Git Supercharged)
- **GitLens**: Powerful Git extension that turbo-charges version control in VS Code. It annotates lines with blame info, lets you peek at history and diffs inline, and provides a rich repository sidebar. *Features:* line-by-line blame, commit searching, visual diff comparisons, and more. *Example:* See who last modified a function by simply placing the cursor on it (GitLens shows the commit and author in-line), or use the GitLens sidebar to review pull request changes without leaving VS Code. This is invaluable for collaboration on ML projects and tracking experiments.

### Live Share *(Collaboration)*
- **Visual Studio Live Share**: If you collaborate or pair-program, Live Share lets others join your VS Code session securely, with shared editing and debugging. *Example:* Pair-program a machine learning model tuning session with a colleague in real-time, both editing the same code and running cells, each using your own cursor.

### GitHub Copilot (AI Pair Programmer)
- **GitHub Copilot**: An AI code assistant that uses OpenAI Codex to suggest code completions and even entire functions. It learns from context and comments. *Example:* As you write a comment “# function to normalize data”, Copilot might suggest the implementation of the function automatically. It’s extremely useful for boilerplate code or exploring new APIs (note: Copilot is a paid service with a free trial).  
- *Alternative:* **Intellicode** (Microsoft) is a free AI-assisted extension that improves VS Code’s suggestions by ranking them based on usage patterns – useful if Copilot is not available.

### Testing and Linting Extensions
- **Python Test Explorer**: Adds a Testing panel to run unit tests or pytest tests with a GUI in VS Code. *Example:* Discover all your `pytest` tests and run them with a click or keyboard from the Test Explorer sidebar, viewing results immediately in the editor.  
- **ESLint/Pylint**: While the Python extension can integrate linters, you might install **Pylint** or **Flake8** extensions to get real-time lint feedback. *Example:* See code issues (unused imports, undefined variables) highlighted as you type, which helps maintain code quality in ML projects.

### Docstring and Code Quality
- **autoDocstring** (Python Docstring Generator): Automatically generates documentation comments for your functions/classes in the format of your choice (Google, NumPy, etc.) *Example:* Place your cursor inside a function and invoke **Ctrl+Shift+P**, “**Generate Docstring**” – autoDocstring will insert a templated docstring with parameters and returns that you can fill in. This encourages good documentation practice for complex ML model code.  
- **Better Comments**: Improves readability of comments by color-coding TODOs, highlights, queries, etc. in your code. *Example:* Comments starting with `// TODO` or `# FIXME` will be styled differently (e.g., TODO in blue) making them stand out. This is great for marking areas in data science code that need review or improvement.

### Jupyter and Data Science **Utilities**
- **Python Indent**: Automatically fixes indentation when pressing Enter in Python files, which can reduce formatting errors. *Example:* After an `if:` line, when you press Enter, it auto-indents on the new line to start the block, saving keystrokes and preventing indent mistakes.  
- **TensorBoard**: Integrates TensorBoard into VS Code’s interface. *Example:* After training a neural network with TensorFlow/PyTorch and logging metrics, open the Command Palette and run “**Python: Launch TensorBoard**” to see training curves and model graphs in a VS Code tab – no need to switch to a browser. This helps you monitor experiments directly in your IDE.  
- **Visual Studio IntelliCode**: Gives AI-enhanced completions for Python (and other languages) based on thousands of open-source projects. It predicts the most likely API usage (like the next argument or method call) and surfaces those first. Complements Pylance by sorting suggestions smartly.

### Remote Development (SSH/WSL)
- **Remote - SSH** and **Remote - WSL**: If your data or training environment lives on a remote server or WSL2 (Linux on Windows), these extensions let you attach VS Code to those environments. *Example:* Use **Remote - SSH** to code directly on a GPU machine in the cloud via VS Code, or **Remote - WSL** to develop in your local Linux environment – all while enjoying the full VS Code functionality as if it’s local.

---