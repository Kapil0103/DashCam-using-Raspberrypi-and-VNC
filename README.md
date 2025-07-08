Remote-View Dashcam using Raspberry Pi and VNC
This project implements a dashcam with remote viewing capability, built using a Raspberry Pi and a camera module.
It streams live video and lets you view and control the dashcam remotely over a network using VNC (Virtual Network Computing).

🚗 Features
✅ Records live video from the Raspberry Pi camera module
✅ Remote viewing & control via VNC from a smartphone, tablet, or PC
✅ Can save footage locally on SD card or external storage
✅ Compact and cost-effective dashcam solution

🧰 Hardware Requirements
Raspberry Pi (Zero W, 3, 4, etc.)

Raspberry Pi Camera Module (or compatible USB webcam)

MicroSD card with Raspberry Pi OS

Power supply for Raspberry Pi

Optional: LCD display for local preview

🔧 Software Requirements
Raspberry Pi OS (Lite or Desktop)

VNC Server (RealVNC, built into Raspberry Pi OS)

VNC Viewer (on your phone, tablet, or PC)

Optional: fswebcam, raspivid, or motion for recording & streaming

🚀 Setup Instructions
1️⃣ Install Raspberry Pi OS
Flash Raspberry Pi OS onto the SD card using Raspberry Pi Imager.

Boot up the Raspberry Pi and complete the initial setup.

2️⃣ Enable Camera & VNC
Run sudo raspi-config.

Enable the camera interface under Interfacing Options.

Enable VNC under Interfacing Options.

Reboot the Pi.

3️⃣ Connect to Wi-Fi & Find IP Address
Connect the Pi to your Wi-Fi.

Run hostname -I to get the IP address.

4️⃣ Install Optional Tools
bash
Copy
Edit
sudo apt update
sudo apt install fswebcam motion
5️⃣ Start VNC Server
VNC server runs automatically after enabling it.

Download VNC Viewer on your client device and connect using the Pi’s IP.

6️⃣ (Optional) Record Video
Use raspivid or fswebcam to record video or take snapshots:

bash
Copy
Edit
raspivid -o video.h264 -t 60000
📁 Folder Structure (suggested)
bash
Copy
Edit
/dashcam-project/
│
├── scripts/
│   ├── start_camera.sh
│   ├── record_video.sh
│
├── README.md
📷 Sample Commands
Take a photo:

bash
Copy
Edit
raspistill -o image.jpg
Record a video (1 minute):

bash
Copy
Edit
raspivid -o video.h264 -t 60000
🌐 Remote Access
Install VNC Viewer on your remote device.

Enter the Pi’s IP and login credentials.

View and control the Raspberry Pi & camera remotely!

🙌 Contributions
Feel free to open issues or submit pull requests to enhance this project!
