# WiFi Denial of Service Attack Scripts

This repository contains Python scripts designed to perform Denial of Service (DoS) attacks on WiFi networks. The scripts utilize various tools available in Kali Linux for network scanning and deauthentication attacks. **Please use these scripts responsibly and only on networks for which you have explicit permission. Misuse of these tools can lead to legal consequences.**

## Scripts Overview

### `wifi_dos.py`

This script performs a WiFi DoS attack by deauthenticating clients from a selected access point. The process involves:
1. **Scanning for Wireless Interfaces**: Identifies available WiFi interfaces on the system.
2. **Selecting an Interface**: Allows the user to choose the desired interface for the attack.
3. **Killing Conflicting Processes**: Ensures that no other processes interfere with the attack.
4. **Switching to Monitor Mode**: Configures the selected WiFi adapter to monitor mode.
5. **Discovering Access Points**: Uses `airodump-ng` to scan and list nearby access points.
6. **Attacking**: Deauthenticates clients connected to a chosen access point using `aireplay-ng`.

This script is useful for testing the resilience of a network against deauthentication attacks.

### `wifi_dos_own.py`

This script provides a basic WiFi DoS attack capability, similar to `wifi_dos3.py`, but with a slightly different approach:
1. **Scanning and Selecting Interface**: Identifies and allows the user to select a WiFi interface.
2. **Killing Conflicting Processes**: Ensures no other processes are using the WiFi adapter.
3. **Switching to Monitor Mode**: Configures the WiFi adapter for monitoring.
4. **Discovering Access Points**: Scans for nearby access points.
5. **Attacking**: Deauthenticates clients from a selected access point.

The main difference from `wifi_dos3.py` is in the implementation details and the ability to select devices to keep the Wifi running without any interference. This script is a straightforward approach for performing DoS attacks.

### `wifi_dos_type1.py`

This script is designed for a more specific use case in WiFi DoS attacks:
1. **Initial Setup**: Checks for necessary privileges and moves any existing CSV files to a backup directory.
2. **Scanning for Interfaces**: Identifies available WiFi interfaces.
3. **Selecting and Configuring Interface**: Allows interface selection and puts it into monitor mode.
4. **Access Point Discovery**: Uses `airodump-ng` to discover nearby access points and logs them.
5. **Attacking**: Deauthenticates clients from the chosen access point using `aireplay-ng`.

`wifi_dos_type1.py` offers a more detailed and user-friendly approach to executing a DoS attack, including CSV file handling and dynamic interface selection.

### `wifi_dos_type2.py`

This script performs a similar function to `wifi_dos_type1.py` but includes some additional features:
1. **Setup and Backup**: Moves existing CSV files to a backup folder before proceeding.
2. **Interface Selection**: Identifies and allows the user to choose a WiFi interface.
3. **Configuring the Interface**: Switches the selected interface to monitor mode.
4. **Access Point Discovery**: Scans for and logs nearby access points.
5. **Attacking**: Initiates a continuous deauthentication attack and provides real-time feedback.

`wifi_dos_type2.py` includes features like real-time monitoring and continuous deauthentication, making it more suitable for extended testing periods.

## Important Notice

**These scripts are intended for educational and testing purposes only. Do not use them for unauthorized attacks on networks. Always ensure you have explicit permission to test the network you are targeting. Unauthorized use of these tools is illegal and can result in severe penalties.**

**Author:** Purva Patel
