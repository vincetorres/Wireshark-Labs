# Wireshark Network Traffic Analysis Lab 

## Objective
Simulate network traffic using `hping3`, capture the traffic in **Wireshark**, apply name resolution settings, and configure custom name resolution to demonstrate the ability to analyze and interpret network traffic.

## Steps

### 1. **Simulate Traffic Using `hping3`**
   - Use `hping3` to send a **SYN** packet to **youtube.com** on port 443 (HTTPS) to generate network traffic for Wireshark capture.  
     Command used:
     ```bash
     Sudo hping3 -S -p 443 youtube.com
     ```

![Simulating traffic using hping3](https://github.com/user-attachments/assets/4d807bd9-ff08-4455-9050-68a25418bf5e)



### 2. **Running Wireshark**
   - Start **Wireshark** and begin capturing traffic on the relevant network interface (e.g., `eth0` or `wlan0`).

### 3. **Name Resolution Settings**
   - Configure **Wireshark** to resolve:
     - **MAC addresses**
     - **Transport names**
     - **IP addresses**
     - **DNS packet data**
     - **System DNS settings**
    
   ![Name Resolution settings](https://github.com/user-attachments/assets/427990fe-1e3a-4d49-b1ca-bc03f63682a8)

   
   These settings ensure that hostnames are resolved in Wireshark. For example, `youtube.com` should appear instead of its raw IP address.

## Before

![Name Resolution Before](https://github.com/user-attachments/assets/20579681-f7c5-40ae-bc3e-565a06476013)


## After

![Name Resolution After](https://github.com/user-attachments/assets/7e32e201-35c1-4bcf-88cb-d44e359ce5cc)



### 4. **Custom Name Resolution**
   - Edit **Name Resolution** settings in Wireshark to associate a custom name (`my-lab-machine.local`) with my local machine’s IP address.
   - **Custom Resolution Steps**:
     - Go to **Edit > Preferences > Name Resolution > Edit**.
     - Add custom name mapping for my IP: `my-lab-machine.local`.

![Custom Name Resolution](https://github.com/user-attachments/assets/4969980d-d37d-4b20-9b36-587d5f819f98)

Result: Once you apply this custom resolution setting, Wireshark will display the mapped name (my-lab-machine.local) instead of the raw IP address in the capture

![Custom Name Resolution - Result](https://github.com/user-attachments/assets/01a82715-7044-4524-b514-23a7d60253ed)


### 5. **Custom Name Resolved in Conversations**
   - Go to **Statistics > Conversations** in Wireshark and verify that the custom name resolution (`my-lab-machine.local`) is visible instead of the raw IP address in the conversation list.

 ![Name resolution reflected in conversations](https://github.com/user-attachments/assets/15c276e7-ae74-4cbf-9345-47a8d50620d8)


### 6. **PCAP Saved**
   - Save the network traffic capture as a `.pcap` file by going to **File > Save As** in Wireshark.

![Proof of pcap](https://github.com/user-attachments/assets/36b160ff-6407-40de-b4be-d57cbcc15d50)


## Results
- **Traffic Simulated**: A SYN packet was successfully sent to YouTube on port 443 using `hping3`.
- **Name Resolution Applied**: The IP address for YouTube resolved to `youtube.com`.
- **Custom Name Resolution**: My local machine’s IP address was resolved to `my-lab-machine.local` in Wireshark.
- **PCAP Saved**: The capture file was saved successfully and is available for further analysis.

