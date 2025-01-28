# Minitalk  

A **42/1337 School Project** – Minitalk is a simple messaging system that demonstrates inter-process communication using **signals** in C. This project highlights low-level programming skills, signal handling, and process synchronization.

## 📜 Project Overview  

Minitalk consists of a **client** and a **server**:
- **Server**: Receives messages and prints them to the console.
- **Client**: Sends messages to the server using Unix signals (`SIGUSR1` and `SIGUSR2`).

The project emphasizes understanding how to:
- Use Unix signals for IPC (Inter-Process Communication).
- Implement a custom protocol for message encoding and decoding.
- Manage processes efficiently.

---

## 🛠️ Features  
- Custom message encoding using **binary translation**.
- Communication via **SIGUSR1** and **SIGUSR2** signals.
- Reliable transfer of messages with precise timing.
- Supports Unicode/extended ASCII characters.

---

## 🚀 Getting Started  

### Prerequisites  
- **OS**: Linux (tested on Ubuntu).
- **Compiler**: GCC or any C-compatible compiler.  
Ensure you have **Make** installed.

### Installation  
1. Clone this repository:  
   ```bash
   git clone https://github.com/<your_username>/minitalk.git
   cd minitalk
   ```

2. Build the project using Make:  
   ```bash
   make
   ```

---

### Usage  

1. Start the server:  
   ```bash
   ./server
   ```  
   The server will display its **Process ID (PID)**, which is required for the client to send messages.

2. Send a message from the client:  
   ```bash
   ./client <server_pid> "Your message here"
   ```  

Example:  
```bash
./client 12345 "Hello, 42!"
```

---

## 📂 Project Structure  

- **server.c**: Core server logic for receiving and decoding messages.  
- **client.c**: Logic for encoding and sending messages to the server.  
- **Makefile**: Automates the build process for the project.

---

## 🧠 Learning Outcomes  

Through Minitalk, you will:
- Gain a deeper understanding of **process communication**.
- Learn to handle Unix **signals** effectively.
- Master timing and synchronization between processes.

---

## 📋 Evaluation Criteria  

This project follows **1337/42 School**'s rigorous standards:  
- **Norm-compliant** code.  
- No memory leaks (verified with tools like `valgrind`).  
- Efficient and robust communication.

---

## 👩‍💻 Contributions  

If you'd like to contribute:
1. Fork the repository.
2. Create a feature branch:  
   ```bash
   git checkout -b feature-name
   ```  
3. Commit your changes:  
   ```bash
   git commit -m "Description of changes"
   ```  
4. Push your changes:  
   ```bash
   git push origin feature-name
   ```  
5. Submit a pull request!

---


## 🏆 Acknowledgments  

Special thanks to **1337 School** and the **42 Network** for the incredible learning opportunity.

