# Neo-vim settings for me!

# Prerequisites
- Install the `ripgrep` for `Telescope`
  - Mac
    ```
    $ brew install ripgrep 
    ```
  - Ubuntu
    ```
    $ sudo apt-get install -y ripgrep
    ```
- Install `Meslo LG M DZ Regular Nerd Font Complete Mono` for `nvim-tree`
  - Font files in [here](./font/)

# Debugging
### Rust
- Dubugging for binary project.
  1. Compile rust project with `cargo build`, `cargo run`.
  2. Copy & Paste [.vimspector.json](./rust/.vimspector.json) to the root directory of your rust project.
  3. Create breakpoint in your code. (Maybe shortcut `Db`)
  4. Run the debugger. (Maybe shortcut `F9`)
- Debugging for test.
  1. Run the test with `cargo test`.
     - Remember your test binary path (like `target/debug/deps/app-0682f52a2359de0`)
  2. Copy & Paste [.vimspector.json](./rust/.vimspector.json) to the root directory of your rust project.
  3. Update program path which you remember above.
  4. Create breakpoint in your code. (Maybe shortcut `Db`)
  5. Run the debugger. (Maybe shortcut `F9`)

# Shortcuts
|Plugin|Action|Mode|Binding|Command|
|------|------|----|-------|-------|
|lsp-config|show definition, references|n|`gf`|`<cmd>Lspsaga lsp_finder<CR>`|
|lsp-config|got to declaration|n|`gD`|`<Cmd>lua vim.lsp.buf.declaration()<CR>`|
|lsp-config|see definition and make edits in window|n|`gd`|`<cmd>Lspsaga peek_definition<CR>`|
|lsp-config|go to implementation|n|`gi`|`<cmd>lua vim.lsp.buf.implementation()<CR>`|
|lsp-config|see available code actions|n|`<leader>ca`|`<cmd>Lspsaga code_action<CR>`|
|lsp-config|smart rename|n|`<leader>rn`|`<cmd>Lspsaga rename<CR>`|
|lsp-config|show diagnostics for line|n|`<leader>D`|`<cmd>Lspsaga show_line_diagnostics<CR>`|
|lsp-config|show diagnostics for cursor|n|`<leader>d`|`<cmd>Lspsaga show_cursor_diagnostics<CR>`|
|lsp-config|jump to previous diagnostic in buffer|n|`[d`|`<cmd>Lspsaga diagnostic_jump_prev<CR>`|
|lsp-config|jump to next diagnostic in buffer|n|`]d`|`<cmd>Lspsaga diagnostic_jump_next<CR>`|
|lsp-config|show documentation for what is under cursor|n|`K`|`<cmd>Lspsaga hover_doc<CR>`|
|lsp-config|see outline on right hand side|n|`<leader>o`|`<cmd>LSoutlineToggle<CR>`|
|lspsaga|move prev in lspsaga|n|`C-k`|`prev`|
|lspsaga|move next in lspsaga|n|`C-j`|`next`|
|lspsaga|to open file with definition preview in lspsaga|n|`<CR>`| |
|cmp|mapping select prev item|n|`C-[`|`cmp.mapping.select_prev_item()`|
|cmp|mapping select next item|n|`C-]`|`cmp.mapping.select_next_item()`|
|cmp|mapping select prev item|n|`S-Tab`|`cmp.mapping.select_prev_item()`|
|cmp|mapping select next item|n|`Tab`|`cmp.mapping.select_next_item()`|
|cmp|mapping scroll docs to the 4 position before|n|`C-d`|`cmp.mapping.scroll_docs(-4)`|
|cmp|mapping scroll docs to the 4 position ahead|n|`C-f`|`cmp.mapping.scroll_docs(4)`|
|cmp|mapping close|n|`C-e`|`cmp.mapping.close()`|
|cmp|mapping confirm|n|`CR`|`cmp.mapping.confirm`|
|typescript|rename file and update imports|n|`<leader>rf`|`TypescriptRenameFile<CR>`|
|typescript|organize imports|n|`<leader>oi`|`TypescriptOrganizeImports<CR>`|
|typescript|remove unused variables|n|`<leader>ru`|`TypescriptRemoveUnused<CR>`|
|rust-tools|hover action for rost-tools|n|`<Leader>h`|`rt.hover_actions.hover_actions`|
|rust-tools|code action group for rust-tools|n|`<Leader>a`|`rt.code_action_group.code_action_group`|
|telescope|move to prev result| |`C-k`|`actions.move_selection_previous`|
|telescope|move to next result| |`C-j`|`actions.move_selection_next`|
|telescope|send selected to quickfixlist| |`C-q`|`actions.send_selected_to_qflist + actions.open_qflist`|
|telescope|find files within current working directory, respects .gitignore|n|`<leader>ff`|`<cmd>Telescope find_files<cr>`| 
|telescope|find string in current working directory as you type|n|`<leader>fs`|`<cmd>Telescope live_grep<cr>`| 
|telescope|find string under cursor in current working directory|n|`<leader>fc`|`<cmd>Telescope grep_string<cr>`| 
|telescope|list open buffers in current neovim instance|n|`<leader>fb`|`<cmd>Telescope buffers<cr>`| 
|telescope|list available help help_tags|n|`<leader>fh`|`<cmd>Telescope help_tags<cr>`| 
|telescope|list all git commits (use <cr> to checkout) ["gc" for git commits]|n|`<leader>gc`|`<cmd>Telescope git_commits<cr>`| 
|telescope|list git commits for current file/buffer (use <cr> to checkout) ["gfc" for git file commits]|n|`<leader>gfc`|`<cmd>Telescope git_bcommits<cr>`| 
|telescope|list git branches (use <cr> to checkout) ["gb" for git branch]|n|`<leader>gb`|`<cmd>Telescope git_branches<cr>`| 
|telescope|list current changes per file with diff preview ["gs" for git status]|n|`<leader>gs`|`<cmd>Telescope git_status<cr>`| 
|nvim-tree|toggle file explorer|n|`<leader>e`|`<cmd>NvimTreeToggle<CR>`| 
|vimspector|launch debugger |n|`F9`|`<cmd>vimspector#Launch()`|
|vimspector|step over|n|`F5`|`<cmd>vimspector#StepOver()<CR>`|
|vimspector|step into|n|`F6`|`<cmd>vimspector#StepInto()`|
|vimspector|step out|n|`F7`|`<cmd>vimspector#StepOut()`|
|vimspector|reset|n|`F8`|`<cmd>vimspector#Reset()`|
|vimspector|set breakpoint to the source code line|n|`Db`|`call vimspector#ToggleBreakpoint()<CR>`|
|vimspector|add watcher|n|`Dw`|`call vimspector#AddWatch()<CR>`|
|vimspector|evaluate|n|`De`|`call vimspector#Evaluate()<CR>`|

# Troubleshooting
- Install the `codelldb` by `Mason`
  ```
  $ vi
  --- nvim ---
  :MasonInstall codelldb
  ```

# References
- [dev-environment-files](https://github.com/josean-dev/dev-environment-files)
