# Networking Commands Cheat Sheet 🌐

Made with :heart: by **Fardeen Ahmad Khan**

A quick reference guide to commonly used networking commands for troubleshooting and managing network connections.

Welcome to the Networking Commands Cheat Sheet! 🚀 Whether you're a networking enthusiast or dealing with network-related tasks, this cheatsheet will be your handy companion.

Feel free to bookmark or print this cheatsheet for quick access. If you find it helpful, don't forget to give it a ⭐️ on GitHub!

For more insights and updates, follow the author, Fardeen Ahmad Khan, on [GitHub](https://github.com/I-Fardeen). Let's dive into the world of networking commands and make your network management tasks easier.


## Check Network Status 📊

- Check IP configuration:
  ```bash
  ipconfig (Windows)
  ifconfig (Linux/macOS)
  ```

- Display network interfaces:
  ```bash
  netstat -i (Linux/macOS)
  ```

## Test Connectivity 🌐

- Ping a host:
  ```bash
  ping <host>
  ```

- Perform DNS lookup:
  ```bash
  nslookup <domain>
  ```

- Trace route to a host:
  ```bash
  tracert <host> (Windows)
  traceroute <host> (Linux/macOS)
  ```

## Network Information ℹ️

- Show routing table:
  ```bash
  route print (Windows)
  route -n (Linux)
  ```

- Display active network connections:
  ```bash
  netstat -a (Windows)
  netstat -an (Linux/macOS)
  ```

## Network Configuration ⚙️

- Configure IP address:
  ```bash
  ipconfig /set <interface> <ip_address> (Windows)
  ifconfig <interface> <ip_address> (Linux/macOS)
  ```

- Change hostname:
  ```bash
  hostnamectl set-hostname <new_hostname> (Linux)
  ```

- Configure DNS servers:
  ```bash
  nmcli con mod <connection_name> ipv4.dns <dns_servers> (Linux)
  ```

## Firewall and Security 🔥🛡️

- Display firewall rules:
  ```bash
  iptables -L (Linux)
  netsh advfirewall show allprofiles (Windows)
  ```

- Allow a port through the firewall:
  ```bash
  iptables -A INPUT -p <protocol> --dport <port> -j ACCEPT (Linux)
  ```

- Check open ports:
  ```bash
  nmap -p- <host> (Linux)
  ```

## Wi-Fi Management 📶

- List available Wi-Fi networks:
  ```bash
  nmcli dev wifi list (Linux)
  ```

- Connect to a Wi-Fi network:
  ```bash
  nmcli dev wifi connect <SSID> password <password> (Linux)
  ```

## Miscellaneous 🌀

- Display ARP table:
  ```bash
  arp -a (Windows/Linux/macOS)
  ```

- Flush DNS cache:
  ```bash
  ipconfig /flushdns (Windows)
  sudo systemd-resolve --flush-caches (Linux)
  ```

Remember to run most of these commands with administrative privileges, especially on Windows systems. Always exercise caution while executing network-related commands.

For more detailed information and options, refer to the official documentation of your operating system.

Made with :heart: by **Fardeen Ahmad Khan**
