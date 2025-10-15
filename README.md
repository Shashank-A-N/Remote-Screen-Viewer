# 🖥️ Remote Screen Viewer & Controller

This project enables **real-time screen sharing and remote control** from one device to another — directly in the web browser — using a secure peer-to-peer connection.

---

## 🌟 Features

- **Real-time Screen Sharing:** View the screen of a host device (like a phone) from a controller device (like a desktop or another phone).  
- **Remote Click Interaction:** Send click commands from the controller to the host device.  
- **Easy QR Code Connection:** Simplifies the connection process by scanning QR codes.  
- **Web-Based:** No native app installation required — runs entirely in modern web browsers.  
- **Secure P2P Connection:** Utilizes WebRTC (via **PeerJS**) for a direct and secure connection between devices — your screen data never passes through a central server.

---

## 🤔 How It Works

The system consists of two parts:

- **Host:** The device whose screen you want to share and control (runs the host page).  
- **Controller:** The device you use to view and interact with the host’s screen (runs the controller page).

The connection is established using **PeerJS**, which facilitates a direct **WebRTC** data and media connection between browsers.  
The **Controller** generates a unique ID, displays it as a QR code, and the **Host** scans it to initiate the connection.

---

## 🚀 How to Use

### 1. Open the Controller Page
Open the `just.html` file in your browser on the device you want to **control from**.

### 2. Set Up the Host
You will be greeted with a splash screen.  
Use your other device (the one you want to control) to scan the QR code or manually open this URL:  
🔗 **[https://shashank-a-n.github.io/Scan-Phone/](https://shashank-a-n.github.io/Scan-Phone/)**

### 3. Proceed to Controller
Click the **"Continue to Controller"** button on the controller page.

### 4. Connect the Devices
- The controller page will now display a new QR code under **"Scan to Auto-Connect"**.  
- On the host device, use its interface to scan this QR code.

### 5. Start Sharing
- Once connected, the controller status turns green and says **"Connected"**.  
- The host device will prompt to **grant screen sharing permissions**.  
- After permission is granted, the host’s screen will appear on the controller’s virtual display.

### 6. Remote Control
Click anywhere on the video stream within the controller’s phone display to send a **click event** to that corresponding location on the host’s screen.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|-------------|----------|
| **HTML, CSS, JavaScript** | Core web app foundation |
| **Tailwind CSS** | Rapid UI development |
| **PeerJS** | Simplified WebRTC peer-to-peer connection |
| **QRCode.js** | Dynamic QR code generation in browser |

---

## 📂 Project Structure
📦 Remote-Screen-Viewer
├── index.html # Controller/landing page
├── host.html # Host screen-sharing page
├── just.html # Controller setup page
├── script.js # PeerJS + QR handling
├── style.css # Custom styles
└── README.md # Project documentation
