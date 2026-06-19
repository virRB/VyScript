# Built-in Modules (VyScript)

This file contains documentation for all built-in modules included with VyScript.

---

VyScript provides several built-in modules for common tasks such as file handling, randomness, time control, GUI creation, cursor control, and AI interaction.

The cursor module allows control of the system mouse cursor. It depends on pyautogui, which must be installed separately. It provides two functions: MOVE(x, y), which moves the cursor to a specific screen position, and CLICK(), which performs a mouse click at the current cursor location.

The vytime module provides basic time utilities. It has no external dependencies. Its primary function is pause(seconds), which halts execution for a given number of seconds.

The file module provides simple file input and output functionality. It supports reading and modifying files using three functions: getContent(file) reads and returns file contents, appendTo(file, text) appends text to a file, and wipeAndWrite(file, text) clears a file and writes new content.

The rand module provides random number generation utilities. It has no dependencies. Its function pick(start, end) returns a random integer between the provided range values.

The vywin module provides a simple graphical user interface system built on top of tkinter. It allows the creation of windows, buttons, labels, and input fields. It depends on tkinter, which is usually included with Python. The module includes window(title) to create a window, loop(window) to start the GUI event loop, button(window, text, ev) to create clickable buttons with optional event callbacks, text(window, text) to display labels, entry(window) to create input fields, get(entry) to retrieve input field content, and clear(entry) to clear input fields.

The virgpt module provides access to a local AI model through Ollama. It requires both the requests library and a running local installation of Ollama. It provides a single function, askAI(prompt, personality), which sends a prompt to the model and returns a response. The personality parameter is optional and modifies the tone or style of the AI response. If no personality is provided, the model responds normally.

All modules in VyScript are accessed using a consistent syntax:

module.use -> function()
