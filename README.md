# Aurora Dracula Theme

A beautiful dark theme collection for IntelliJ IDEA, based on [Evondev Dracula](https://marketplace.visualstudio.com/items?itemName=evondev.evondev-dracula) for Visual Studio Code.

## Reference Projects

| Project | Author | Description |
|---------|--------|-------------|
| [Evondev Dracula](https://github.com/namapple/evondev-dracula) | evondev | Original VS Code theme (this project ported from) |
| [Dracula Official](https://github.com/dracula/dracula) | Zeno Rocha | Original Dracula theme that inspired all variants |

## Theme Variants

- **Evondev Dracula** — Base theme
- **Evondev Dracula Author** — Author variant
- **Evondev Dracula Darker Contrast** — Darker background, higher contrast
- **Evondev Dracula Darker Contrast New Color** — Darker variant with new color palette
- **Evondev Dracula High Contrast** — High contrast variant
- **Evondev Dracula High Contrast New Color** — High contrast with new colors
- **Evondev Dracula Night Contrast** — Night contrast variant
- **Evondev Dracula Night Contrast New Color** — Night contrast with new colors
- **Evondev Dracula New Contrast** — New contrast variant
- **Evondev Dracula Normal Contrast** — Normal contrast variant

## Building

```bash
./gradlew build
```

The plugin will be built to `build/distributions/`.

## Installation

1. Build the plugin: `./gradlew build`
2. Find the plugin JAR in `build/distributions/`
3. Install via IntelliJ IDEA: Settings → Plugins → Install Plugin from Disk...

## Technical Notes

### Java Interface Highlighting Fix

The original `JAVA_INTERFACE` attribute does not work in IntelliJ IDEA syntax highlighting. Use `DEFAULT_INTERFACE_NAME` instead. See [Java Syntax Highlighting Reference](./src/colors/Java_Syntax_Highlighting_Reference.md) for details.

### Color Scheme Format

- `.theme.json` — UI colors (backgrounds, borders, editor UI elements)
- `.xml` — Editor syntax highlighting colors (code tokens, keywords, strings)
