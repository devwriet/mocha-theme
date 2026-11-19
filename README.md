# Mocha Setup

Lightweight dark Vencord theme. Catppuccin Mocha colors, A2Z font, geometric background.

## Install

Copy `theme.css` into Vencord's themes folder (Settings > Themes > Open Themes Folder) and enable it.

Or add this URL under Online Themes:

```
https://raw.githubusercontent.com/devwriet/mocha-theme/main/theme.css
```

## Snippets

Optional. Need `theme.css` enabled.

- `snippets/shapes.css`: more background shapes.
- `snippets/plain-names.css`: display names use the theme font.

## Customize

- Typing text: `--mocha-typing-*` tokens in `theme.css`.
- Loading quotes: the `mocha-quotes` keyframes in `theme.css`. First quote is the base `content` above them.

## Notes

- Dark mode only.
- Hides back/forward, title, Inbox, and Help in the top bar. On macOS the Vencord Toolbox, DevTools, and update icons move to the chat header.
- Discord updates can break selectors.

## Credits

- [Catppuccin](https://github.com/catppuccin/catppuccin) palette (MIT)
- A2Z (에이투지체) by Freesentation (OFL 1.1). `fonts/` holds copies with the empty Hangul entries removed, so missing syllables fall back instead of showing blank. License in `fonts/OFL.txt`.
- [Pretendard](https://github.com/orioncactus/pretendard) (OFL 1.1), fallback for Hangul that A2Z lacks

## License

MIT. See [LICENSE](LICENSE).
