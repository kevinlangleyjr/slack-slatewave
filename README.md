<div align="center">

# Slatewave (Slack)

A Slatewave sidebar theme for [Slack](https://slack.com) — slate foundation, teal signature. Designed as a twin to the [Slatewave VSCode theme](https://github.com/kevinlangleyjr/vscode-slatewave), [Ghostty theme](https://github.com/kevinlangleyjr/ghostty-slatewave), [iTerm2 preset](https://github.com/kevinlangleyjr/iterm2-slatewave), [Obsidian theme](https://github.com/kevinlangleyjr/obsidian-slatewave), [Logseq theme](https://github.com/kevinlangleyjr/logseq-slatewave), and [oh-my-posh prompt](https://github.com/kevinlangleyjr/slatewave-omp) — editor, terminal, notes, and chat share a single color vocabulary.

> _Slate below, teal above._

</div>

---

## What it styles

Slack's "Custom theme" input accepts eight comma-separated hex colors that drive the left sidebar, channel list, presence dots, and mention badges. Slatewave maps them like this:

- **Column BG** — slate-800 `#1E293B`, matching the VSCode ANSI black and terminal sidebar tones
- **Menu BG** — `#282C34`, the Slatewave editor background; used for the workspace-switcher and slash-menu surface
- **Active Item** — slate-700 `#334155`, mirroring VSCode's `list.activeSelectionBackground` for a calm, non-competing highlight
- **Active Item Text** — teal-300 `#5EEAD4`, the signature accent; pops the currently selected channel or DM
- **Hover Item** — `#282C34`, one step lighter than the column for a subtle hover affordance
- **Text Color** — slate-200 `#E2E8F0`, matching the VSCode editor foreground
- **Active Presence** — teal-300 `#5EEAD4`, replacing Slack's default green to keep the palette consistent
- **Mention Badge** — rose-400 `#FB7185`, matching ANSI red across the companion themes

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

| # | Slot | Hex | Tailwind | Role |
|---|---|---|---|---|
| 1 | Column BG | `#1E293B` | slate-800 | sidebar background |
| 2 | Menu BG | `#282C34` | — | workspace menu / slash-menu surface |
| 3 | Active Item | `#334155` | slate-700 | selected channel background |
| 4 | Active Item Text | `#5EEAD4` | teal-300 | selected channel text (signature) |
| 5 | Hover Item | `#282C34` | — | hover background |
| 6 | Text Color | `#E2E8F0` | slate-200 | default sidebar text |
| 7 | Active Presence | `#5EEAD4` | teal-300 | online indicator dot |
| 8 | Mention Badge | `#FB7185` | rose-400 | unread mention badge |

### Visual anchors

| | Hex | Tailwind | Role |
|---|---|---|---|
| ![#1E293B](https://placehold.co/20x20/1e293b/1e293b.png) | `#1E293B` | slate-800 | column background |
| ![#282C34](https://placehold.co/20x20/282c34/282c34.png) | `#282C34` | — | menu / hover surface |
| ![#334155](https://placehold.co/20x20/334155/334155.png) | `#334155` | slate-700 | active item |
| ![#E2E8F0](https://placehold.co/20x20/e2e8f0/e2e8f0.png) | `#E2E8F0` | slate-200 | text |
| ![#5EEAD4](https://placehold.co/20x20/5eead4/5eead4.png) | `#5EEAD4` | teal-300 | active text / presence |
| ![#FB7185](https://placehold.co/20x20/fb7185/fb7185.png) | `#FB7185` | rose-400 | mention badge |

---

## Customize

The theme is a plain comma-separated hex string — eight colors, in the order above. To tweak a single slot without forking, edit the value in Slack's **Create a custom theme** dialog after pasting. Slack stores the theme in its local preferences, not in this file, so changes there stick per-workspace without affecting anything upstream.

To fork the string itself: edit [`slatewave.txt`](./slatewave.txt). Slack accepts upper- or lower-case hex; the leading `#` is required on each color.

### Pair with Slack's base theme

For the cleanest match, set Slack's base appearance to **Dark** (**Preferences → Themes → Dark**) before pasting the custom colors. The sidebar custom theme composes over the dark base — pasting over the light base will give you a mismatched message pane.

---

## Companion themes

Slatewave is one palette, many surfaces. Run them together and your editor, terminal, prompt, notes, and chat all speak the same visual language.

- **Editor** — [vscode-slatewave](https://github.com/kevinlangleyjr/vscode-slatewave)
- **Prompt** — [slatewave-omp](https://github.com/kevinlangleyjr/slatewave-omp)
- **Notes (Obsidian)** — [obsidian-slatewave](https://github.com/kevinlangleyjr/obsidian-slatewave)
- **Notes (Logseq)** — [logseq-slatewave](https://github.com/kevinlangleyjr/logseq-slatewave)
- **Terminal (iTerm2)** — [iterm2-slatewave](https://github.com/kevinlangleyjr/iterm2-slatewave)
- **Terminal (Ghostty)** — [ghostty-slatewave](https://github.com/kevinlangleyjr/ghostty-slatewave)
- **Chat (Slack)** — this repo

---

## Contributing

Issues and PRs welcome. For palette changes, include a before/after screenshot of the Slack sidebar with at least one active channel, one unread channel with a mention badge, and one DM with an online presence dot so the visual tradeoff is obvious.

---

## License

WTFPL — Do What The Fuck You Want To Public License. See [LICENSE](LICENSE).
