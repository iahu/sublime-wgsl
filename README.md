# WGSL Enhance

Enhanced WGSL support for Sublime Text with syntax highlighting and snippets.

## Features

- Full WGSL syntax highlighting support
- Snippets for common WGSL patterns
- Support for tagged template literals in JavaScript/TypeScript
- Integration with wgsl-analyzer for LSP support

## Installation

### Via Package Control

1. Open Sublime Text
2. Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows/Linux)
3. Type "Package Control: Install Package"
4. Search for "WGSL" and install

### Manual Installation

1. Download a zip file and unzip it, or clone this repo from github
2. Put the folder under Sublime Text Packages directory:
   - Mac: `~/Library/Application Support/Sublime Text/Packages/`
   - Windows: `%APPDATA%\Sublime Text\Packages\`
   - Linux: `~/.config/sublime-text/Packages/`

## Usage

### Tagged Template Highlight

```js
var code = `//wgsl
  @fragment
  fn fs() -> @location(0) vec4f {
    return vec4f(1.0, 0.0, 0.0, 1.0);
  }
`;
```

### LSP Integration

1. Install [wgsl-analyzer](https://github.com/wgsl-analyzer/wgsl-analyzer)
2. Open Preferences > Package Settings > LSP > Settings and add the "wgsl-ls" client configuration to the "clients":

```jsonc
{
  "clients": {
    "wgsl-lsp": {
      "enabled": true,
      "command": ["wgsl_analyzer"],
      "selector": "source.wgsl"
    }
  }
}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License
