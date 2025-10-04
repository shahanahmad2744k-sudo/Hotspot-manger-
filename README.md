# Hotspot Manager Android App

An Android application that monitors and manages devices connected to your phone's mobile hotspot.

## Features

- **Connected Devices List**: Displays all active hotspot connections with device name, IP address, and MAC address
- **Device Blocking**: Block or disconnect any connected device directly from the app
- **Auto-Refresh**: Continuously updates the list every 5 seconds as devices connect/disconnect
- **Clean UI**: Simple, user-friendly interface optimized for Android 10+

## Requirements

- Android 10 (API level 29) or higher
- Root access required for device blocking functionality
- Location permission for WiFi scanning

## Permissions

The app requests the following permissions:
- `ACCESS_WIFI_STATE` - To access WiFi information
- `CHANGE_WIFI_STATE` - To modify WiFi settings
- `ACCESS_NETWORK_STATE` - To access network information
- `ACCESS_FINE_LOCATION` - Required for WiFi scanning on Android 10+
- `WRITE_SETTINGS` - To modify system settings

## Installation

1. Open the project in Android Studio
2. Build and run on your Android device
3. Grant all requested permissions
4. For device blocking functionality, root access is required

## Usage

1. Enable mobile hotspot on your device
2. Open the Hotspot Manager app
3. View all connected devices in the list
4. Tap "Block Device" to disconnect a specific device
5. Use the refresh button or wait for auto-refresh to update the list

## Technical Implementation

- Built with Kotlin and Android SDK
- Uses ARP table parsing to detect connected devices
- Implements iptables commands for device blocking (requires root)
- RecyclerView for efficient device list display
- Auto-refresh mechanism with Handler and Runnable

## Note

Device blocking functionality requires root access. Without root, the app will display connected devices but cannot block them.