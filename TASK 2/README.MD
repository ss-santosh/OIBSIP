🔥 Basic Firewall Configuration Using UFW

🧾 What This Script Does

This script configures a basic firewall on a Linux system using **UFW (Uncomplicated Firewall)**.  
It performs the following actions:

- Allows SSH traffic on port 22 (to ensure remote access is not blocked).
- Denies HTTP traffic on port 80 (as a basic security measure).
- Displays the current status of the firewall with all active rules.

---

🔐 Why SSH is Allowed and HTTP is Denied

- **SSH (Port 22)** is allowed so that secure remote access remains possible, especially for system administrators.
- **HTTP (Port 80)** is denied in this example to simulate restricting access to web services. This can be useful if a web server is misconfigured or under maintenance.

---

🔧 UFW Basics

UFW (Uncomplicated Firewall) is a frontend for iptables and is designed to make managing a firewall easier.  
Common commands:

- `sudo ufw enable` – Enables the firewall  
- `sudo ufw allow <service>` – Allows a service or port (e.g., ssh)  
- `sudo ufw deny <service>` – Denies a service or port (e.g., http)  
- `sudo ufw status verbose` – Shows detailed status and rules

---

✅ Sample Output

After running the script, the expected output of:

Status: active

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW       Anywhere
80/tcp                     DENY        Anywhere
22/tcp (v6)                ALLOW       Anywhere (v6)
80/tcp (v6)                DENY        Anywhere (v6)
