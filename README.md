# Task-4-Setup-and-Use-a-Firewall-on-Windows
Configure and test basic firewall rules to allow or block traffic using the window firewall tool 

# Windows Firewall Configuration Task
## Objective
Configure and test basic firewall rules to allow or block traffic.

## Tools Used
- **Windows Defender Firewall with Advanced Security** (built into Windows OS)

### 1. Open Windows Firewall Configuration Tool
1. Press `Win + S` and search for **Windows Defender Firewall with Advanced Security**.
2. Open the tool.

### 2. List Current Firewall Rules
- In the left pane, click **Inbound Rules**.
- Existing rules are displayed with:
  - **Name**: The application/port name.
  - **Action**: Allow or Block.
  - **Protocol/Port**: TCP, UDP, etc.
  - **Profile**: Domain, Private, Public.

### 3. Add a Rule to Block Inbound Traffic on Port 23 (Telnet)
1. In **Inbound Rules**, click **New Rule…** (right Actions pane).
2. Select **Port** → Click **Next**.
3. Select **TCP**, specify port **23** → Click **Next**.
4. Select **Block the connection** → Click **Next**.
5. Apply rule to all profiles (Domain, Private, Public) → Click **Next**.
6. Name it **Block TCP Port 23** → Click **Finish**.

---

### 4. Test the Rule
- Try connecting to port 23 using `telnet <IP> 23`.
- The connection should fail.

### 5. Remove the Test Block Rule
1. In **Inbound Rules**, find `Block TCP Port 23`.
2. Right-click → **Delete**.
3. Confirm deletion.

### 6. How the Firewall Filters Traffic
- **Rule-Based Filtering**: Matches traffic to allow/block rules based on protocol, port, program, IP address, and profile.
- **Profiles**: Domain, Private, Public — determines when rules apply.
- **Direction**:  
  - *Inbound rules* control traffic entering the system.  
  - *Outbound rules* control traffic leaving the system.
- **Priority**: Block rules override allow rules when both apply.

## Deliverables
- **Before Rule Screenshot** – inbound rules before adding the block.
- **After Rule Screenshot** – inbound rules with `Block TCP Port 23`.
- **Test Result** – Telnet connection blocked.

## Outcome
Gained hands-on experience with:
- Viewing and managing firewall rules.
- Creating and deleting inbound port block rules.
- Understanding Windows Firewall traffic filtering.
