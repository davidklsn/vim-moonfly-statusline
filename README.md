moonfly statusline
==================

_moonfly statusline_ is a simple yet informative _statusline_ for Vim and Neovim
that uses [moonfly](https://github.com/bluz71/vim-moonfly-colors) colors by
default.

:cake: when the `g:moonflyHonorUserDefinedColors` option is enabled the
[nightly](https://github.com/bluz71/vim-nightfly-guicolors) Vim theme will style
the `statusline` using _nightfly_ colors.

Screenshots
-----------

<img width="900" alt="normal" src="https://raw.githubusercontent.com/bluz71/misc-binaries/master/moonfly/moonfly_normal.png">

<img width="900" alt="insert" src="https://raw.githubusercontent.com/bluz71/misc-binaries/master/moonfly/moonfly_insert.png">

<img width="900" alt="visual" src="https://raw.githubusercontent.com/bluz71/misc-binaries/master/moonfly/moonfly_visual.png">

The font in use is [Iosevka](https://github.com/be5invis/Iosevka).

Dependency
----------

First install [moonfly](https://github.com/bluz71/vim-moonfly-colors)

Plugins supported
-----------------

- [fugitive](https://github.com/tpope/vim-fugitive)

- [obsession](https://github.com/tpope/vim-obsession)

- [ALE](https://github.com/dense-analysis/ale)

Installation
------------

Use your favoured plugin manager to install **bluz71/vim-moonfly-statusline**.

If using [vim-plug](https://github.com/junegunn/vim-plug) do the following:

1. Add `Plug 'bluz71/vim-moonfly-statusline'` to your _vimrc_
2. Run `:PlugInstall`

Notice
------

File explorers, such as _NERDTree_ and _netrw_, and certain other special
windows will specifically **not** be styled by this plugin. Mode indicators in
such windows are not useful.

Options
-------

### g:moonflyWithGitBranchCharacter

_moonfly statusline_ supports Tim Pope's
[fugitive](https://github.com/tpope/vim-fugitive) plugin.

The `g:moonflyWithGitBranchCharacter` option specifies whether to display Git
branch details using the Unicode Git branch character `U+E0A0`. By default Git
branches displayed in the `statusline` will not use that character since many
monospace fonts will not contain it. However, some modern fonts, such as [Fira
Code](https://github.com/tonsky/FiraCode) and
[Iosevka](https://github.com/be5invis/Iosevka), do contain the Git branch
character.

If `g:moonflyWithGitBranchCharacter` is unset the default value from
the fugitive plugin will be used.

To display the Unicode Git branch character please add the following to your
_vimrc_:

```viml
let g:moonflyWithGitBranchCharacter = 1
```

The above screenshots are displayed with the Git branch character.

### g:moonflyWithObessionGeometricCharacters

_moonfly statusline_ supports Tim Pope's
[obsession](https://github.com/tpope/vim-obsession) plugin.

The `g:moonflyWithObessionGeometricCharacters` option specifies whether to
display obsession details using Unicode geometric characters (`U+25A0` - Black
Square & `U+25CF` - Black Circle). A modern font, such as
[Iosevka](https://github.com/be5invis/Iosevka), will contain those Unicode
geometric characters.

If `g:moonflyWithObessionGeometricCharacters` is unset the default value from
the obsession plugin will be used.

To display Obsession status with geometric characters please add the following
to your _vimrc_:

```viml
let g:moonflyWithObessionGeometricCharacters = 1
```

### g:moonflyWithALECrossCharacter

_moonfly statusline_ supports the [ALE](https://github.com/dense-analysis/ale)
plugin.

The `g:moonflyWithALECrossCharacter` option specifies whether to indicate ALE
errors using the Unicode cross character (`U+2716`). A modern font, such as
[Iosevka](https://github.com/be5invis/Iosevka), will contain that Unicode
character.

If `g:moonflyWithALECrossCharacter` is unset then a simple `x` will be used to
indicate ALE lint errors.

To use the Unicode cross character please add the following to your _vimrc_:

```viml
let g:moonflyWithALECrossCharacter = 1
```

### g:moonflyHonorUserDefinedColors

The `g:moonflyHonorUserDefinedColors` option specifies whether user-defined, or
theme-defined such as
[nightfly](https://github.com/bluz71/vim-nightfly-guicolors), colors should be
used instead of the default colors from the moonfly color scheme.

```viml
let g:moonflyHonorUserDefinedColors = 1
```

Here is an example user-defined theme override saved in an appropriate `after`
file such as `~/.vim/after/plugin/moonfly-statusline.vim`:

```viml
highlight! link User1 DiffText
highlight! link User2 DiffAdd
highlight! link User3 Search
highlight! link User4 IncSearch
highlight! link User5 StatusLine
highlight! link User6 StatusLine
highlight! link User7 StatusLine
highlight! link User8 StatusLine
```

License
-------

[MIT](https://opensource.org/licenses/MIT)
