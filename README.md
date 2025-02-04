# Wireshark Network Traffic Analysis

## Objective
Simulate network traffic using `hping3`, capture the traffic in **Wireshark**, apply name resolution settings, and configure custom name resolution to demonstrate the ability to analyze and interpret network traffic.

## Steps

### 1. **Simulate Traffic Using `hping3`**
   - Use `hping3` to send a **SYN** packet to **youtube.com** on port 443 (HTTPS) to generate network traffic for Wireshark capture.  
     Command used:
     ```bash
     hping3 -S -p 443 youtube.com
     ```

### 2. **Running Wireshark**
   - Start **Wireshark** and begin capturing traffic on the relevant network interface (e.g., `eth0` or `wlan0`).
     - (No screenshot for this step, as it simply involves running the tool and starting the capture.)

### 3. **Name Resolution Settings**
   - Configure **Wireshark** to resolve:
     - **MAC addresses**
     - **Transport names**
     - **IP addresses**
     - **DNS packet data**
     - **System DNS settings**
   
   These settings ensure that hostnames are resolved in Wireshark. For example, `youtube.com` should appear instead of its raw IP address.
   
   - **Before and After Screenshots**:
     - Show how the name resolution settings resolve `youtube.com` instead of just the raw IP address.

### 4. **Custom Name Resolution**
   - Edit **Name Resolution** settings in Wireshark to associate a custom name (`my-lab-machine.local`) with my local machine’s IP address.
   - **Custom Resolution Steps**:
     - Go to **Edit > Preferences > Name Resolution > Edit**.
     - Add custom name mapping for my IP: `my-lab-machine.local`.
   
   - **Before and After Screenshots**:
     - Show the process of adding this custom name and how the name appears in the Wireshark interface.

### 5. **Show Custom Name Resolved in Conversations**
   - Go to **Statistics > Conversations** in Wireshark to verify that the custom name resolution (`my-lab-machine.local`) is visible instead of the raw IP address in the conversation list.

### 6. **Proof of PCAP Saved**
   - Save the network traffic capture as a `.pcap` file by going to **File > Save As** in Wireshark.
   - **Screenshot** showing the saved **.pcap** file.

## Results
- **Traffic Simulated**: A SYN packet was successfully sent to YouTube on port 443 using `hping3`.
- **Name Resolution Applied**: The IP address for YouTube resolved to `youtube.com`.
- **Custom Name Resolution**: My local machine’s IP address was resolved to `my-lab-machine.local` in Wireshark.
- **PCAP Saved**: The capture file was saved successfully and is available for further analysis.

