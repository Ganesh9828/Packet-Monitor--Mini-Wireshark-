 Packet Monitor – Mini Wireshark

A lightweight Java-based network packet analyzer that captures, parses, and visualizes network traffic in real-time. This project functions as a simplified, educational alternative to Wireshark — ideal for learning packet structures, debugging applications, or monitoring network behavior.

 Overview

This tool provides:

Real-time packet sniffing

Analysis of protocols, headers, and metadata

A graphical interface for viewing captured traffic

Search, filtering, and detailed packet breakdown

Perfect for students learning networking or developers debugging network flows

 Features
 Packet Capture

Sniffs live packets directly from a network interface

Works for Ethernet, TCP, UDP, ARP, ICMP and more

Displays source/destination, ports, packet size, protocol

 Packet Analysis

Parses packet structure

Header + payload breakdown

Easy-to-read UI fields

View metadata (TTL, flags, checksum, etc.)

 Graphical User Interface

Built using Java Swing

Windows for packet list, packet details, and inspection

Clean interface for beginners & students

 Extensible Architecture

Analyzer module for packet interpretation

Viewinfo module to display decoded fields

Easy to extend with new protocols

 Project Structure
Packet-Monitor--Mini-Wireshark/
│
├── LICENSE
├── .gitattributes
│
└── Network_traffic_monitor-master/
    └── Network_traffic_monitor-master/
        ├── Analyzer.java           # Core packet decoding logic
        ├── PacketDemo.java         # Main GUI window
        ├── PacketDemo.form         # GUI form design
        ├── Viewinfo.java           # Packet detail viewer
        ├── Viewinfo.form           # UI layout
        ├── Test.java               # Test runner
        ├── manifest.mf             # Manifest for building JAR
        └── nbproject/              # NetBeans project files

 Installation & Setup
1. Clone the repository
git clone https://github.com/yourusername/Packet-Monitor--Mini-Wireshark.git
cd Packet-Monitor--Mini-Wireshark/Network_traffic_monitor-master/Network_traffic_monitor-master

2. Open in NetBeans (recommended)

Go to File → Open Project

Select the folder containing nbproject/

3. Build and Run

Just press Run in NetBeans
—or—
from terminal:

javac *.java
java PacketDemo

 Permissions Requirement (Important)

Packet sniffing often requires administrator/root privileges.

Example (Linux/macOS):

sudo java PacketDemo
 How It Works
 Capture Flow

Raw packet captured from network interface

Forwarded to Analyzer.java

Protocol detection (Ethernet → IPv4 → TCP/UDP…)

Extract headers, ports, flags

Sent to UI for display

User selects packet → Viewinfo shows detailed breakdown

 Packet Fields Parsed

MAC addresses

IP headers

Port numbers

Length

TTL

Flags

Payload (hex view / ASCII)

 Build JAR (Optional)

A manifest.mf file exists for packaging.

jar cfm PacketMonitor.jar manifest.mf *.class
java -jar PacketMonitor.jar

 License

This project is covered under the MIT License.

 Contributing

Feel free to improve the packet decoder, add protocol support, or enhance the GUI.

Support

If you want enhancements like:
✔ Protocol color highlighting
✔ Packet export to .pcap
✔ Live charts
✔ A modern JavaFX GUI

Just tell me — I can help you upgrade this project.


Windows users should run NetBeans/JDK as Administrator.
