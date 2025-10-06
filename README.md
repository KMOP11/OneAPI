# OneAPI

A Minecraft bot built with Mineflayer that automatically moves around to prevent AFK (Away From Keyboard) kicks on Minecraft servers.

## Features

- Automatic movement to prevent AFK kicks
- Random movement patterns (forward, back, left, right)
- Configurable movement intervals
- Random timing variations to appear more human-like
- Automatic item activation
- Simple configuration system

## Prerequisites

- Node.js (version 12 or higher)
- Access to a Minecraft server

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/OneAPI.git
cd OneAPI
```

2. Install dependencies:
```bash
npm install
```

3. Configure the bot by editing `config.json`:
```json
{
    "ip": "your-server-ip",
    "port": "25565",
    "name": "your-bot-username"
}
```

## Usage

1. Update the `config.json` file with your server details and bot username
2. Run the bot:
```bash
npm start
```

The bot will automatically connect to the specified server and begin moving around to prevent AFK kicks.

## Configuration

The bot can be configured by modifying the following variables in `index.js`:

- `moveinterval`: Base movement interval in seconds (default: 2)
- `maxrandom`: Maximum random seconds to add to movement interval (default: 5)

## How It Works

The bot uses the Mineflayer library to connect to Minecraft servers and:
1. Connects to the specified server
2. Waits for spawn confirmation
3. Periodically moves in random directions
4. Activates items to simulate player activity
5. Uses random timing to avoid detection

## Dependencies

- `mineflayer`: Minecraft bot library
- `config`: Configuration management
- `fs`: File system operations

## License

ISC License

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## Disclaimer

This bot is for educational purposes. Please ensure you have permission to use bots on the target server and comply with the server's terms of service.
