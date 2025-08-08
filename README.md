# Drone Communications Analysis & Network Reconnaissance

This project demonstrates how to analyze and interpret drone communications using open-source tools in a controlled environment. Using Python, MAVProxy, and Wireshark, I established a connection between my computer and a drone via Mission Planner and performed packet-level reconnaissance on MAVLink traffic.

##Key Concepts Demonstrated

- Network Protocol Analysis – Observing UDP traffic between devices (drone and GCS).
- Packet Capture with Wireshark – Analyzing MAVLink messages and device behavior.
- IP Discovery & Mapping – Identifying the IPs of the host (192.168.4.27) and drone (192.168.4.20).
- Command-Line Tool Proficiency – Installing and using mavproxy.py via pip.
- Python Network Interaction – Setting up and launching MAVProxy.
- Ethical Reconnaissance – Conducted in a safe, isolated network lab.

## Tools Used

- Python – For installing and running MAVProxy.
- Command Prompt – Command-line interface to interact with tools.
- MAVProxy – CLI ground control station for MAVLink.
- Mission Planner – GUI ground station for monitoring the drone.
- Wireshark – Network sniffer for capturing and analyzing packets.
- Smartphone – Used as a secondary network device to generate activity and perform pings.

## Project Workflow

1. Environment Setup  
Installed Python and MAVProxy using:  
pip install mavproxy  
Configured Mission Planner for UDP communication.

2. Connecting to the Drone  
Ran MAVProxy with:  
mavproxy.py --master=com3 --baudrate=57600 --out=udp:192.168.4.27:14550 --console

3. Capturing Network Traffic  
Started Wireshark on the host machine.  
Interacted with the drone via Mission Planner and monitored MAVLink traffic.

4. Identifying IP Addresses  
Drone: 192.168.4.20  
Host PC: 192.168.4.27  
Used smartphone to ping drone IP to confirm visibility on the local network.

## Screenshots

### MAVProxy Terminal Connection  
![MAVProxy Terminal](https://github.com/Gebrin86/Project-Lab/blob/cf40cedeaaec328fe63033e696605c41d3df3662/Screenshot%202025-07-28%20174105.png)

### Mission Planner Connected  
![Mission Planner](https://github.com/Gebrin86/Project-Lab/blob/d264602e0fc0a0547cc12f0c964d069ce96d2a54/Screenshot%202025-07-28%20174346.png)

### Wireshark MAVLink Packets During Arming  
![Wireshark Arming](https://github.com/Gebrin86/Project-Lab/blob/ac634dc59b925555e91b372c4505d22084628eb2/Screenshot%202025-07-28%20182707.png)

### Phone Ping to Drone  
![Phone Ping](https://github.com/Gebrin86/Project-Lab/blob/6c7d8a14a5d5ca251c73eef1088ba9b63b36f672/IMG_3469.png)

## Observations & Takeaways

- Successfully captured MAVLink UDP packets.
- Identified how the drone and GCS communicate over the local network.
- Highlighted activity during critical drone actions (arming).
- Reinforced skills in packet analysis and ethical reconnaissance.

## Future Enhancements

- Analyze MAVLink packet contents for telemetry and control commands.
- Write Python scripts to parse MAVLink data from .pcap files.
- Simulate and detect spoofed MAVLink packets in a lab setting.
- Explore secure MAVLink alternatives or encryption options.

## ⚠️ Ethical Disclaimer

**This project was conducted in a fully controlled lab environment.**  
The goal is purely educational: demonstrating ethical reconnaissance and packet analysis.
