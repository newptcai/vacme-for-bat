# vacme for bat

A simple port of the vacme color theme for [bat](https://github.com/sharkdp/bat), the modern `cat` clone with syntax highlighting.

## Files
- `vacme.tmTheme` --- TextMate theme used by bat.

## Install
You can use bat's config directory helper so this works across platforms.

```bash
# 1) Ensure the themes directory exists
mkdir -p "$(bat --config-dir)/themes"

# 2) Copy the theme into place
cp vacme.tmTheme "$(bat --config-dir)/themes/"

# 3) Rebuild bat's theme cache
bat cache --build
```

## Use
- One-off: `bat --theme=vacme path/to/file`
- Default theme via config:
  ```bash
  echo '--theme="vacme"' >> "$(bat --config-dir)/config"
  ```
- Or via env var: `export BAT_THEME=vacme`

## Update
If you change or replace the theme file, run `bat cache --build` again.

## Uninstall
```bash
rm -f "$(bat --config-dir)/themes/vacme.tmTheme"
bat cache --build
```

## History
- vacme originates as a Vim colorscheme by [overvale/vacme](https://github.com/overvale/vacme).
- It's inspired by Plan 9 and the [Acme editor](http://acme.cat-v.org), prioritizing interface colors over heavy syntax coloring.
- Acme, created at Bell Labs (by Rob Pike) for Plan 9, is known for a clean, high‑contrast aesthetic and minimal chrome; vacme channels that look and feel.

## Credits
- Original theme: https://github.com/overvale/vacme
- Port for bat: this repository

## License
See `LICENSE`.
