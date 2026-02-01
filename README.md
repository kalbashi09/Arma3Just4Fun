# 🪖 Arma3Just4Fun: Co-op Setup Guide

A streamlined guide for hosting private Arma 3 sessions with friends using **ZeroTier**. This method bypasses the need for complex port forwarding and works perfectly for small co-op groups.

---

## 🛠 Pre-Flight Checklist
Before starting, ensure everyone in the squad has:
1. **Matching Mods:** Download the `.html` modlist file from this repo. Open the Arma 3 Launcher, go to the **Mods** tab, click **Import**, and select that file.
2. **ZeroTier One:** Download and install from [zerotier.com](https://www.zerotier.com/download/).

---

## 🌐 Network Setup (The "Virtual LAN")
ZeroTier creates a private "tunnel" between your PCs, making Arma think you are in the same room.

### For the Host (The Leader)
1. **Create an Account:** Sign up on the ZeroTier website.
2. **Create a Network:** Click "Create A Network" to generate a **16-digit Network ID**.
3. **Share the ID:** Send that ID to your friends.
4. **Authorize:** As friends join, go to your ZeroTier dashboard, scroll down to **Members**, and **check the "Auth" box** for each friend. They cannot connect until you do this.

### For the Players (The Squad)
1. **Join Network:** Right-click the ZeroTier icon in your **System Tray** (bottom right icons).
2. **Enter ID:** Click "Join Network" and paste the ID provided by the host.
3. **Wait for Auth:** You are connected once the host checks your box on the dashboard.

---

## 🎮 How to Connect
Once the ZeroTier status says "OK," follow these steps:

### 1. Hosting the Game
* Launch Arma 3 -> Multiplayer -> **Server Browser**.
* Click **Host Server**.
* Set a Server Name and Password.
* **IMPORTANT:** Ensure the **UPNP** box is **UNCHECKED** (ZeroTier handles the routing).

### 2. Joining the Game
* Go to the **LAN tab** in the Server Browser. Your friend's server should appear there.
* **If it doesn't appear:** Use the **Direct Connect** button.

### 📍 Finding the Correct IP
If using Direct Connect, the host must provide their **ZeroTier Managed IP**:
1. Right-click ZeroTier in the System Tray.
2. Hover over the Network Name and select **"Show Managed Addresses."**
3. **Copy the IP:** It looks like `192.168.191.x`. (Ignore the `/24` or `/230` suffix).
4. **Port:** Use the default Arma port: `2302`.

---

## 🤝 Joining My Sessions
I host private sessions for a specific group of players. 
* **Steam Group:** We have an active Steam group for coordination. Ask me for an invite!
* **Access:** I only authorize ZeroTier access to players who have contacted me directly first.

---

## 🛡 Troubleshooting & Performance
* **Firewall:** If you can't see the server, ensure **Windows Firewall** allows Arma 3 and ZeroTier through.
* **Network Profile:** Set the ZeroTier connection to "Private" or "Home" when Windows prompts you.
* **CPU Limits:** I host on an i7-4700MQ. To keep frames stable for everyone, I keep the AI count optimized and reasonable.

> [!CAUTION]
> **Security:** Only authorize people you trust. ZeroTier acts like a physical cable plugged into your router. If a stranger joins your dashboard, **Delete/De-auth** them immediately.

**Happy Hunting!**
