# Mocha Setup

A lightweight, dark-mode-only Vencord theme with Catppuccin Mocha colors, A2Z typography, and geometric chat backgrounds.

## Install

1. Download `theme.css` and, optionally, `snippets/shapes.css` and `snippets/plain-names.css` into Vencord's themes folder (Vencord Settings > Themes > Open Themes Folder), then enable them in the Themes tab.
2. Or add these URLs in the Online Themes tab. Only the first one is required.
   - `https://raw.githubusercontent.com/devwriet/mocha-theme/main/theme.css`
   - `https://raw.githubusercontent.com/devwriet/mocha-theme/main/snippets/shapes.css`
   - `https://raw.githubusercontent.com/devwriet/mocha-theme/main/snippets/plain-names.css`

## Snippets

- `shapes.css`: full geometric background. Requires `theme.css` enabled. Disable it to restore the sparse default.
- `plain-names.css`: shows every display name in the theme font instead of its display name style font. Name colors and gradients stay. Requires `theme.css` enabled.

## Performance notes

The theme avoids a base-theme `@import`, `backdrop-filter`, blur, and message-list animations. It loads only three WOFF2 font weights from jsDelivr and uses static inline SVG shapes. Discord's CSS variables can change without notice, so an update can break parts of the theme.

Compared with a Midnight-based theme that used animated blur, `backdrop-filter`, and about 11 MB of TTF fonts:

| | Midnight-based theme | Mocha Setup |
| --- | --- | --- |
| Frame rate while switching channels and scrolling | 23.9 fps | 49.9 fps |
| Time frozen in a 20-second run | 8.2 s | 2.3 s |
| Theme downloads | ~12.6 MB | 290 KB |

These are one run each on one Mac, so expect the exact numbers to vary.

## Notes

The theme slims the top title bar and hides back/forward buttons, the title, Inbox, and Help. On macOS it places the Vencord Toolbox, DevTools, and update icons at the right end of the chat header; on Windows and Linux it leaves that group in the top bar to keep native window controls in place.

The typing indicator uses custom text set by the `--mocha-typing-*` tokens in `theme.css`.

The loading screen cycles custom quotes. Edit the first quote in the base `content` declaration in `theme.css` and the rest in the `mocha-quotes` keyframes below it. CSS cannot randomize, so each load starts on the first quote.

## Credits

- Catppuccin palette, MIT: https://github.com/catppuccin/catppuccin
- A2Z font (에이투지체) by Freesentation, SIL Open Font License 1.1; loaded from the noonnu jsDelivr mirror (projectnoonnu), not bundled in this repository.

## License

Theme code is MIT licensed; see [LICENSE](LICENSE).
