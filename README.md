# Custom TCP Server

A lightweight Go TCP server that accepts client connections, reads incoming messages, and logs them to the console. It is designed as a simple foundation for learning socket programming, message handling, and basic network server patterns in Go.

## Features

- Listens for TCP connections on port 3000
- Accepts multiple client connections concurrently
- Reads incoming data from each client connection
- Sends a welcome message when a client connects
- Confirms receipt of each message with a response
- Prints the sender address and payload to the terminal

## Project Structure

```text
Custom_TCP_Server/
├── README.md
└── server/
    ├── go.mod
    └── main.go
```

## Prerequisites

- Go 1.20 or later

## Running the Server

From the project root:

```bash
cd server
go run .
```

The server starts listening on:

```text
:3000
```

## Example Usage

You can test it using a simple TCP client such as `nc`:

```bash
nc localhost 3000
```

Once connected, type a message and press Enter. The server will:

- display the client address and message in the terminal
- send back: `thank you for your message!`

## Example Output

```text
New connection to the server 127.0.0.1:54321
received message from connection (127.0.0.1:54321):hello from client
```

## Notes

This project is intentionally minimal and serves as a starting point for building more advanced networking features such as:

- multiple room/chat handling
- message broadcasting
- authentication
- protocol parsing
- persistent storage or logging

## License

This project is provided as-is for learning and experimentation.
