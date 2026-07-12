# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a browser-based JSON utility tool that provides real-time conversion and pretty-printing of JSON data to multiple formats (JSON, YAML, TOML). The entire application is contained within a single HTML file with embedded CSS and JavaScript.

## Architecture

- **Single-file application**: Everything is contained in `index.html`
- **No build process**: Pure HTML/CSS/JavaScript that runs directly in browsers
- **External dependencies**: Only js-yaml from CDN for YAML conversion
- **Custom TOML converter**: Built-in JavaScript function handles TOML conversion without external libraries

## Development

### Running the Application
```bash
# Serve locally for testing
python3 -m http.server 8000
# Then open http://localhost:8000 in browser

# Or simply open index.html directly in any modern browser
```

### Code Structure
- **HTML**: Two-panel layout with controls (indent level, format dropdown)
- **CSS**: Responsive design with 50/50 split, mobile-friendly
- **JavaScript**: Real-time conversion logic with error handling

Key functions:
- `convertJson()`: Main conversion function handling all three formats
- `jsonToToml()`: Custom TOML converter for nested objects and arrays

### Making Changes
Since this is a single-file application, all modifications go into `index.html`. The code is organized in sections:
1. HTML structure and layout
2. Embedded CSS styles
3. External script includes (js-yaml)
4. JavaScript logic for conversion

### Testing
Test manually by:
1. Loading various JSON inputs (valid/invalid)
2. Changing indent levels (0-8)
3. Switching between output formats
4. Testing responsive design on different screen sizes
5. Verifying error handling with malformed JSON