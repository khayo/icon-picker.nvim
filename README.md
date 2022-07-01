# icon-picker.nvim

icon-picker.nvim is a Neovim plugin that helps you pick 𝑨𝕃𝚻 Font Characters, Symbols Σ, Nerd Font Icons  & Emojis ✨

https://user-images.githubusercontent.com/102876811/174574267-d38861f2-cd11-416f-81b8-93ff115fe6b5.mp4

https://user-images.githubusercontent.com/102876811/174574279-37d4dc95-3fa3-41e2-881c-4c89860bbe22.mp4

![Pick Symbol Screenshot](https://user-images.githubusercontent.com/102876811/174749829-de1f8ab6-bd5a-4c5e-87db-78c3b5c96d49.png)

![Alt Font Screenshot](https://user-images.githubusercontent.com/102876811/174749842-4802bd94-d517-4e53-942a-53351646f5cc.png)

# Installation

#### This plugin utilizes `vim.ui.select()`, so you're gonna need something like [dressing.nvim](https://github.com/stevearc/dressing.nvim) and a fuzzy finder like [Telescope](nvim-telescope/telescope.nvim) or [fzf-lua](https://github.com/ibhagwan/fzf-lua)

For Packer

```lua
use "stevearc/dressing.nvim"
use({
  "ziontee113/icon-picker.nvim",
  config = function()
    require("icon-picker")
  end,
})
```

# Usage

#### Sample Config:

```lua
local opts = { noremap = true, silent = true }

vim.keymap.set("n", "<Leader><Leader>i", "<cmd>PickIcons<cr>", opts)
vim.keymap.set("i", "<C-i>", "<cmd>PickInsert<cr>", opts)
vim.keymap.set("i", "<A-i>", "<cmd>PickAltFontAndSymbolsInsert<cr>", opts)
```

I personally use `<C-i>` for `PickIconsInsert`. If you also want to map `<C-I>` and can't do it, you can check out my quick guide to solve that on YouTube: [Enable Special Keyboard Combinations in Alacritty / Kitty for Neovim](https://www.youtube.com/watch?v=lHBD6pdJ-Ng)

#### Available Commands:

- Normal Mode:
  - `PickEverything` (Nerd Font Icons & Emojis & Alt Font & Symbols)
  - `PickIcons` (Nerd Font Icons & Emojis)
  - `PickEmoji`
  - `PickNerd`
  - `PickSymbols`
  - `PickAltFont`
  - `PickAltFontAndSymbols`
- Insert Mode:
  - `PickEverythingInsert` (Nerd Font Icons & Emojis & Alt Font & Symbols)
  - `PickIconsInsert` (Nerd Font Icons & Emojis)
  - `PickEmojiInsert`
  - `PickNerdInsert`
  - `PickSymbolsInsert`
  - `PickAltFontInsert`
  - `PickAltFontAndSymbolsInsert`

You can use `:help ` to see the details for any of those commands.
Example: `:help PickAltFont`

## Todo:

Fine tune the Insert Mode experience.

## Feedback

If you run into issues or come up with an awesome idea, please feel free to open an issue or PR.

## License

The project is licensed under MIT license. See [LICENSE](./LICENSE) file for details.
