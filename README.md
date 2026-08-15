# Deep Packet Inspection (DPI) Engine

A high-performance **Deep Packet Inspection (DPI) Engine** designed to analyze network traffic, extract packet information, track network flows, and perform rule-based inspection.

The project focuses on building a lightweight packet analysis framework capable of processing PCAP files and performing real-time traffic analysis using optimized packet processing techniques.

---

## Features

- Packet capture and PCAP file analysis
- Ethernet, IPv4, TCP, and UDP packet parsing
- Five-tuple based flow identification
- Network connection tracking
- TLS SNI (Server Name Indication) extraction
- Rule-based packet inspection
- Multi-threaded packet processing pipeline
- Thread-safe packet queue implementation
- Load balancing across worker threads
- Optimized fast-path packet processing

---

## Project Architecture

```
                Packet Input
                     |
                     |
              PCAP Reader
                     |
                     |
             Packet Parser
                     |
                     |
        +------------+------------+
        |                         |
 Connection Tracker        DPI Engine
        |                         |
        |                    Rule Manager
        |
        |
 Multi-thread Processing Pipeline
        |
        |
     Analysis Output
```

---

## Technologies Used

- C++
- CMake
- Libpcap
- Multi-threading
- Network Protocol Analysis
- TCP/IP Networking Concepts

---

## Directory Structure

```
PacketAnalyzer/
│
├── include/
│   ├── packet_parser.h
│   ├── pcap_reader.h
│   ├── dpi_engine.h
│   ├── connection_tracker.h
│   ├── rule_manager.h
│   ├── thread_safe_queue.h
│   └── types.h
│
├── src/
│   ├── main_dpi.cpp
│   ├── packet_parser.cpp
│   ├── pcap_reader.cpp
│   ├── dpi_engine.cpp
│   ├── connection_tracker.cpp
│   ├── rule_manager.cpp
│   └── load_balancer.cpp
│
├── CMakeLists.txt
├── README.md
└── WINDOWS_SETUP.md
```

---

## Build Instructions

### Linux

Install dependencies:

```bash
sudo apt update
sudo apt install cmake g++ libpcap-dev
```

Build the project:

```bash
mkdir build
cd build

cmake ..
make
```

Run:

```bash
./dpi_engine
```

---

## Windows

Refer to:

```
WINDOWS_SETUP.md
```

for complete installation and build instructions.

---

## Future Improvements

- Real-time packet capture support
- Web-based monitoring dashboard
- Machine learning based traffic classification
- Advanced protocol detection
- Distributed packet processing

---

## Author

Developed as a network security and traffic analysis project.
