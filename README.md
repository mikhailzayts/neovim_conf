# Setting up Neovim on Windows

## Basic installation
1) `winget install Neovim.Neovim`
2) 
```
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |
ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/  nvim-data/site/autoload/plug.vim" -Force
```
3) https://jdhao.github.io/2018/11/15/neovim_configuration_windows/

## Setting up LSP:
1) Add `Plug 'neovim/nvim-lspconfig'` to the init.vim plugins list
2) Install clangd LSP server `scoop install clangd`
3) Copy configuration from https://github.com/neovim/nvim-lspconfig in the init.vim
4) Set up clangd support with `require'lspconfig'.clangd.setup{}` 

## Different plugins
