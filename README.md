# JSON Utility

A simple, browser-based tool for converting and pretty-printing JSON data to multiple formats.

## Features

- **Pretty Print JSON** with customizable indentation (0-8 spaces)
- **Convert to YAML** with proper formatting
- **Convert to TOML** with nested object support
- **Real-time conversion** as you type
- **Error handling** with visual feedback
- **Responsive design** for desktop and mobile
- **Two-panel layout** with 50/50 split for easy comparison

## Usage

1. Open `index.html` in your web browser
2. Paste or type JSON data in the left panel
3. Adjust indent level (0-8 spaces) using the input field
4. Select output format from dropdown: JSON, YAML, or TOML
5. View the converted output in the right panel

## Supported Formats

### JSON
- Pretty printing with customizable indentation
- Syntax error detection and highlighting

### YAML
- Full YAML conversion using js-yaml library
- Preserves data types and structure
- Customizable indentation

### TOML
- Custom TOML converter handles:
  - Strings, numbers, booleans
  - Arrays of primitive types
  - Nested objects as TOML sections
  - Proper escaping of special characters

## Technical Details

- Pure HTML/CSS/JavaScript - no build process required
- Uses CDN for js-yaml library
- Custom TOML converter (no external dependencies)
- Responsive CSS Grid layout
- Real-time input validation and conversion

## Browser Compatibility

Works in all modern browsers that support:
- ES6 JavaScript features
- CSS Grid and Flexbox
- Local file serving or HTTP(S) protocols