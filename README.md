# 🌐 Web Browser MCP Server

[![PyPI version](https://badge.fury.io/py/web-browser-mcp-server.svg)](https://badge.fury.io/py/web-browser-mcp-server)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

> 🤖 Transform your AI applications with powerful web browsing capabilities! Let your AI read and understand the web.

## ✨ Features

- 🎯 **Smart Content Extraction** - Target exactly what you need with CSS selectors
- ⚡ **Lightning Fast** - Built with async processing for optimal performance
- 📊 **Rich Metadata** - Capture titles, links, and structured content
- 🛡️ **Robust & Reliable** - Built-in error handling and timeout management
- 🌍 **Cross-Platform** - Works everywhere Python runs

## 🚀 Quick Start

### Installation

Choose your favorite package manager:

```bash
# Using pip
pip install web-browser-mcp-server

# Using uv (recommended)
uv pip install web-browser-mcp-server
```

### 🔌 Claude Desktop Integration

Add this to your Claude Desktop config to unlock web browsing superpowers:

<details>
<summary>📝 Click to view configuration</summary>

```json
{
    "mcpServers": {
        "web-browser-mcp-server": {
            "command": "uv",
            "args": [
                "--directory",
                "/path/to/web-browser-mcp-server",
                "run",
                "web-browser-mcp-server"
            ],
            "env": {
                "REQUEST_TIMEOUT": "30"
            }
        }
    }
}
```
</details>

> 💡 Replace `/path/to/web-browser-mcp-server` with your installation path

## 🎮 Usage Examples

Extract exactly what you need from any webpage:

```python
# Basic webpage fetch
result = browse_webpage(url="https://example.com")

# Target specific content with CSS selectors
result = browse_webpage(
    url="https://example.com",
    selectors={
        "headlines": "h1, h2",
        "main_content": "article.content",
        "navigation": "nav a"
    }
)
```

## ⚙️ Configuration

Customize behavior with environment variables:

| Variable | Description | Default |
|----------|-------------|---------|
| `REQUEST_TIMEOUT` | ⏱️ Max request time (seconds) | 30 |
| `USER_AGENT` | 🕵️ Custom user agent string | Modern Chrome UA |
| `LOG_LEVEL` | 📝 Logging verbosity | "info" |
| `MAX_RETRIES` | 🔄 Max retry attempts | 3 |

## 🛠️ Development

Set up your dev environment in seconds:

```bash
# Create and activate virtual environment
uv venv
source .venv/bin/activate

# Install dev dependencies
uv pip install -e ".[test]"

# Run tests
python -m pytest
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

- 🐛 Report bugs
- 💡 Suggest features
- 🔧 Submit pull requests

## 📜 License

MIT License - do what you want! See [LICENSE](LICENSE) for details.

---

<div align="center">

### 🌟 Level Up Your AI with Web Browsing Powers! 🌟

Built for the [Model Context Protocol](https://github.com/anthropics/anthropic-tools) | Made with ❤️ by the MCP Community

<details>
<summary>🎉 Star us on GitHub!</summary>
<br>
If you find this tool useful, consider giving it a star! It helps others discover the project.
</details>

</div>