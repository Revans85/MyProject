# SCSS Project Setup

## Overview
This project uses SCSS (Sass) for styling. The SCSS files are compiled to CSS for use in the HTML pages.

## Project Structure

```
styles/
├── main.scss           # Main SCSS file (imports all partials)
├── main.css            # Compiled CSS (generated from main.scss)
├── _colors.scss        # Color variables partial
├── mystyles.css        # Legacy CSS file (can be removed)
└── vendor/
    └── _normalize.scss # CSS reset/normalize partial
```

## Color Variables

The project uses the following SCSS color variables defined in `_colors.scss`:

- `$primary-font-color: #575757` - Primary text color
- `$secondary-font-color: #DB8D33` - Secondary text color (accent)
- `$dark-background: #414141` - Dark background color
- `$darker-background: #150300` - Darker background color

## Building the Project

### Option 1: Using npm and Sass

1. Install dependencies:
   ```bash
   npm install
   ```

2. Compile SCSS to CSS:
   ```bash
   npm run sass
   ```

3. Watch for changes and automatically compile:
   ```bash
   npm run sass:watch
   ```

### Option 2: Using VS Code Extensions

Install the "Live Sass Compiler" extension in VS Code:
- Search for "Live Sass Compiler" in VS Code extensions
- Click "World Sass" button in the bottom status bar to start watching
- CSS files are auto-generated when you save SCSS files

## Usage

The HTML files are configured to use `styles/main.css`. When you modify the SCSS files, recompile them to update the styles.

To use the color variables in your SCSS files:
```scss
.my-element {
  color: $primary-font-color;
  background-color: $dark-background;
}
```

## Notes

- Do not edit `main.css` directly - it is generated from `main.scss`
- Always modify the SCSS files and recompile
- The `_normalize.scss` provides CSS reset/normalization for cross-browser consistency
- The `_colors.scss` file is for color variable definitions
