# Built-in Modules (VyScript)

This file contains documentation for all built-in modules included with VyScript.

---

## cursor

### Description

Controls the user's mouse cursor.

### Dependencies

* pyautogui

Install if missing:

```bash
pip install pyautogui
```

### Functions

#### MOVE(x, y)

Moves the mouse cursor to the specified screen coordinates.

#### CLICK()

Clicks the mouse at the current cursor position.

---

## vytime

### Description

Provides time-related utilities for controlling execution flow.

### Dependencies

* None

### Functions

#### pause(x)

Pauses execution for `x` seconds (blocking).

---

## file

### Description

Provides basic file reading and writing utilities.

### Dependencies

* None

### Functions

#### getContent(file)

Returns the content of the specified file.

#### appendTo(file, text)

Appends text to the end of a file without overwriting existing content.

#### wipeAndWrite(file, text)

Clears a file and writes new text to it.

---

## rand

### Description

Provides random number utilities.

### Dependencies

* None

### Functions

#### pick(start, end)

Returns a random number between `start` and `end`.

---

## vywin

### Description

GUI module built on top of Python tkinter, used to create windows and interface elements.

### Dependencies

* tkinter (usually built-in with Python)

---

### Functions

#### window(title)

Creates a window with the given title and returns it.

VyScript

```
var win = Vywin.use -> window("My App")
```

---

#### loop(root)

Starts the GUI event loop.

VyScript

```
Vywin.use -> loop(win)
```

---

#### button(root, text, ev)

Creates a button.

Text and event must be passed as named arguments.

VyScript

```
Vywin.use -> button(win, text="Click Me", ev=myFunction)
```

---

#### text(root, text)

Creates a text label.

Must use named argument.

VyScript

```
Vywin.use -> text(win, text="Hello")
```

---

#### entry(root)

Creates a text input field.

VyScript

```
var inputBox = Vywin.use -> entry(win)
```

---

#### get(entry)

Returns the value inside an entry field.

VyScript

```
var value = Vywin.use -> get(inputBox)
```

---

#### clear(entry)

Clears the contents of an entry field.

VyScript

```
Vywin.use -> clear(inputBox)
```
