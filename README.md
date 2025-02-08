# JinaFetch

A CLI tool to fetch web content and save it as Markdown using [Jina Reader API](https://github.com/jina-ai/reader).

## Features

- 🚀 Fast web content conversion to Markdown
- 🔑 Secure API key management via `.env`
- 🎨 Rich terminal output with success/error formatting
- 📂 Automatic filename generation with fallback

## Installation

```bash
pipx install jinafetch  # Recommended
# or
pip install jinafetch
```

## Usage

### Configure API Key
```bash
jinafetch configure  # Update stored API key
jinafetch show-config  # See where credentials are stored
```

### Basic fetching
```bash
jinafetch fetch https://example.com
```

### Specify output file
```bash
jinafetch fetch https://example.com --output my_document.md
```

### Environment Configuration

The CLI will guide you through first-time setup:
1. Run any command (e.g. `jinafetch fetch https://example.com`)
2. You'll be prompted to enter your Jina API key
3. Your key will be securely stored in:
   - Linux: `~/.config/jinafetch/config.ini`
   - macOS: `~/Library/Application Support/jinafetch/config.ini`
   - Windows: `C:\Users\<user>\AppData\Local\jinafetch\config.ini`

For CI/CD use cases, you can still set via environment variable:
```bash
export JINA_API_KEY=your_key_here
# or
JINA_API_KEY=your_key_here jinafetch fetch...
```

## Error Handling
Common error scenarios include:
- 🔒 Missing API key
- 🌐 Network errors
- 💾 File write permissions
- 🔗 Invalid URLs

Errors display clear messages in red with details.

## Requirements
- Python 3.12+
- Valid Jina Reader API key

---

📝 Note: Requires valid authentication via Jina Reader API

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
