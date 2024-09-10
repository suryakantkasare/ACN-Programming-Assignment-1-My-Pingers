# ACN-Programming-Assignment-1-My-Pingers

**Make sure you are in the directory where you have saved the files before running the programs.**

---

## Part 1: UDP Pinger

### Files Used:
1. `UDPPingerServer.py`
2. `UDPPingerClient.py`
3. `UDPPingerModifiedServer.py`
4. `UDPPingerThreadServer.py`

### Task 1:

1. **Check Server and Client with Local Host**
    - Ensure the server socket binds to the local address in the server program and sends packets to the respective server in the client.
    - **Run Server**:
      ```bash
      python3 UDPPingerServer.py
      ```
    - **Run Client** (on the same machine):
      ```bash
      python3 UDPPingerClient.py
      ```

2. **Check Server and Client with Single Client**
    - Ensure the server socket binds to your address in the server program and sends packets to the respective server in the client (on other machines).
    - **Run Server**:
      ```bash
      python3 UDPPingerServer.py
      ```
    - **Run Client** (on the second machine):
      ```bash
      python3 UDPPingerClient.py
      ```

3. **Check Server and Client with Multiple Clients**
    - Ensure the server socket binds to your address in the server program and sends packets to the respective server in the clients on other machines.
    - **Run Server**:
      ```bash
      python3 UDPPingerThreadServer.py
      ```
    - **Run Client** (on multiple machines):
      ```bash
      python3 UDPPingerClient.py
      ```

4. **Check Server and Client with Modified Server**
    - Simulate packet loss on your network interface using the Linux `tc` command.
    - **Simulate Packet Loss**:
      ```bash
      sudo tc qdisc add dev wlp0s20f3 root netem loss 30%
      ```
    - **Run Server**:
      ```bash
      python3 UDPPingerModifiedServer.py
      ```
    - **Run Client** (on multiple machines):
      ```bash
      python3 UDPPingerClient.py
      ```
    - **Stop Simulating Packet Loss**:
      ```bash
      sudo tc qdisc del dev wlp0s20f3 root netem loss 30%
      ```

---

## Part 2: TCP Pinger

### Files Used:
1. `TCPPingerServer.py`
2. `TCPPingerClient.py`
3. `TCPPingerModifiedServer.py`
4. `TCPPingerThreadServer.py`

### Task 1:

1. **Check Server and Client with Local Host**
    - Ensure the server socket binds to the local address in the server program and connects to the respective server in the client.
    - **Run Server**:
      ```bash
      python3 TCPPingerServer.py
      ```
    - **Run Client** (on the same machine):
      ```bash
      python3 TCPPingerClient.py
      ```

2. **Check Server and Client with Single Client**
    - Ensure the server socket binds to your address in the server program and connects to the respective server in the client (on other machines).
    - **Run Server**:
      ```bash
      python3 TCPPingerServer.py
      ```
    - **Run Client** (on the second machine):
      ```bash
      python3 TCPPingerClient.py
      ```

3. **Check Server and Client with Multiple Clients**
    - Ensure the server socket binds to your address in the server program and connects to the respective server in the clients on other machines.
    - **Run Server**:
      ```bash
      python3 TCPPingerThreadServer.py
      ```
    - **Run Client** (on multiple machines):
      ```bash
      python3 TCPPingerClient.py
      ```

4. **Check Server and Client with Modified Server**
    - Simulate packet loss on your network interface using the Linux `tc` command.
    - **Simulate Packet Loss**:
      ```bash
      sudo tc qdisc add dev wlp0s20f3 root netem loss 30%
      ```
    - **Run Server**:
      ```bash
      python3 TCPPingerModifiedServer.py
      ```
    - **Run Client** (on multiple machines):
      ```bash
      python3 TCPPingerClient.py
      ```
    - **Stop Simulating Packet Loss**:
      ```bash
      sudo tc qdisc del dev wlp0s20f3 root netem loss 30%
      ```

---

## Part 3: ICMP Pinger

### File Used:
1. `ICMPPinger.py`

### Task:

- Since root privileges are needed to run the ICMP code, use `sudo` before executing the command.

    ```bash
    sudo python3 ICMPPinger.py
    ```
    Enter your password when prompted:

    ```bash
    password: <enter your password>
    ```
