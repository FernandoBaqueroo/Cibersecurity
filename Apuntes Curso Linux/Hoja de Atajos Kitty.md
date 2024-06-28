# 🐱 Kitty Terminal Emulator

## 🌟 Overview

**kitty** is a terminal emulator designed for power users, focusing on keyboard control, configurability, and extensibility. It is written in C, Python, and Go for performance, flexibility, and command-line utility respectively, and uses OpenGL for rendering.

## 🎨 Design Philosophy

1. **🖥️ Keyboard-centric Controls**: All actions can be performed via keyboard shortcuts.
2. **📝 Simple Configuration**: Configurations are stored in a single, human-readable file.
3. **🛠️ Hackable and Extensible**: Easy to add new features and customize.

## 🗂️ Tabs and Windows

kitty supports multiple programs organized into tabs and windows.

### 🔄 Scrolling

| Action                      | Shortcut (Windows/Linux)          | Shortcut (macOS)             |
|-----------------------------|-----------------------------------|------------------------------|
| Line up                     | `ctrl+shift+up`                   | `⌥+⌘+⇞` / `⌘+↑`              |
| Line down                   | `ctrl+shift+down`                 | `⌥+⌘+⇟` / `⌘+↓`              |
| Page up                     | `ctrl+shift+page_up`              | `⌘+⇞`                        |
| Page down                   | `ctrl+shift+page_down`            | `⌘+⇟`                        |
| Top                         | `ctrl+shift+home`                 | `⌘+↖`                        |
| Bottom                      | `ctrl+shift+end`                  | `⌘+↘`                        |
| Previous shell prompt       | `ctrl+shift+z`                    |                              |
| Next shell prompt           | `ctrl+shift+x`                    |                              |
| Browse scrollback in less   | `ctrl+shift+h`                    |                              |
| Browse last cmd output      | `ctrl+shift+g`                    |                              |

### 🗂️ Tabs

| Action                      | Shortcut (Windows/Linux)          | Shortcut (macOS)             |
|-----------------------------|-----------------------------------|------------------------------|
| New tab                     | `ctrl+shift+t`                    | `⌘+t`                        |
| Close tab                   | `ctrl+shift+q`                    | `⌘+w`                        |
| Next tab                    | `ctrl+shift+right`                | `⌃+⇥` / `⇧+⌘+]`              |
| Previous tab                | `ctrl+shift+left`                 | `⇧+⌃+⇥` / `⇧+⌘+[ `           |
| Next layout                 | `ctrl+shift+l`                    |                              |
| Move tab forward            | `ctrl+shift+.`                    |                              |
| Move tab backward           | `ctrl+shift+,`                    |                              |
| Set tab title               | `ctrl+shift+alt+t`                | `⇧+⌘+i`                      |

### 🔲 Windows

| Action                      | Shortcut (Windows/Linux)          | Shortcut (macOS)             |
|-----------------------------|-----------------------------------|------------------------------|
| New window                  | `ctrl+shift+enter`                | `⌘+↩`                        |
| New OS window               | `ctrl+shift+n`                    | `⌘+n`                        |
| Close window                | `ctrl+shift+w`                    | `⇧+⌘+d`                      |
| Resize window               | `ctrl+shift+r`                    | `⌘+r`                        |
| Next window                 | `ctrl+shift+]`                    |                              |
| Previous window             | `ctrl+shift+[ `                   |                              |
| Move window forward         | `ctrl+shift+f`                    |                              |
| Move window backward        | `ctrl+shift+b`                    |                              |
| Move window to top          | `ctrl+shift+\``                   |                              |
| Visually focus window       | `ctrl+shift+f7`                   |                              |
| Visually swap window        | `ctrl+shift+f8`                   |                              |
| Focus specific window       | `ctrl+shift+1...0`                | `⌘+1...9`                    |

### ⌨️ Additional Shortcuts

| Action                      | Shortcut (Windows/Linux)          | Shortcut (macOS)             |
|-----------------------------|-----------------------------------|------------------------------|
| Show help                   | `ctrl+shift+f1`                   |                              |
| Copy to clipboard           | `ctrl+shift+c`                    | `⌘+c`                        |
| Paste from clipboard        | `ctrl+shift+v`                    | `⌘+v`                        |
| Paste from selection        | `ctrl+shift+s`                    |                              |
| Pass selection to program   | `ctrl+shift+o`                    |                              |
| Increase font size          | `ctrl+shift+equal`                | `⌘++`                        |
| Decrease font size          | `ctrl+shift+minus`                | `⌘+-`                        |
| Restore font size           | `ctrl+shift+backspace`            | `⌘+0`                        |
| Toggle fullscreen           | `ctrl+shift+f11`                  | `⌃+⌘+f`                      |
| Toggle maximized            | `ctrl+shift+f10`                  |                              |
| Input Unicode character     | `ctrl+shift+u`                    | `⌃+⌘+space`                  |
| Open URL in web browser     | `ctrl+shift+e`                    |                              |
| Reset the terminal          | `ctrl+shift+delete`               | `⌥+⌘+r`                      |
| Edit kitty.conf             | `ctrl+shift+f2`                   | `⌘+,`                        |
| Reload kitty.conf           | `ctrl+shift+f5`                   | `⌃+⌘+,`                      |
| Debug kitty.conf            | `ctrl+shift+f6`                   | `⌥+⌘+,`                      |
| Open a kitty shell          | `ctrl+shift+escape`               |                              |
| Increase background opacity | `ctrl+shift+a>m`                  |                              |
| Decrease background opacity | `ctrl+shift+a>l`                  |                              |
| Full background opacity     | `ctrl+shift+a>1`                  |                              |
| Reset background opacity    | `ctrl+shift+a>d`                  |                              |

## ⚙️ Configuring kitty

kitty is highly configurable, allowing you to tweak everything from keyboard shortcuts to rendering options. Press `ctrl+shift+f2` to open the configuration file in your text editor. For more details, refer to the [configuration docs](https://sw.kovidgoyal.net/kitty/conf.html).

## 🖼️ Layouts

kitty supports seven different window layouts:

1. **Fat**: Full-width windows on top, side-by-side windows on the bottom.
2. **Grid**: All windows in a grid.
3. **Horizontal**: All windows side-by-side.
4. **Splits**: Arbitrary patterns using horizontal and vertical splits.
5. **Stack**: One maximized window at a time.
6. **Tall**: Full-height windows on the left, stacked windows on the right.
7. **Vertical**: All windows stacked vertically.

Switch layouts with `ctrl+shift+l` or customize your own layout shortcuts.

## 🐍 Extending kitty

kitty supports scripting through small terminal programs called **kittens**. You can create custom kittens for additional features or use existing ones. Examples include viewing images or diffing files with image support.

### 🕵️‍♂️ Watchers Framework

Create Python scripts that respond to events like window resizing or closing.

## 🔧 Remote Control

Control kitty from the shell prompt, even over SSH. Change colors, fonts, open new windows/tabs, set titles, and more. Refer to the [tutorial](https://sw.kovidgoyal.net/kitty/remote-control.html) to get started.

## 🚀 Startup Sessions

Create session files to control the layout, working directory, startup programs, etc. Use the `kitty --session` command line flag or `startup_session` option in `kitty.conf`.

### Example

```shell
layout tall
cd ~
launch zsh
new_tab my tab
cd ~/somewhere
enabled_layouts tall,stack
layout stack
launch zsh
new_os_window
os_window_size 80c 24c
launch sh
resize_window wider 2
focus
focus_os_window
launch emacs

