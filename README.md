# internship_task_5

# Task 5: Capture and Analyze Network Traffic Using Wireshark.
## Objective: Capture live network packets and identify basic protocols and traffic types.
### Tools: Wireshark
### Deliverables: A packet capture (.pcap) file and a short report of protocols identified. 

## Outcome: Hands-on packet analysis skills and protocol awareness. 

## Installation
    Download wireshark or check if already installed on Kali linux.
    Capture Setup
    Confirmed packet flow before starting capture.
    Generated Network Traffic
    Identify and Analyze Protocols.
        1. DNS (Domain Name System) - Translates domain names to IP addresses.
        ## DNS traffic is usually over UDP port 53. Attackers often use DNS tunneling to exfiltrate data in corporate breaches. Monitoring DNS anomalies is a critical security practice.

        2. TCP (Transmission Control Protocol) - Reliable connection-oriented communication
        ## TCP handshake timing and flags (RST, FIN) can reveal port scans or session hijacks. TCP retransmissions or duplicate ACKs indicate possible network issue 
        3-Way Handshake: SYN → SYN-ACK → ACK observed

        3. HTTP (HyperText Transfer Protocol) - Transfer of web pages and resources.
        HTTP traffic reveals full URLs and content in plaintext — exposing data during man-in-the-middle (MITM) attacks if HTTPS is not enforced.

        4. TLS/SSL (Transport Layer Security) - Secure encrypted communication (used in HTTPS).
        TLS handshake visibility helps identify weak encryption (e.g., TLS 1.0) and track potential certificate forgery in spoofed sites.

        5. ICMP (Internet Control Message Protocol) - Diagnostic protocol (used by ping).
        ICMP floods (ping of death) and smurf attacks are often used in DoS/DDoS attacks. Restricting ICMP traffic is a common security policy in enterprise networks.

### Packet Dissection: Wireshark shows multi-layer views: Ethernet → IP → TCP → Application protocols.

### Protocol Stack Visualization: Ability to identify where security issues lie — from physical to application layer.

## Behavior Analysis: 
  Can monitor unusual patterns, such as:

      High DNS request frequency (sign of malware beaconing)
      HTTP POST requests with suspicious payloads
      TLS using self-signed certificates (phishing/spoofing)

        

        

        
        
