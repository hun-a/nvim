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

# Troubleshooting
- Install the `codelldb` by `Mason`
  ```
  $ vi
  --- nvim ---
  :MasonInstall codelldb
  ```

# References
- [dev-environment-files](https://github.com/josean-dev/dev-environment-files)
