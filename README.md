# Document Transmission System
# Overview
This system facilitates secure communication between two entities, Alice and Bob, using SSL/TLS for encryption. It ensures the integrity and confidentiality of the data transmitted.

# File Structure
1. alice.py: Script for Alice's end of the communication.
2. bob.py: Script for Bob's end of the communication.
3. server.key: SSL/TLS key file.
4. server.crt: SSL/TLS certificate file.
5. Info-Security Report.pdf: Project report and additional documentation.
6. readme.txt: Basic information about the project.

# Setup Instructions
 SSL/TLS Configuration
 1. Certificate and Key Files: Ensure that server.crt and server.key are located in the same directory as alice.py and bob.py.

 2. Socket Configuration: Wrap the socket with SSL/TLS in both alice.py and bob.py by using the following syntaxin pthon:

ssl_socket = ssl.wrap_socket(
    client_socket,
    server_side=True,
    keyfile="<path_to_server.key>",
    certfile="<path_to_server.crt>",
    ssl_version=ssl.PROTOCOL_TLS
)
Replace <path_to_server.key> and <path_to_server.crt> with the actual file paths of server.key and server.crt.

# Running the Scripts
1. Execute Alice's Script: Run alice.py first. It initializes the connection and waits for Bob's script to connect.
2. Execute Bob's Script: Run bob.py next to establish the connection with Alice's script.
# Additional Notes
1. Ensure Python and necessary SSL libraries are installed.
2. Check the Info-Security Report.pdf for detailed project information and security details.
![ASecurity-Screenshot](https://github.com/aninda20/document-transmission-system/blob/main/Security%20transfer/image/Screenshot.png)


