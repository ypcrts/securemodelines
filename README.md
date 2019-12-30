<!-- vi: ft=markdown tw=80 ts=2 sw=2 sts=2 fdm=marker fmr={{{,}}} et: -->
# securemodelines
A secure alternative to Vim modelines

This is a maintained fork of the [original vimscript](https://github.com/ciaranm/securemodelines).

## Description

Vim's internal modeline support allows all sorts of annoying and potentially
insecure options to be set. This script implements a much more heavily
restricted modeline parser that permits only user-specified options to be set.

## Installation

No configuration required.
Using [vim-plug](https://github.com/junegunn/vim-plug)
```vim
Plug 'ypcrts/securemodelines'
```


##  Internals
The `g:secure_modelines_allowed_items` array contains allowed options.  See
`:help securemodelines_options` for default values.

The `g:secure_modelines_verbose` variable, if set to something true, will make
the script warn when a modeline attempts to set any other option.

The `g:secure_modelines_modelines` variable overrides the number of lines to
check. By default it is 5.

If `g:secure_modelines_leave_modeline` is defined, the script will not clobber
&modeline. Otherwise &modeline will be unset.

If `b:disable_secure_modelines` is defined, securemodelines will not run for
the current buffer. The intent being to turn off securemodelines in an
ftplugin.


## Contributors

See the [contributors
graph](https://github.com/ypcrts/securemodelines/graphs/contributors).
