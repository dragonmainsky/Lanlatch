# Lanlatch

**Lanlatch** is a tool that scans your local network (LAN) for routers, displays them in an easy-to-read table, and lets you open each one's login page directly. It can also remember the configuration details and passwords **you enter yourself** for convenient access later.

> ⚠️ Lanlatch is **not a hacking tool**. It has no password guessing, brute-force, or intrusion features of any kind. The program only discovers devices on the network you're connected to and securely stores the credentials you provide yourself.

## Features

- 🔍 Scans all devices on your LAN and identifies which ones are likely routers/access points
- 📋 Displays results in a table: name, IP, MAC, vendor, status
- 🌐 Click an IP to open that router's login page directly in your browser
- 🔐 Save each router's username/password (entered by you) encrypted with a Master Password
- 🗂️ Group or nickname your routers for easy reference when managing multiple sites

## Project Status

🚧 Early development — structure and features may change.

## Installation

```bash
git clone https://github.com/<your-username>/lanlatch.git
cd lanlatch
pip install -r requirements.txt
```

## Usage

```bash
python main.py
```

1. Set a Master Password on first run (used to encrypt saved data)
2. Click **Scan** to discover routers on your LAN
3. Click a router's IP to open its login page
4. Enter your own username/password in the app to save it for next time

## Tech Stack

- Python 3
- `socket` / `psutil` — network device discovery
- `requests` — inspecting device web pages
- `sqlite3` — data storage
- `cryptography` — encrypting saved passwords
- Tkinter — desktop UI

## Data Security

- All passwords are encrypted before being written to disk — nothing is stored as plain text
- The Master Password never leaves your machine
- The app only operates on your local network (LAN); no data is sent to the internet

## Caution

- Only use this tool on networks you own or have permission to manage
- Scan results may not be 100% complete, depending on each network's firewall/AP isolation settings

## License

This project is released under the [MIT License](LICENSE)

## Contributing

Pull requests and issues are welcome — feel free to open an issue if you find a bug or have a feature idea.
