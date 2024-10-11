# Recon

## What is Recon?

### Reconnaissance (Recon) in Cybersecurity
- **Purpose:** Gathering information about a target system or network to identify vulnerabilities.
- **Types:**
  - **Passive Recon:** Gathering information without interacting directly with the target (e.g., WHOIS lookups, DNS queries, social media).
  - **Active Recon:** Direct interaction with the target to gather data (e.g., port scanning, banner grabbing).
  
#### Key Techniques:
1. **Footprinting:** Collecting general info about the target (IP ranges, domain names, DNS info).
2. **Network Scanning:** Identifying live hosts, open ports, and services running.
3. **Vulnerability Scanning:** Detecting known vulnerabilities in systems (using tools like Nmap or Nessus).
4. **Social Engineering:** Using human interaction to gather sensitive information (e.g., phishing).
5. **OSINT (Open Source Intelligence):** Gathering public data from websites, forums, and social media.


## Types of Recon

### Types of Reconnaissance (Recon) in Cybersecurity

#### 1. **Passive Reconnaissance**
- **Description:** Involves gathering information without directly interacting with the target.
- **Techniques:**
  - **WHOIS Lookup:** Identifying domain registration details.
  - **DNS Queries:** Obtaining information about domain names and IP addresses.
  - **Social Media Investigation:** Gathering data from public profiles and posts.
  - **Public Records:** Accessing databases and archives for information.

#### 2. **Active Reconnaissance**
- **Description:** Involves direct interaction with the target to collect information.
- **Techniques:**
  - **Port Scanning:** Identifying open ports and services on the target system.
  - **Ping Sweeping:** Determining which IP addresses are active.
  - **Banner Grabbing:** Collecting information about software and versions running on the target.
  - **Network Mapping:** Creating a visual representation of the network structure.

#### 3. **Social Engineering Reconnaissance**
- **Description:** Manipulating individuals to gain confidential information.
- **Techniques:**
  - **Phishing:** Sending deceptive emails to trick users into revealing sensitive data.
  - **Pretexting:** Creating a fabricated scenario to obtain information.
  - **Baiting:** Using false information or offers to lure targets into revealing data.

#### 4. **Physical Reconnaissance**
- **Description:** Observing the physical environment of the target.
- **Techniques:**
  - **Site Visits:** Physically scouting locations to gather information about security measures.
  - **Surveillance:** Monitoring target behavior and security protocols.

- **Importance:** Understanding these types of recon helps in preparing effective defensive strategies and identifying potential vulnerabilities.


## Important Prerequisites

### CIDR (Classless Inter-Domain Routing)
- **Purpose:** Flexible allocation of IP addresses and efficient routing.
- **Format:** `IP_address/number_of_network_bits`

#### Example 1:
- **192.168.10.0/24**
  - Network: First 24 bits are the network.
  - Host range: `192.168.10.1` to `192.168.10.254`
  - Broadcast: `192.168.10.255`

#### Example 2:
- **192.168.0.0/16**
  - Network: First 16 bits are the network.
  - Host range: `192.168.0.1` to `192.168.255.254`

- **Benefit:** Optimizes IP address allocation by avoiding fixed class sizes (e.g., Class A, B, C).

### ASN (Autonomous System Number)
- **Purpose:** Identifies an Autonomous System (AS) for routing on the internet.
- **Format:** A unique number assigned to a network or group of IPs.
- **Usage:** Helps in routing decisions between different ASes using protocols like BGP.
- **Types:** 
  - **16-bit ASN:** Ranges from `1` to `65535`.
  - **32-bit ASN:** Ranges from `0` to `4,294,967,295`.

- **Example:** A network provider may have ASN `12345` to represent its routing domain.

### IP Pool 
- **Definition:** A range of IP addresses allocated to an organization for use in its network infrastructure.
- **Purpose:** Enables large organizations to assign unique IPs to servers, devices, and users.
- **Usage:** Companies may have a large block of public IPs (IPv4 or IPv6) assigned by a regional internet registry (RIR) for internal and external operations.

#### Example:
- A company might be assigned an IP pool like `192.168.0.0/16`, allowing them to use IP addresses from `192.168.0.1` to `192.168.255.254`.
