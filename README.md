# ACN-Programming-Assignment-1-My-Pinger

---
**Make sure you are in the directory where you have saved the files before running the programs.**
---

## **Task 1: UDP Pinger**

**Files:**
- `client.py`
- `server.py`
- `serverModified.py`

**Tasks:**

1. **Local Host Test**
   - **Run UDP Server:**
     ```bash
     python3 server.py
     ```
   - **Run UDP Client (on the same machine):**
     ```bash
     python3 client.py
     ```

2. **Single Client Test**
   - **Run UDP Server:**
     ```bash
     python3 server.py
     ```
   - **Run UDP Client (on a different machine):**
     ```bash
     python3 client.py
     ```

3. **Multiple Clients Test**
   - **Run Multi-client UDP Server:**
     ```bash
     python3 serverThread.py
     ```
   - **Run UDP Client (on multiple machines):**
     ```bash
     python3 client.py
     ```

4. **Packet Loss Simulation**
   - **Simulate Packet Loss:**
     ```bash
     sudo tc qdisc add dev wlp0s20f3 root netem loss 30%
     ```
     Enter your password when prompted:
     ```bash
     password: <enter your password>
     ```
   - **Run Modified UDP Server:**
     ```bash
     python3 serverModified.py
     ```
   - **Run UDP Client (on multiple machines):**
     ```bash
     python3 client.py
     ```
   - **Stop Packet Loss Simulation:**
     ```bash
     sudo tc qdisc del dev wlp0s20f3 root netem loss 30%
     ```
     Enter your password when prompted:
     ```bash
     password: <enter your password>
     ```

---

## **Task 2: TCP Pinger**

**Files:**
- `TCPPingerClient.py`
- `TCPPingerServer.py`
- `TCPPingerThreadServer.py`

**Tasks:**

1. **Local Host Test**
   - **Run TCP Server:**
     ```bash
     python3 TCPPingerServer.py
     ```
   - **Run TCP Client (on the same machine):**
     ```bash
     python3 TCPPingerClient.py
     ```

2. **Single Client Test**
   - **Run TCP Server:**
     ```bash
     python3 TCPPingerServer.py
     ```
   - **Run TCP Client (on a different machine):**
     ```bash
     python3 TCPPingerClient.py
     ```

3. **Multiple Clients Test**
   - **Run Multi-client TCP Server:**
     ```bash
     python3 TCPPingerThreadServer.py
     ```
   - **Run TCP Client (on multiple machines):**
     ```bash
     python3 TCPPingerClient.py
     ```

4. **Packet Loss Simulation**
   - **Simulate Packet Loss:**
     ```bash
     sudo tc qdisc add dev wlp0s20f3 root netem loss 30%
     ```
     Enter your password when prompted:
     ```bash
     password: <enter your password>
     ```
   - **Run Modified TCP Server:**
     ```bash
     python3 TCPPingerModifiedServer.py
     ```
   - **Run TCP Client (on multiple machines):**
     ```bash
     python3 TCPPingerClient.py
     ```
   - **Stop Packet Loss Simulation:**
     ```bash
     sudo tc qdisc del dev wlp0s20f3 root netem loss 30%
     ```
     Enter your password when prompted:
     ```bash
     password: <enter your password>
     ```

---

## **Task 3: ICMP Pinger**

**File:**
- `ICMP_Pinger.py`

**Task:**
- **Run ICMP Pinger (requires root privileges):**
  ```bash
  sudo python3 ICMP_Pinger.py
  ```
  Enter your password when prompted:
  ```bash
  password: <enter your password>
  ```

---

## **Task 4: UDP with ICMP**

**Files:**
- `clientUdp.py`
- `serverUdp.py`

**Tasks:**

1. **Test UDP with ICMP**
   - **Run UDP Server:**
     ```bash
     sudo python3 serverUdp.py
     ```
   - **Run UDP Client:**
     ```bash
     sudo ython3 clientUdp.py
     ```
     Enter your password when prompted:
     ```bash
     password: <enter your password>
     ```

---

## **Task 5: TCP with ICMP**

**Files:**
- `client.py`
- `server.py`

**Tasks:**

1. **Test TCP with ICMP**
   - **Run TCP Server:**
     ```bash
     sudo python3 server.py
     ```
   - **Run TCP Client:**
     ```bash
     sudo python3 client.py
     ```
  
     Enter your password when prompted:
     ```bash
     password: <enter your password>
     ```

---
## Blocking IP Addresses

To block specific IP addresses using `iptables` and reject ICMP packets with a specific error response, use the following command:

```bash
sudo iptables -A INPUT -s <source_ip_address> -p icmp -j REJECT --reject-with <error_response>
