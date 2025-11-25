   ____ _           _    _                    _ 
  / ___| |__   __ _| | _| |    ___   __ _  __| |
 | |   | '_ \ / _` | |/ / |   / _ \ / _` |/ _` |
 | |___| | | | (_| |   <| |__| (_) | (_| | (_| |
  \____|_| |_|\__,_|_|\_\_____\___/ \__,_|\__,_|

                                                

Comprehensive CLI tool for load testing web applications and Telegram bots with support for multiple frameworks (Locust, K6, Artillery, JMeter).

## Features

- Interactive terminal interface with color themes
- Multiple load testing frameworks support
- Built-in templates for common test scenarios
- Real-time progress tracking
- Detailed metrics and reporting
- Command-based operation with `/` commands

## Installation

```bash
pip install chakload-cli
```

Or using pipx:

```bash
pipx install chakload-cli
```

After installation, run the tool using:

```bash
chakload
```

### External Dependencies

Some advanced frameworks require separate installation:

**K6**:
- Download from https://github.com/grafana/k6/releases
- Or use Chocolatey: `choco install k6`
- Or use Scoop: `scoop install k6`

**Locust**:
- Install via pip: `pip install locust`

**JMeter**:
- Download from https://jmeter.apache.org/download_jmeter.cgi

**Artillery**:
- Install via npm: `npm install -g artillery`

The built-in frameworks (simple, advanced) are included by default and require no additional installation.

## Quick Start

Run the interactive CLI:

```bash
chakload
```

In the interactive mode, you can use commands like:

- `/framework locust` - Select Locust as the testing framework
- `/type web-site` - Select the type of test
- `/url https://example.com` - Set the target URL
- `/users 100` - Set the number of concurrent users
- `/run` - Start the load test

## Command Reference

- `/help` - Show available commands
- `/framework <name>` - Select framework (locust, k6, artillery, jmeter)
- `/type <test-type>` - Select test type (web-site, telegram-webhook, api-endpoint)
- `/config` - Show current configuration
- `/run` - Execute the test
- `/results` - Show test results
- `/export <format>` - Export results (json, csv, html)
- `/theme <name>` - Change color theme
- `/exit` - Exit the CLI

## Supported Test Types

- Web site testing (HTTP/HTTPS)
- Telegram bot webhook testing
- API endpoint testing
- GraphQL endpoint testing
- WebSocket connection testing

## Supported Frameworks

- Simple HTTP (Built-in, using requests library)
- More frameworks coming soon (Locust, K6, Artillery, JMeter)

## Configuration

Save and load configuration presets:

```bash
# Save current configuration
/config save my-test-config

# Load a saved configuration
/config load my-test-config
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License.