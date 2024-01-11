# Alacritty Theme Switcher

This simple Bash script allows you to easily switch themes in the Alacritty terminal emulator by updating the configuration file.

## Prerequisites

Have installed: 
- Alacritty
- Fish (for autocompletion)

Your Alacritty configuration file exists at `~/.config/alacritty/alacritty.toml`.

## Installation

Mark `alacritty-switch-theme` as executable with `chmod +x alacritty-switch-theme` then add it to path. 
Move `alacritty-switch-theme.fish` to `~/.config/fish/completions`

## Usage

```bash
./theme-switcher.sh <theme_path>
```

- `<theme_path>`: The path to the new theme file in TOML format.

If no `<theme_path>` is provided, the script will display the currently applied theme.

## Example

To apply a new theme, run:

```bash
./theme-switcher.sh /path/to/new/theme.toml
```

## Autocomplete

For improved usability, the script supports autocomplete for theme paths. Simply press the Tab key after entering the initial characters of the theme path to autocomplete. 

Autocomplete will show all files in `~/.config/alacritty/themes`.

**NOTE: ** Autocomplete requires a fish shell to work. 

## Important Notes

- The script checks if the Alacritty configuration file exists. If not, it will display an error message and exit.
- It validates whether the specified theme file exists and has a ".toml" extension before making any changes.
- The script replaces the existing theme path in the Alacritty configuration file with the new theme path.

Feel free to customize the script according to your needs or integrate it into your workflow for efficient theme switching in Alacritty.
