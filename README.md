# Zed Assembly Syntax

Extension for [Zed](https://zed.dev) that adds assembly syntax highlighting and [`asm-lsp`](https://github.com/bergercookie/asm-lsp) support.

## Language Server

You can configure the language server by creating a `.asm-lsp.toml` in the root of your workspace

Example `.asm-lsp.toml` for cross-compiled assembly:
```toml
[default_config]
assembler = "gas"
instruction_set = "riscv"

[default_config.opts]
compiler = "riscv64-unknown-elf-gcc"
```

See the [asm-lsp README.md](https://github.com/bergercookie/asm-lsp?tab=readme-ov-file#optional-configure-via-asm-lsptoml) for more configuration options

### Disabling the Language Server

To disable the language server of this extension, you can add `disable = true` to your asm-lsp config

`.asm-lsp.toml`:
```toml
disable = true # make sure this isn't under any [header]

# other options...
```

### Note for Windows Users

As a 2025-06-12, there is no prebuild binaries for Windows, so you will need to get `asm-lsp` and add it to `$PATH` yourself.
