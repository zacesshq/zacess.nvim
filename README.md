# zacess.nvim

![Zacess Dark in an editor: code with keywords, functions, types, strings and comments in distinct high contrast colours on a dark background](previews/zacess-dark.png)

Six Neovim colour schemes matching the [Zacess](https://zacess.com) reader's contrast themes:
`zacess-light`, `zacess-dark`, `zacess-yellow-on-black` for low vision, `zacess-cream` for
dyslexia friendly reading and `zacess-high-contrast-dark` and `zacess-high-contrast-light` for the
highest contrast. Every text and syntax colour keeps at least 7:1 contrast on the
background, the selection and the current line. Each scheme sets `background`, the standard
highlight groups, the Tree-sitter `@` groups, the LSP semantic token groups and the 16 terminal
colours.

## Install

With [lazy.nvim](https://github.com/folke/lazy.nvim):

```lua
{
  "zacesshq/zacess.nvim",
  lazy = false,
  priority = 1000,
  config = function()
    vim.o.termguicolors = true
    vim.cmd.colorscheme("zacess-dark")
  end,
}
```

With any other plugin manager, add `zacesshq/zacess.nvim` and run
`vim.cmd.colorscheme("zacess-dark")`. To install by hand, copy the `colors` folder into
`~/.config/nvim/colors/`.

> [!IMPORTANT]
> The schemes use exact colours, so `termguicolors` must be on and the terminal must support true
> colour. Without it Neovim rounds each colour to the nearest of 256 and the contrast is no longer
> what was measured.

## The six schemes

| Scheme | Background |
| --- | --- |
| `zacess-light` | Ink on white |
| `zacess-dark` | Light text on near black |
| `zacess-yellow-on-black` | Yellow on black, for low vision |
| `zacess-cream` | Black on cream, for dyslexia friendly reading |
| `zacess-high-contrast-dark` | White on pure black, for the highest contrast on a dark screen |
| `zacess-high-contrast-light` | Black on pure white, for the highest contrast on a light screen |

Previews of all six are in [previews](previews).

## Releases

Each release here matches a release of [zacesshq/themes](https://github.com/zacesshq/themes) with
the same version. The full notes for every version are in its
[changelog](https://github.com/zacesshq/themes/blob/main/CHANGELOG.md).

## Where the schemes are made

> [!NOTE]
> This repository is a read-only copy for Neovim plugin managers. The schemes are generated from
> one palette in [zacesshq/themes](https://github.com/zacesshq/themes), which also has the
> same themes for VS Code, JetBrains IDEs, Obsidian, Zed and terminals. Issues, ideas and pull
> requests go there.

## Licence

[MIT](LICENSE)
