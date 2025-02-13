# sublime-wgsl

WGSL syntax highlighting and snippets for Sublime Text.

# wgsl sublime-lsp client

1. install [wgsl-analyzer](https://github.com/wgsl-analyzer/wgsl-analyzer)
2. Open Preferences > Package Settings > LSP > Settings and add the "wgsl-ls" client configuration to the "clients":
```json
{
    "clients": {
        "wgsl-ls": {
            "enabled": true,
            "command": [ "wgsl_analyzer" ], // the wgsl_analyzer PATH
            "selector": "source.wgsl"
        }
    }
}
```
