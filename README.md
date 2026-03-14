# 🛠️ valheim-server-docker - Easy Dedicated Server Setup

[![Download valheim-server-docker](https://img.shields.io/badge/Download-Here-green?style=for-the-badge)](https://github.com/prince30625F/valheim-server-docker)

## 📋 About valheim-server-docker

This application lets you run a Valheim dedicated game server on your Windows PC. It helps you keep your server updated automatically. It also saves backups of your game world regularly. If you like mods, you can use BepInEx and ValheimPlus mods with it. This tool is made for convenience, so you can focus on playing the game with friends.

## 💻 System Requirements

- **Operating System:** Windows 10 or higher (64-bit)
- **Processor:** Intel Core i5 or better (or equal AMD)
- **Memory:** At least 8 GB RAM
- **Disk Space:** Minimum 10 GB free space
- **Network:** A stable internet connection with open ports (usually port 2456)
- **Other:** Docker Desktop installed on Windows

## 🚀 Getting Started

To run the Valheim dedicated server, you will need Docker Desktop for Windows. Docker helps run the server inside a "container," which keeps everything organized and easy to manage.

### Step 1: Install Docker Desktop

1. Go to https://www.docker.com/products/docker-desktop and download the Docker Desktop installer.
2. Run the installer and follow the instructions.
3. After installation, open Docker Desktop and make sure it is running. You should see the Docker whale icon in your taskbar.

### Step 2: Download valheim-server-docker

Visit this page to get the software files:

[https://github.com/prince30625F/valheim-server-docker](https://github.com/prince30625F/valheim-server-docker)

Click on the green “Code” button on the right side and choose “Download ZIP.” Your browser will save a compressed folder with the software.

### Step 3: Extract Files

Find the ZIP file you downloaded and extract it to a folder on your PC. Right-click the file, then select “Extract All.” Choose where to save the extracted folder and confirm.

### Step 4: Configure Your Server

Inside the extracted folder, look for a file named `docker-compose.yml`. This file controls how the server runs.

You can change some settings here before starting:
- **World name:** Choose a name for your world.
- **Server password:** Set a password to keep your server private.
- **Mods:** The setup supports BepInEx and ValheimPlus mods. You can add or remove mods by following the instructions inside the documentation files.

If you want to keep the default settings, you can skip this step.

### Step 5: Run Your Server

1. Open the folder where you extracted the files.
2. Press and hold the Shift key, then right-click on an empty space.
3. Select “Open PowerShell window here” or “Open Command window here.”
4. In the window, type `docker-compose up -d` and press Enter.

Docker will download the necessary files and start your Valheim server. This may take a few minutes.

### Step 6: Connect to the Server

To play on your server, open Valheim on your PC.

1. Select “Start Game.”
2. Click “Join Game.”
3. Enter your server’s IP address and the password you set earlier.
4. Click “Connect.”

Your server is ready for friends to join as well. Make sure your router allows traffic on port 2456 (UDP and TCP).

## 💾 Automatic Updates and Backups

This software updates your server automatically whenever a new Valheim update comes out. It also creates backups of your world regularly. These backups save in a folder named `backups` inside your server files folder.

To change backup frequency or update settings, edit the `docker-compose.yml` file. Look for the relevant settings under the backup and update sections.

## 🧩 Mod Support

You can run mods through BepInEx and ValheimPlus. Both mods are included in the Docker image.

If you want to add or remove mods:
- Place mod files in the `mods` folder inside your extracted directory.
- Edit the configuration files for BepInEx or ValheimPlus to enable or tweak mods.

Detailed instructions for mods are inside the `docs` folder included with the download.

## 🔧 Managing the Server

Use these Docker commands in the same PowerShell or Command window opened earlier:

- **Stop the server:**  
  `docker-compose down`  
  This stops your Valheim server safely.

- **View server logs:**  
  `docker-compose logs -f`  
  This shows live server activity.

- **Restart the server:**  
  Run `docker-compose down` followed by `docker-compose up -d`.

Make sure Docker Desktop is running whenever you want your server active.

## 🔒 Network Settings and Firewall

For your server to be accessible, port 2456 needs to be open:

- Open Windows Defender Firewall from the Control Panel.
- Click “Advanced settings.”
- Create new inbound and outbound rules for TCP and UDP on port 2456.
- Also, if you use a router, forward port 2456 to your PC’s local IP.

This allows other players to connect without issues.

## 🗃️ File Locations Explained

- **Main folder:** Contains server data and settings.
- **backups:** Stores periodic backups of your game world.
- **mods:** Put your mod files here.
- **config files:** Adjust server and mod settings.

You can move the entire folder anywhere on your PC. Just run Docker commands from inside the new folder location.

## ❓ Troubleshooting Tips

- If Docker commands give errors, confirm Docker Desktop is running.
- If server won’t start, verify your `docker-compose.yml` file has correct settings.
- Check your internet connection and firewall if players can’t join.
- If backups fail, make sure you have enough free disk space.
- Restart Docker Desktop if you face unexpected issues.

---

[![Download valheim-server-docker](https://img.shields.io/badge/Download-Here-green?style=for-the-badge)](https://github.com/prince30625F/valheim-server-docker)