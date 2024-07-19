# Mini VPN in C
## Overview
This project implements a simple VPN (Virtual Private Network) in C. It uses OpenSSL for encryption and decryption, and supports both client and server modes. The VPN uses AES-128-CBC for encryption and HMAC-SHA256 for message integrity.

## Features
- **Encryption/Decryption:** Uses AES-128-CBC for data encryption and decryption.
- **Message Integrity:** Ensures message integrity using HMAC-SHA256.
- **Client/Server Modes:** Can operate as either a client or a server.
- **Interactive Client Menu:** Provides an interactive menu for the client to input keys and initialization vectors (IVs).
- **SSL/TLS Authentication:** Uses SSL/TLS for secure communication and client-server authentication.
- **UDP and TCP Support:** Supports both UDP and TCP protocols.

## Usage
### Compilation
To compile the project, you need to have OpenSSL installed. Use the following command to compile:
```console
gcc -o minivpn minivpn.c -lssl -lcrypto
```
### Running the VPN
#### Server Mode
To start the VPN in server mode, use the following command:
```console
./minivpn -s <port>
```
Replace `<port>` with the desired port number.

#### Client Mode
To start the VPN in client mode, use the following command:
```console
./minivpn -c <target_ip>:<port>
```

Replace `<target_ip>` with the server's IP address and `<port>` with the server's port number.

### Client Menu
When running in client mode, the following options are available:

- `k`: Enter a new key.
- `i`: Enter a new initialization vector (IV).
- `r`: Randomize key and IV.
- `c`: Clear the current session.
- `s`: Stop the VPN.

## Dependencies
- OpenSSL library