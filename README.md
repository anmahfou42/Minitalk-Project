MiniTalk 🗨️
A lightweight client-server chat application
By: [Your Name/Login]

Badge C License

📖 Overview
MiniTalk is a simple client-server chat application written in C. It allows two programs to communicate using UNIX signals (SIGUSR1 and SIGUSR2). This project is part of the curriculum at 1337 School (42 Network) and demonstrates low-level system programming and inter-process communication (IPC).

✨ Features
Client-Server Architecture: One program acts as the server, the other as the client.

Signal-Based Communication: Uses SIGUSR1 and SIGUSR2 to send bits (0s and 1s).

Unicode Support: Can send ASCII and extended Unicode characters.

Acknowledgement System: The server sends a confirmation signal after receiving each message.

Error Handling: Robust error checks for invalid PIDs, signal errors, and timeouts.

🛠️ Installation
Clone the Repository

bash
Copy
git clone https://github.com/[your_username]/minitlk.git
cd minitlk
Compile the Code

bash
Copy
make
This will generate two executables:

server

client

🚀 Usage
Step 1: Start the Server
Run the server program. It will display its PID:

bash
Copy
./server
> Server PID: 4242
Step 2: Run the Client
Provide the server’s PID and a message to send:

bash
Copy
./client 4242 "Hello, 1337!"
Example Output
Server Side:

plaintext
Copy
Message received: Hello, 1337!
Client Side:

plaintext
Copy
Message sent successfully!
📚 Documentation
For a detailed explanation of the project:

PDF Subject

Technical Notes:

Signals are sent bit-by-bit (8 bits per character).

The server uses usleep to handle signal congestion.

🧪 Testing
Test the program with edge cases:

bash
Copy
# Very long message
./client [PID] "$(cat /dev/urandom | head -c 1000)"

# Empty message (should throw an error)
./client [PID] ""
🤝 Contributing
Fork the repository.

Create a branch: git checkout -b feature/your-feature.

Commit changes: git commit -m 'Add some feature'.

Push to the branch: git push origin feature/your-feature.

Open a Pull Request.

📜 License
This project is licensed under the MIT License. See LICENSE for details.

