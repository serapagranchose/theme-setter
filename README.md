# wallpaper_setter

## Applying the theme to new terminals

`wal` only applies the new colors to the currently open terminals. Any new terminal windows you open won't use the new theme unless you add a single line to your shell's start up file.

Add this line to your shell startup file. (`.bashrc`, `.zshrc`, `.mkshrc` etc.)

```sh
# Import colorscheme from 'wal' asynchronously
# &   # Run the process in the background.
# ( ) # Hide shell job control messages.
# Not supported in the "fish" shell.
(cat ~/.cache/wal/sequences &)

# Alternative (blocks terminal for 0-3ms)
cat ~/.cache/wal/sequences

# To add support for TTYs this line can be optionally added.
source ~/.cache/wal/colors-tty.sh
```
