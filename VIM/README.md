# Vim Cheat Sheet 
### Contents

1. [Inserting](#inserting)
2. [Cursor movement](#cursor-movement)
3. [Editing](#editing)
4. [Cut and Paste](#cut-and-paste)
5. [Search and Replace](#search-and-replace)
6. [Visual Mode](#visual-mode)
7. [Visual Commands](#visual-commands)
8. [Others](#others)

---


## Inserting

```i``` - insert before the cursor  
```I``` - insert at the beginning of the line  
```a``` - insert (append) after the cursor  
```A``` - insert (append) at the end of the line  
```o``` - append (open) a new line below the current line  
```O``` - append (open) a new line above the current line  
```ea``` - insert (append) at the end of the word  
```Esc``` - exit insert mode 

## Cursor movement


  **Tip:** For example, 4j moves down 4 lines.

```h``` - move cursor left  
```j``` - move cursor down  
```k``` - move cursor up  
```l``` - move cursor right  
```H``` - move to top of screen   
```M``` - move to middle of screen   
```L``` - move to bottom of screen  
```w``` - jump forwards to the start of a word   
```W``` - jump forwards to the start of a word (words can contain punctuation)   
```e``` - jump forwards to the end of a word  
```E``` - jump forwards to the end of a word (words can contain punctuation)  
```b``` - jump backwards to the start of a word  
```B``` - jump backwards to the start of a word (words can contain punctuation)  
```%``` - move to matching character (default supported pairs: '()', '{}', '[]' - use :h matchpairs in vim for more info)  
```0``` - jump to the start of the line  
```^``` - jump to the first non-blank character of the line  
```$``` - jump to the end of the line  
```g_``` - jump to the last non-blank character of the line  
```gg``` - go to the first line of the document
```G``` - go to the last line of the document  
```5G``` - go to line 5  
```fx``` - jump to next occurrence of character x  
```tx``` - jump to before next occurrence of character x  
```Fx``` - jump to previous occurence of character x  
```Tx``` - jump to after previous occurence of character x  
```;``` - repeat previous f, t, F or T movement  
```,``` - repeat previous f, t, F or T movement, backwards  
```}``` - jump to next paragraph (or function/block, when editing code)  
```{``` - jump to previous paragraph (or function/block, when editing code)  
```zz``` - center cursor on screen  
```Ctrl + e``` - move screen down one line (without moving cursor)  
```Ctrl + y``` - move screen up one line (without moving cursor)  
```Ctrl + b``` - move back one full screen  
```Ctrl + f``` - move forward one full screen  
```Ctrl + d``` - move forward 1/2 a screen  
```Ctrl + u``` - move back 1/2 a screen  



## Editing

```r ``` - replace a single character  
```J``` - join line below to the current one with one space in between  
```gJ``` - join line below to the current one without space in between  
```gwip``` - reflow paragraph  
```cc``` - change (replace) entire line  
```cw``` - change (replace) to the end of the word  
```c$``` - change (replace) to the end of the line  
```s``` - delete character and substitute text  
```S``` - delete line and substitute text (same as cc)
```xp``` - transpose two letters (delete and paste)  
```u``` - undo  
```Ctrl + r``` - redo  
```.``` - repeat last command



 ## Cut and Paste

```yy``` - yank (copy) a line  
```2yy``` - yank (copy) 2 lines  
```yw``` - yank (copy) the characters of the word from the cursor position to the start of the next word  
```y$``` - yank (copy) to end of line
```p``` - put (paste) the clipboard after cursor
```P``` - put (paste) before cursor  
```dd``` - delete (cut) a line
```2dd``` - delete (cut) 2 lines  
```dw``` - delete (cut) the characters of the word from the cursor position to the start of the next word  
```D``` - delete (cut) to the end of the line  
```d$``` - delete (cut) to the end of the line  
```x``` - delete (cut) character  


## Search and Replace

```/pattern``` - search for pattern  
```?pattern``` - search backward for pattern  
```\vpattern``` - 'very magic' pattern: non-alphanumeric characters are interpreted as special regex symbols (no escaping needed)  
```n``` - repeat search in same direction   
```N``` - repeat search in opposite direction  
```:%s/old/new/g``` - replace all old with new throughout file  
```:%s/old/new/gc``` - replace all old with new throughout file with confirmations   
```:noh``` - remove highlighting of search matches  


## Visual Mode

```v``` - start visual mode, mark lines, then do a command (like y-yank)  
```V``` - start linewise visual mode   
```o``` - move to other end of marked area   
```Ctrl + v``` - start visual block mode  
```O``` - move to other corner of block  
```aw``` - mark a word  
```ab``` - a block with ()  
```aB``` - a block with {}  
```ib``` - inner block with ()  
```iB``` - inner block with {}  
```Esc``` - exit visual mode  

## Visual Commands

```>``` - shift text right   
```<``` - shift text left  
```y``` - yank (copy) marked text  
```d``` - delete marked text  
```~``` - switch case  

## Others

```:help keyword``` - open help for keyword  
```:o file``` - open file  
```:saveas file``` - save file as  
```:close``` - close current pane  
```K``` - open man page for word under the cursor  