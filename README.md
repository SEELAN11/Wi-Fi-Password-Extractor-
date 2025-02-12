# Wi-Fi-Password-Extractor-

## Description
This Python script retrieves saved WiFi profiles and their passwords on a Windows machine using the `netsh` command-line tool. It lists all WiFi networks stored on the system and attempts to extract their passwords if available.

## How It Works
1. The script uses the `subprocess` module to run `netsh wlan show profiles` and extracts the WiFi network names (SSIDs).
2. For each SSID, it runs `netsh wlan show profile <SSID> key=clear` to retrieve the stored password.
3. Extracted WiFi names and passwords are displayed in a formatted table.
4. If a password is not found, it prints an empty string.
5. If the script encounters an encoding error, it prints `ENCODING ERROR`.

## Requirements
- Windows operating system (since `netsh` is a Windows command-line tool)
- Python 3 installed

## Usage
1. Open a command prompt or terminal.
2. Run the script using:
   ```sh
   python script.py
   ```
3. The output will display saved WiFi profiles along with their passwords (if available).

## Example Output
```
Network_1                     |  password123
Network_2                     |  mysecurepass
Network_3                     |  
```

## Disclaimer
This script should only be used for educational and ethical purposes. Retrieving stored WiFi passwords without permission may violate privacy laws and terms of service agreements. Use this tool responsibly on your own devices.

## License
This project is for educational use only. Unauthorized usage is strictly prohibited.

