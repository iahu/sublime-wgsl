# sublime-wgsl

WGSL syntax highlighting and snippets for Sublime Text.

## install
Download a zip file unzip it, or clone this repo from github, then put the folder under Sublime Text Packages directory.

## tagged template highlight
```js
var code = `//wgsl
  @fragment
  fn fs() -> @location(0) vec4f {
    return vec4f(1.0, 0.0, 0.0, 1.0);
  }
`

```

## wgsl sublime-lsp client

1. install [wgsl-analyzer](https://github.com/wgsl-analyzer/wgsl-analyzer)
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
