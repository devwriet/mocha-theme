# Mocha Setup

A lightweight, dark-mode-only Vencord theme with Catppuccin Mocha colors, A2Z typography, and geometric chat backgrounds.

## Install

1. Download `theme.css` and optionally `snippets/shapes.css` into Vencord's themes folder (Vencord Settings > Themes > Open Themes Folder), then enable them in the Themes tab.
2. Or add `https://raw.githubusercontent.com/devwriet/mocha-setup/main/theme.css` and optionally `https://raw.githubusercontent.com/devwriet/mocha-setup/main/snippets/shapes.css` in the Online Themes tab.

## Snippets

- `shapes.css`: full geometric background. Requires `theme.css` enabled. Disable it to restore the sparse default.
- `plain-names.css`: shows every display name in the theme font instead of its display name style font. Name colors and gradients stay. Requires `theme.css` enabled.

## Performance notes

The theme avoids a base-theme `@import`, `backdrop-filter`, blur, and message-list animations. It loads only three WOFF2 font weights from jsDelivr and uses static inline SVG shapes. These choices remove theme-side costs that made the previous theme slow. Discord's CSS variables can change without notice, so an update can break parts of the theme.

## Notes

The theme slims the top title bar and hides back/forward buttons, the title, Inbox, and Help. On macOS it places the Vencord Toolbox, DevTools, and update icons at the right end of the chat header; on Windows and Linux it leaves that group in the top bar to keep native window controls in place.
The typing indicator uses custom text set by the `--mocha-typing-*` tokens in `theme.css`.
The loading screen cycles custom quotes; edit the first quote in the base `content` declaration in `theme.css`. CSS cannot randomize, so each load starts on the first quote.

## Credits

- Catppuccin palette, MIT: https://github.com/catppuccin/catppuccin
- A2Z font (에이투지체) by Freesentation, SIL Open Font License 1.1; loaded from the noonnu jsDelivr mirror (projectnoonnu), not bundled in this repository.

## License

Theme code is MIT licensed; see [LICENSE](LICENSE).
