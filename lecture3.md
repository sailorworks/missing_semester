# Complete Vim guide

## Why should we learn Vim?

Most of us like using [VSCode](https://en.wikipedia.org/wiki/Visual_Studio_Code), and there are some pretty awesome features as a graphical editor when compared to other editors out there. On the other hand, [Vim](https://en.wikipedia.org/wiki/Vim_(text_editor)) is the most popular editor that is based within a command line.

Vim has different modes which allows insert and manupilate test quickly. In the end Vim is an editor that can match the speed at which you think.

This documentation was created with Vim.

## Let's understand the basics:

We can understand the Vim's interface as a programming language because different keys give different commands to the editor.

Let's cover a few of them:
- *movement* - (```h```,```j```,```k```,```l```) [left,up,down,right] 
          
  we can learn this by setting up mnemonics for them; knowing the layout of the keyboard tells us that ```h``` is on the leftmost side(among the above keys) and therefore it is used for-moving left. ```j```- jumping down; downward direction. ```k```- kicking the ball up; upward direction and at the end ```l``` i.e on the rightmost side is for-right movement.

- *modes*:

  Normal: for moving around a file and making edits, in the beginning the Vim is always in the noraml mode.
   
  Insert: for inserting text, and to switch in to Insert mode use ```i```.

  Replace: for replacing text, and to switch in to Replace mode use ```R```.

  Visual (plain, line, or block): for selecting blocks of text, and to switch in to Visual mode use ```v```, for Visual line mode ```V```, Visual block mode ```ctrl-v```.

  Command-line: for running a command, and to switch in to Command-line mode use  ' : '(semicolon).
- *buffer, windows and tabs:*
   
   Open files are basically buffers. To open a window use ```:sp```, it will split your screen into two section and both of them will represent the same file until there are changes made. To open a new command use ```tabnew``` and it will take you to new tab.

- *Command-line:*
   It is used for opening, saving, and closing files, and quitting Vim.
   
   For command-line:

    - ```:q``` quit (close window)

    - ```:w``` save (“write”)

    - ```:wq``` save and quit
    
    -  ```:e``` {name of file} open file for editing

    - ```:ls``` show open buffers

    - ```:help``` {topic} open help

- *Edits:*

   Basic idea of Vim was eliminating the use of a mouse as it just takes too much time. So, the following commands helps us edit from the keyboard itself(mnemonices included).

   - ```i``` enter Insert mode

  - ```o``` / ```O``` insert line below- to learn; we can think of it as a hole to directly start typing./ above - 
  - ```d{motion}``` delete {motion}
     e.g. ```dw``` is delete word, ```d0``` is delete to beginning of line
  - ```c{motion}``` change {motion}
    - e.g. ```cw``` is change word
  - ```x``` delete character (equal do dl)
  - ```s``` substitute character (equal to cl)
  - Visual mode + manipulation
     select text, ```d``` to delete it or ```c``` to change it
  - ```u``` to undo, <C-r> to redo
  - ```y``` to copy / “yank” (some other commands like d also copy)
  - ```p``` to paste

  Most of the letter's mnemonics goes without saying.

## Vim plugins:

Vim, like VsCode, supports a large number of plugins that can be downloaded directly from their github repositories. This documentation used a [markdown plugin](https://github.com/junegunn/goyo.vim) although there was no preview option inside the Vim itself. [This](https://vimawesome.com/) is a list of plugins which develpers often use.

## Resources:
These are some resources which are standard to get started with Vim:
 -  [Vim Adventures](https://vim-adventures.com/) is a game to learn Vim
 - [Vim Tips Wiki](http://vim.wikia.com/wiki/Vim_Tips_Wiki)
 - [Vim Advent Calendar](https://vimways.org/2019/) has various Vim tips
 - [Vim Golf](http://www.vimgolf.com/) is code golf, but where the programming language is Vim’s UI
 - [Vi/Vim](https://vi.stackexchange.com/) Stack Exchange
 - [Vim Screencasts](http://vimcasts.org/)
 - [Practical Vim](https://pragprog.com/titles/dnvim2/) (book)
 
 Now let's try using Vim for the next month.
          
Exercise:
          <img width="637" alt="Screenshot 2022-12-21 at 4 37 18 PM" src="https://user-images.githubusercontent.com/97829644/208891722-1357483f-3925-46ce-89d7-f6356fa7009a.png">
