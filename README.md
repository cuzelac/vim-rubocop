# Vim RuboCop

The **Vim RuboCop** plugin runs [RuboCop](https://github.com/bbatsov/rubocop) and displays the results in Vim.

## Requirements

Please note that the current version of the Vim RuboCop plugin requires RuboCop 0.12.0 or later.

## Installation

Obtain a copy of this plugin and place `rubocop.vim` in your Vim plugin directory.

## Usage

You can use the `:RuboCop` command to run RuboCop and display the results.

You can also use the `:RuboCop` command together with options. For example, `:RuboCop -l`, `:RuboCop -a` and so on.

You can use the `:RuboCopAutoCorrect` command to write out your buffer,
run `rubocop -a` on the file and re-open it in your buffer.  This will
prevent the results window from opening.

### Configuration File

To run with the specified configuration file, add the following line to your `.vimrc` file:

```viml
let g:vimrubocop_config = '/path/to/rubocop.yml'
```

### Keyboard Shortcuts

Credit for Shortcuts: [Ack.vim](https://github.com/mileszs/ack.vim)

In the quickfix window, you can use:

    o    to open (same as enter)
    go   to preview file (open but maintain focus on ack.vim results)
    t    to open in new tab
    T    to open in new tab silently
    h    to open in horizontal split
    H    to open in horizontal split silently
    v    to open in vertical split
    gv   to open in vertical split silently
    q    to close the quickfix window

Additionally, the plugin registers:

* `<Leader>ru` in normal mode for triggering `:RuboCop`
* `<Leader>ra` in normal mode for triggering `:RuboCopAutoCorrect`

You can disable these default mappings by setting
`g:vimrubocop_keymap` in your `.vimrc` file, and then remap them differently.

For instance, to trigger RuboCop by pressing `<Leader>r` you can put the following in
your `.vimrc`:

```viml
let g:vimrubocop_keymap = 0
nmap <Leader>r :RuboCop<CR>
nmap <Leader>a :RuboCopAutoCorrect<CR>
```

## License

The Vim RuboCop plugin is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
