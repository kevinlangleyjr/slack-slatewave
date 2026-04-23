<div align="center">

<img src="docs/logo.png" alt="Slatewave" width="840" />

# Slatewave (Slack)

A Slatewave sidebar theme for [Slack](https://slack.com) — slate foundation, teal signature. Part of the [Slatewave family](#slatewave-family) — one palette across editors, terminals, prompts, notes, and more.

> _Slate below, teal above._

</div>

---

## What it styles

Slack's "Custom theme" input accepts eight comma-separated hex colors that drive the left sidebar, channel list, presence dots, and mention badges. Slatewave maps them like this:

- ![#1E293B](https://placehold.co/16x16/1e293b/1e293b.png) **Column BG** — slate-800 `#1E293B`, matching the VSCode ANSI black and terminal sidebar tones
- ![#282C34](https://placehold.co/16x16/282c34/282c34.png) **Menu BG** — `#282C34`, the Slatewave editor background; used for the workspace-switcher and slash-menu surface
- ![#334155](https://placehold.co/16x16/334155/334155.png) **Active Item** — slate-700 `#334155`, mirroring VSCode's `list.activeSelectionBackground` for a calm, non-competing highlight
- ![#5EEAD4](https://placehold.co/16x16/5eead4/5eead4.png) **Active Item Text** — teal-300 `#5EEAD4`, the signature accent; pops the currently selected channel or DM
- ![#282C34](https://placehold.co/16x16/282c34/282c34.png) **Hover Item** — `#282C34`, one step lighter than the column for a subtle hover affordance
- ![#E2E8F0](https://placehold.co/16x16/e2e8f0/e2e8f0.png) **Text Color** — slate-200 `#E2E8F0`, matching the VSCode editor foreground
- ![#5EEAD4](https://placehold.co/16x16/5eead4/5eead4.png) **Active Presence** — teal-300 `#5EEAD4`, replacing Slack's default green to keep the palette consistent
- ![#FB7185](https://placehold.co/16x16/fb7185/fb7185.png) **Mention Badge** — rose-400 `#FB7185`, matching ANSI red across the companion themes

---

## Installation

Slack doesn't expose a theme file format — themes are pasted into Preferences as a comma-separated hex string.

### Paste the theme

1. Copy the line below (or grab it from [`slatewave.txt`](./slatewave.txt)):

   ```
   #1E293B,#282C34,#334155,#5EEAD4,#282C34,#E2E8F0,#5EEAD4,#FB7185
   ```

2. In Slack, open **Preferences → Themes**.
3. Scroll to **Colors** and click **Create a custom theme**.
4. Paste the string into the **colors** box at the bottom of the dialog (the single-line input; not the individual color pickers).
5. Slack applies the theme immediately. Close the dialog to keep it.

### Share with your workspace

Once pasted, click **Share this theme with your workspace** to post the string into any channel. Teammates can click **Switch sidebar theme** on the message to apply it in one tap.

### From a local clone

```sh
git clone https://github.com/kevinlangleyjr/slack-slatewave
pbcopy < slack-slatewave/slatewave.txt
```

Then paste into Slack's custom theme dialog as above.

---

## Palette

Slatewave shares its palette with the companion themes. The eight slots, in Slack's custom-theme order:

| # | | Slot | Hex | Tailwind | Role |
|---|---|---|---|---|---|
| 1 | ![#1E293B](https://placehold.co/20x20/1e293b/1e293b.png) | Column BG | `#1E293B` | slate-800 | sidebar background |
| 2 | ![#282C34](https://placehold.co/20x20/282c34/282c34.png) | Menu BG | `#282C34` | — | workspace menu / slash-menu surface |
| 3 | ![#334155](https://placehold.co/20x20/334155/334155.png) | Active Item | `#334155` | slate-700 | selected channel background |
| 4 | ![#5EEAD4](https://placehold.co/20x20/5eead4/5eead4.png) | Active Item Text | `#5EEAD4` | teal-300 | selected channel text (signature) |
| 5 | ![#282C34](https://placehold.co/20x20/282c34/282c34.png) | Hover Item | `#282C34` | — | hover background |
| 6 | ![#E2E8F0](https://placehold.co/20x20/e2e8f0/e2e8f0.png) | Text Color | `#E2E8F0` | slate-200 | default sidebar text |
| 7 | ![#5EEAD4](https://placehold.co/20x20/5eead4/5eead4.png) | Active Presence | `#5EEAD4` | teal-300 | online indicator dot |
| 8 | ![#FB7185](https://placehold.co/20x20/fb7185/fb7185.png) | Mention Badge | `#FB7185` | rose-400 | unread mention badge |

---

## Customize

The theme is a plain comma-separated hex string — eight colors, in the order above. To tweak a single slot without forking, edit the value in Slack's **Create a custom theme** dialog after pasting. Slack stores the theme in its local preferences, not in this file, so changes there stick per-workspace without affecting anything upstream.

To fork the string itself: edit [`slatewave.txt`](./slatewave.txt). Slack accepts upper- or lower-case hex; the leading `#` is required on each color.

### Pair with Slack's base theme

For the cleanest match, set Slack's base appearance to **Dark** (**Preferences → Themes → Dark**) before pasting the custom colors. The sidebar custom theme composes over the dark base — pasting over the light base will give you a mismatched message pane.

---

## Slatewave family

One palette. Every tool.

- **Editors** — [VSCode](https://github.com/kevinlangleyjr/vscode-slatewave) · [Neovim](https://github.com/kevinlangleyjr/neovim-slatewave) · [Helix](https://github.com/kevinlangleyjr/helix-slatewave) · [Zed](https://github.com/kevinlangleyjr/zed-slatewave) · [Sublime Text](https://github.com/kevinlangleyjr/sublime-text-slatewave) · [JetBrains](https://github.com/kevinlangleyjr/jetbrains-slatewave)
- **Terminals** — [Alacritty](https://github.com/kevinlangleyjr/alacritty-slatewave) · [Ghostty](https://github.com/kevinlangleyjr/ghostty-slatewave) · [iTerm2](https://github.com/kevinlangleyjr/iterm2-slatewave) · [WezTerm](https://github.com/kevinlangleyjr/wezterm-slatewave) · [Windows Terminal](https://github.com/kevinlangleyjr/windows-terminal-slatewave)
- **Prompts** — [Oh My Posh](https://github.com/kevinlangleyjr/slatewave-omp) · [Starship](https://github.com/kevinlangleyjr/starship-slatewave)
- **Multiplexer** — [tmux](https://github.com/kevinlangleyjr/tmux-slatewave)
- **Notes** — [Obsidian](https://github.com/kevinlangleyjr/obsidian-slatewave) · [Logseq](https://github.com/kevinlangleyjr/logseq-slatewave)
- **Launchers** — [Alfred](https://github.com/kevinlangleyjr/alfred-slatewave) · [Raycast](https://github.com/kevinlangleyjr/raycast-slatewave)

See [getslatewave.com](https://getslatewave.com) for the full family.

---

## Contributing

Issues and PRs welcome. For palette changes, include a before/after screenshot of the Slack sidebar with at least one active channel, one unread channel with a mention badge, and one DM with an online presence dot so the visual tradeoff is obvious.

---

## License

WTFPL — Do What The Fuck You Want To Public License. See [LICENSE](LICENSE).
