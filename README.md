# Preseaw App - Mirror Phone Screen
![Preseaw icon](/src/app_icon.png)

Preseaw is a beauty app used to mirror mobile device screen to desktop with low latency, high resolution, high FPS and support audio playback. 
It come with 2 supporting software: 
- [**Preseaw Desktop**](/Desktop/) (running on computer).
- [**Preseaw Agent**](/Agent/) (running on mobile device)  

The main protocol media for transfer media data stream is **TCP/IP**.

**Window demo screen shot**:

#### Portrait Screen
![Preseaw screen shot](/src/screenshotzero.jpg)

#### Multiple devices

![Preseaw screen shot](/src/screenshot1.jpg)

#### Big Landscape Screen

![Preseaw screen shot](/src/screenshot2.jpg)

#### Full screen

![Preseaw screen shot](/src/screenshot3.png)


## Technology 🧑‍💻
### Preseaw Desktop  
Use [ElectronJS](https://www.electronjs.org/) for building desktop application and comes with [Webpack](https://webpack.js.org/) development and [Electron-forge](https://www.electronforge.io/) for application packaging.

### Preseaw Agent
Use native Java with of support of *MediaProjection* and *MediaEncoder* for screen capture and encode **H264/AVC** stream. Preseaw Agent currently only supports Android from android version **8.0 Oreo** (API level >= 26) and only support audio playback from Android 10 (API level >= 29).

## Connection

- `Wire` Preseaw Desktop find mobile devices via **ADB** then automating install and launch Agent.

- `Wireless`Preseaw **Desktop** and **Agent** find each other via Boardcast and MDNS. While deskop work as a server for broadcast and answer MDNS query for Agent to listen and query information.  


## Ways to pair 
* #### Via USB cable - Wire
  Mobile device need to connect with computer via cable and enable USB debugging in developer settings. 

  Specific steps:
  - Connect phone to computer with a USB cable.
  - Enable developer mode on phone.
  - In develeoper mode select USB debugging click allow for the computer connected.
  - Now **Preseaw Desktop** will detect device and launch **Preseaw Agent** automatically (automatically install the agent if it is not already installed) then the connnection will be successful.
  
  The **Preseaw desktop** will leverage the full power of [ADB](https://developer.android.com/studio/command-line/adb) (Android Debug Bridge) for doing things like forwarding in localhost to do socket connect, running [TouchService](https://preseaw.app) class to do on-screen touches, and poweroff screen, etc ...  

  **Advantage**: use this connection type for video transmission     with high quality and low latency. Always encourage users to use the way to connect.  

  **Disadvantage**: having to connect via wires is inconvenient for moving as well as the range of mobile device.
* #### Via Wi-fi or mobile Hotspot - Wireless
  Both computer and mobile device need to be connected to the same Wi-Fi or Mobile device generate mobile hotspot for desktop as well. Users need to run **Preseaw Desktop** on computer and **Preseaw Agent** on mobile device simultaneously. **Preseaw Agent** will detect the computer automatically or scan with a manual QR code. 

  Specific steps:
    - Connect both computer and mobile device to same Wi-fi network.
    - Launch **Preseaw Desktop** on computer and launch  **Preseaw Agent**  on mobile device simultaneously.
    - Select computer in **Preseaw Agent** to connect and allow share screen permission.
    - The connection successfully and user need to allow more permission like accessibility for other features.  
   This type of connection gives flexibility for mobile mobility but lacks the power of ADB.

   **Advantage**: easy connection without wires and no need to enable USB debugging.

   **Disadvantage**: slow connection speed depends on the quality of the Wi-fi network, low video quality and high latency, lack of cool features that ADB had offered.


## Features 🔧
- Live stream mobile screen to computer real time with low lantency.
- Audio playback with low latency, high quality.
- Video support with quality types `480p(SD)`, `720p(HD)`, `1080p(FULL HD)`, `1440p(2K)`.
- Operation while the screen is off helps save battery life (only supported when connecting is usb cable).
- Record screen with selected video quality with **unlimited** duration.
- Quick screenshot and save type is PNG.
- Support input keyboard from computer to mobile device with both wire and wireless connection modes.
- Fingers simulation - **Gameboard Mode** aids in playing 3rd person games and more (only supported when connecting is usb cable).
- Touch operation controls the screen real time.
- Cinema full screen mode with ambient effect.
- Paint on screen with varieties of tool, shape support by excalidraw.
- Mirror multiple devices to up to **4 devices** simultaneously.
## Future features

- Add more fancy themes.
- Support quick drop transfer files

## Offical Site

👉 [Preseaw App](https://www.preseaw.app)

## Authors
🙋‍♂️ Nguyen Ba Cu  
💁 Follow me on [𝕏/twitter](https://x.com/NgCuHs3)

