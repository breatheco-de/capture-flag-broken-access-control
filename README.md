# Customer Service - Route Discovery and Password Cracking

In this lab, you will explore a web application hosted on an Apache server, identify unauthorized access, and crack encrypted passwords to gain access to sensitive information. You will learn to:

- Detect hidden routes using brute force
- Recognize a case of Broken Access Control
- Analyze and crack MD5 passwords
- Simulate logins for real users

<how-to-start>
   
## 🌱 How to Start This Lab

Follow these instructions to get started:

1. **Download the virtual machine** from this [link](https://storage.googleapis.com/cybersecurity-machines/customer-service-lab.ova).
2. **Import the machine** into your preferred virtualization manager (VirtualBox, VMware, etc.).
3. Once the machine is running, you can start the lab!

</how-to-start>

## 📄 Instructions

You are facing the website of a company offering hosting, domain, and VPS services called **Customer Service**. Your mission is to discover if there is any part of the system that is poorly protected or improperly exposed.

1. **Discover the machine's IP address.**
   - The machine is connected to the same network as you, but its IP has not been provided.
   - Use tools like `nmap`, `netdiscover`, or `arp-scan` to scan the network.

2. **Explore the visible website.**
   - Open your browser and visit the detected IP.
   - Analyze the main page and try to detect if there are hidden directories or routes.

3. **Perform route brute-forcing.**
   - Use tools like `gobuster`, `dirb`, or `ffuf` to discover hidden resources.
   - The goal is to find a hidden panel.

4. **Analyze users and passwords.**
   - Use tools like `john`, `hashcat`, or online services to crack the hashes.

5. **Simulate logging in as different users.**

**Remember:** systems do not always fail due to complex issues. Sometimes, it is enough to bypass a basic access control.

Good luck!
