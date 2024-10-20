# Jefferson Ding - NeoVim Config for Colemak

## <center>Original Source: [The Ultimate NeoVim Config for Colemak Users](https://github.com/theniceboy/nvim)</center>

## Keyboard Shortcuts

### 1 Basic Editor Features

#### 1.1 The Most Basics

**`k`** : switchs to **`INSERT`** : mode (same as key `i` in vanilla vim)

**`Q`** : quits current vim window (same as command `:q` in vanilla vim)

**`S`** : saves the current file (same as command `:w` in vanilla vim)

**_IMPORTANT_**

Since the `i` key has been mapped to `k`, every command (combination) that involves `i` should use `k` instead (for example, `ciw` should be `ckw`).

#### 1.2 Remapped Cursor Movement

| Shortcut   | Action                                                    | Equivalent |
|------------|-----------------------------------------------------------|------------|
| `u`        | Cursor up a terminal line                                 | `k`        |
| `e`        | Cursor down a terminal line                               | `j`        |
| `n`        | Cursor left                                               | `h`        |
| `i`        | Cursor right                                              | `l`        |
| `U`        | Cursor up 5 terminal lines                                | `5k`       |
| `E`        | Cursor down 5 terminal lines                              | `5j`       |
| `N`        | Cursor to the start of the line                           | `0`        |
| `I`        | Cursor to the end of the line                             | `$`        |
| `Ctrl` `u` | Move the view port up 5 lines without moving the cursor   | `Ctrl` `y` |
| `Ctrl` `e` | Move the view port down 5 lines without moving the cursor | `Ctrl` `e` |
| `h`        | Move to the end of this word                              | `e`        |
| `w`        | Move cursor one word forward                              | `w`       |
| `b`        | Move cursor one word backwards                            | `b`       |
| `W`        | Move cursor five words forward                             | `5w`       |
| `B`        | Move cursor five words forward                            | `5b`       |

#### 1.3 Remapped Insert Mode Keys

| Shortcut   | Action                                                               |
|------------|----------------------------------------------------------------------|
| `Ctrl` `a` | Move cursor to the end of the line                                   |

#### 1.4 Remapped Text Manipulating Commands in Normal Mode

| Shortcut        | Action                                |
|-----------------|---------------------------------------|
| `l`             | **undo**               |
|`ctl+r`          |**redo**                               |
| `<`             | Un-indent                             |
| `>`             | Indent                                |
| `SPACE` `SPACE` | Goto the next placeholder (`<++>`)    |

#### 1.5 Other Useful Normal Mode Remappings

| Shortcut        | Action                                         |
|-----------------|------------------------------------------------|
| `r`             | **Compile/Run the current file**               |
| `SPACE` `s` `c` | Toggle spell suggestion a                      |
| `SPACE` `o`     | Fold                                           |
| `SPACE` `-`     | Previous quick-fix position                    |
| `SPACE` `+`     | Next quick-fix position                        |
| `SPACE` `/`     | Create a new terminal below the current window |

#### 1.6 Remapped Commands in Visual Mode

| Shortcut        | Action                                 |
|-----------------|----------------------------------------|
| `Y`             | Copy selected text to system clipboard |

#### 1.7 Common NVim Commands

##### 1.7.1 Cursor Movement

|Shortcut|Action|
|--------|------|
|`w`|Jump by start of words|
|`b`|Jump backwards by words|
|`0`|Jump to start of line|
|`$`|Jump to end of line|
|`ctl+d`|Move down half a page|
|`ctl+u`|Move up half a page|
|`}`|Move to next paragraph|
|`{`|Move to previous paragraph|
|`gg`|Jump to top of page|
|`G`|Jump to bottom of page|

##### 1.7.2 Insert Appending and Editing Text

|Shortcut|Action|
|--------|------|
|`k`|Start insert mode at cursor|
|`K`|Start insert mode at beginning of line|
|`a`|Start insert mode after cursor(append)|
|`A`|Start insert mode at end of line|
|`o`|Open blank line below current line|
|`O`|Open blank line above current line|
|`c`|Delete the marked text and replace(from visual mode)|
|`cc`|Change entire line|
|`r [char]`|Replace a single char|
|`d [movement]`|Delete|
|`de`|Delete word|
|`dd`|Delete line|
|`y`|Copy(Yank) Text|
|`p`|Paste after cursor|
|`P`|Paste before cursor|
|`x`|Delete current Char|

##### 1.7.3 Find and Replace

|Shortcut|Action|
|--------|------|
|`/[pattern]`|Search for pattern|
|`?[pattern]`|Search backwards for pattern|
|`n`|Repeat search in same direction|
|`N`|Repeat search in opposite direction|
|`:s/[old]/[new]/gn`|Replace all old with new through file|

### 2 Window Management

#### 2.1 Creating Window Through Split Screen

| Shortcut    | Action                                                                      |
|-------------|-----------------------------------------------------------------------------|
| `s` `u`     | Create a new horizontal split screen and place it above the current window  |
| `s` `e`     | Create a new horizontal split screen and place it below the current window  |
| `s` `n`     | Create a new vertical split screen and place it left to the current window  |
| `s` `i`     | Create a new vertical split screen and place it right to the current window |
| `s` `v`     | Set the two splits to be vertical                                           |
| `s` `h`     | Set the two splits to be horizontal                                         |
| `s` `r` `v` | Rotate splits and arrange splits vertically                                 |
| `s` `r` `h` | Rotate splits and arrange splits horizontally                               |

#### 2.2 Moving the Cursor Between Different Windows

| Shortcut      | Action                         |
|---------------|--------------------------------|
| `SPACE` + `w` | Move cursor to the next window |
| `SPACE` + `n` | Move cursor one window left    |
| `SPACE` + `i` | Move cursor one window right   |
| `SPACE` + `u` | Move cursor one window up      |
| `SPACE` + `e` | Move cursor one window down    |

#### 2.3 Resizing Different Windows

Use the arrow keys to resize the current window.

#### 2.4 Closing Windows

| Shortcut    | Action                                                                                                     |
|-------------|------------------------------------------------------------------------------------------------------------|
| `Q`         | Close the current window                                                                                   |
| `SPACE` `q` | Close the window below the current window. (The current window will be closed if there is no window below) |

### 3 Tab Management

| Shortcut    | Action           |
|-------------|------------------|
| `t` `u`     | Create a new tab |
| `t` `n`     | Go one tab left  |
| `t` `i`     | Go One tab right |
| `t` `m` `n` | Move tab left    |
| `t` `m` `i` | Move tab right   |

### NerdTree

| Shortcut    | Action                      |
|-------------|-----------------------------|
| `\t`        | Toggle NerdTree             |
| `t` `enter` | Open in new tab             |
| `T` `enter` | Open in new tab silently    |
| `C`         | Change root to selected dir |
| `a`         | Move tree root up a dir     |
| `r`         | Refresh cursor dir          |
| `f`         | Explore directory           |

### 4 Terminal Keyboard Shortcuts

| Shortcut    | Action                                                      |
|-------------|-------------------------------------------------------------|
| `Ctrl` `n`  | Escape from terminal input mode                             |

## Plugin Setups

### Instant Markdown Preview

Install the mini-server by running:

```
    [sudo] npm -g install instant-markdown-d
    or
    pip install --user smdv
```

