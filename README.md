# Applying A Basic Filter And Inspecting A Packet

## Objective
Analyze a network packet capture file that contains traffic data related to a user connecting to an internet site.
- Identify the source and destination IP addresses involved in this web browsing session.
- Examine the protocols that are used when the user makes the connection to the website.
- Analyze some of the data packets to identify the type of information sent and received by the systems that connect to each other when the network data is captured.

## Applying a Basic Wireshark Filter and Inspecting a Packet
The following filter **ip.addr == 142.250.1.139** was entered in association with traffic for a specific IP address.

<img width="1414" alt="Screenshot 2025-05-21 at 1 41 22 PM" src="https://github.com/user-attachments/assets/207f9677-d22c-4639-a7b5-5a905274dce7" />


The first packet that lists **TCP** as the protocol was opened, revealing a packet details pane window.

<img width="734" alt="Screenshot 2025-05-21 at 1 44 56 PM" src="https://github.com/user-attachments/assets/437251a7-2804-4b3d-8734-1bf6437df0af" />

<img width="671" alt="Screenshot 2025-05-21 at 1 45 24 PM" src="https://github.com/user-attachments/assets/72771e75-8067-42ad-a4b7-071db827f179" />

The upper section of this window contains subtrees where Wireshark will provide an analysis of the various parts of the network packet. The lower section of the window contains the raw packet data displayed in hexadecimal and ASCII text. There is also placeholder text for fields where the character data does not apply, as indicated by the dot **(“.”)**.

<img width="735" alt="Screenshot 2025-05-21 at 1 47 34 PM" src="https://github.com/user-attachments/assets/33ff4104-146a-42af-abd9-5e3974d83f19" />

**Frame** in the first subtree provides details about the overall network packet, or frame, including the frame length and the arrival time of the packet. This level will reveal information about the entire packet of data.

<img width="735" alt="Screenshot 2025-05-21 at 1 48 44 PM" src="https://github.com/user-attachments/assets/5aa9b103-217f-43de-b643-0da0bbf20e9b" />

**Ethernet II** in the subtree contains details about the packet at the Ethernet level, including the source and destination MAC addresses and the type of internal protocol that the Ethernet packet contains.

<img width="734" alt="Screenshot 2025-05-21 at 1 49 11 PM" src="https://github.com/user-attachments/assets/e4740c0a-3a2a-4ac9-b021-158d463ff3c3" />

**Internet Protocol Version 4** in the subtree provides packet data about the Internet Protocol (IP) data contained in the Ethernet packet. It contains information such as the source and destination IP addresses and the Internal Protocol (for example, **TCP** or **UDP**), which is carried inside the IP packet.

<img width="735" alt="Screenshot 2025-05-21 at 1 49 41 PM" src="https://github.com/user-attachments/assets/8cd83447-226b-4487-9ad1-9234e52923bf" />

**Transmission Control Protocol** in the subtree provides detailed information about the TCP packet, including the source and destination TCP ports, the TCP sequence numbers, and the TCP flags.

<img width="719" alt="Screenshot 2025-05-21 at 1 51 36 PM" src="https://github.com/user-attachments/assets/f865f3a8-9a70-4db8-8b4e-4d3d57a82439" />

**Flags** will provide a detailed view of the TCP flags set in this packet.






