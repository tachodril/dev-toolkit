# Dev Toolkit

A single-file, browser-based collection of developer tools. No build step, no backend, no sign-up — just open `index.html` and get to work.

**[Live Demo](https://tachodril.github.io/dev-toolkit/)**

---

## Tools

### ID Formatter
Format raw IDs/values into any output format with processing options.

- **9 output formats**: SQL IN (string/numeric), CSV, comma-separated, JSON array, Python list, Markdown list, one-per-line, custom template
- Remove duplicates, sort (A-Z, Z-A, numeric), case conversion
- Prefix/suffix per item, regex filter, find & replace
- Chunk/batch size for SQL 1000-item limits
- Column name input for full `WHERE col IN (...)` generation
- Smart input parser — auto-detects JSON arrays, SQL IN clauses, CSV, tab-separated, mixed quotes
- Live preview, drag & drop file import, export to file
- URL state — settings encoded in query string for bookmarking/sharing

### JSON Validator & Formatter
Validate, format, and explore JSON data.

- Real-time validation with detailed error messages
- Syntax-highlighted formatted output
- Minified output (single line)
- Interactive collapsible tree view
- Click any key in tree to copy its JSON path
- Configurable indent (2 spaces, 4 spaces, tab)
- Sort keys alphabetically (recursive)
- Auto-fix common issues: trailing commas, single quotes, unquoted keys, JS comments
- Export as `.json`

### Markdown Preview
Live markdown editor with full GFM support.

- Real-time preview as you type
- GitHub Flavored Markdown: tables, task lists, strikethrough
- Syntax-highlighted code blocks (all languages via highlight.js)
- Mermaid diagram rendering (flowcharts, sequence diagrams, etc.)
- Auto-generated table of contents
- Copy code buttons on every code block
- Write mode (type markdown) or Upload mode (drag & drop `.md` files)
- Export as self-contained HTML file
- Word/line/character count

### Epoch Converter
Convert between Unix timestamps and human-readable dates.

- Live ticking clock showing current Unix timestamp
- **Epoch to Human**: auto-detects seconds/milliseconds/microseconds/nanoseconds
- **Human to Epoch**: native date picker + free-text parsing (`Jan 15 2024`, ISO 8601, etc.)
- Relative time display ("3 months, 12 days ago")
- Quick buttons: Now, +1 hour, +1 day, Y2K38, Today midnight, +1 week/month/year
- Every result row has a copy button
- **Batch convert**: paste many timestamps or dates, convert all at once

### Base64 / URL / HTML Encode-Decode
Encode and decode text in multiple formats.

- **3 modes**: Base64, URL encoding, HTML entities
- Encode or Decode direction toggle
- Live processing as you type
- Swap input/output (auto-flips direction)
- Byte and character counts
- Full UTF-8 support

### Regex Tester
Test regular expressions with live feedback.

- Live match highlighting directly on the test string
- Flag toggles: `g` (global), `i` (case insensitive), `m` (multiline), `s` (dotall)
- Match list with index positions and capture groups (`$1`, `$2`, ...)
- Replace mode with group references and live preview
- **Pattern library**: 16 common patterns (email, URL, UUID, IPv4, hex color, phone, HTML tag, etc.)
- Error display for invalid patterns
- Copy all matches or replaced result

### JWT Decoder
Decode and inspect JSON Web Tokens.

- Auto-decode on paste — splits header, payload, signature
- Color-coded raw token (blue header / purple payload / green signature)
- Syntax-highlighted decoded header and payload
- Claims table with human-readable labels (Issuer, Subject, Audience, etc.)
- Timestamp claims (`exp`, `iat`, `nbf`) auto-converted to dates
- Expiry badge: green "Valid" or red "Expired"
- Copy individual parts or full payload
- Sample JWT generator for testing

### Diff Viewer
Compare two text blocks with a proper diff algorithm.

- LCS-based (Longest Common Subsequence) line diff
- Color-coded output: green additions, red deletions, grey unchanged
- Dual line numbers (original + modified)
- Options: ignore whitespace, ignore case, trim lines
- Stats: lines added, removed, unchanged
- Swap A/B button

### Compare Lists
Set operations on two lists of values.

- Intersection (A ∩ B)
- Only in A
- Only in B
- Union (A ∪ B)
- Count badges on each result
- Copy any result set

---

## Features

- **Single HTML file** — no build tools, no `npm install`, no framework
- **Dark / Light theme** — auto-detects system preference, toggle with button or `Ctrl+D`
- **Keyboard shortcuts** — `Ctrl+Enter` format, `Ctrl+Shift+C` copy output, `Ctrl+D` dark mode
- **Responsive** — works on desktop and mobile
- **Toast notifications** — non-intrusive feedback
- **Drag & drop** — drop files onto input areas
- **URL state** — formatter settings saved in URL for sharing

## Dependencies

The core toolkit is **zero-dependency**. The Markdown tab loads 3 libraries from CDN:

- [marked](https://github.com/markedjs/marked) — Markdown parser
- [highlight.js](https://github.com/highlightjs/highlight.js) — Syntax highlighting
- [mermaid](https://github.com/mermaid-js/mermaid) — Diagram rendering

Everything else is vanilla HTML, CSS, and JavaScript.

## Usage

```bash
# Clone and open
git clone https://github.com/tachodril/dev-toolkit.git
open dev-toolkit/index.html

# Or just download index.html and double-click it
```

No server required. Works offline (except Markdown tab CDN libs on first load).

## Contributing

Contributions are welcome. Since this is a single-file project, keep these in mind:

- Everything stays in `index.html` — no splitting into multiple files
- No build tools or transpilation
- No external dependencies for core tools (CDN libs only for Markdown)
- Test in both light and dark mode
- Test on mobile viewport

## License

MIT
