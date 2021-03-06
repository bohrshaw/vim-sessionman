# mansion.vim :arrows_clockwise: :relieved:

**mansion** is a Vim session manager. It's all about managing session files. So the options like 'sessionoptions', 'viewoptions', 'viminfo' are not touched. You may find it simple and convenient.

### Usage

Commands provided are self-explained, such as `SessionOpen`, `SessionClose`, `SessionSave`, etc. See `:com Session` for all additional commands. The argument to a command is a session file specification(Look into `mansion#session_path()` for how an argument is translated to a full session file path.). And an extra `:Restart` command is also provided for restarting gVim.

Corresponding mappings are also provided. But you can disable them all if you wish(See below). See `:exe 'map <Leader>s'` for default mappings.

### Session persistence

A session could be saved in the following occasions:
- Before Vim exits.
- After a user defined time(`g:mansion_save_time`), repeatedly.
- Whenever the focused buffer is different(`:SessionFollow`).

### Configuration
- Set the central path of session files: `let g:sessiondir = '~/.vim/session'` (default)
- Disable auto-saving the current session before exiting Vim: `let g:mansion_no_save_on_exit = 1`
- Disable default mappings: `let g:mansion_no_maps = 1`
- Remember the session name when Vim exits: `set viminfo^=!`

### Installation
- [Pathogen](https://github.com/tpope/vim-pathogen):
    `cd ~/.vim/bundle && git clone git://github.com/bohrshaw/vim-mansion.git`
- [Vundle](https://github.com/gmarik/vundle):
    Add `Bundle 'bohrshaw/vim-mansion'` to '.vimrc' and run `:BundleInstall`.

### Related
- [vim-sessionman](http://www.vim.org/scripts/script.php?script_id=2010)
- [vim-obsession](https://github.com/tpope/vim-obsession)

### License
Copyright (c) Bohr Shaw. Distributed under the same terms as Vim itself.
See `:help license`.
