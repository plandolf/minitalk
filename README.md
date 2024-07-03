# Minitalk

## Introduction

Minitalk is a simple communication system using UNIX signals. This project involves creating a client and server program where the client sends a string to the server, which then displays it, all done using UNIX signals.

## Features

- **UNIX Signals**: Implements communication using only SIGUSR1 and SIGUSR2, utilizing `sigaction` for handling signals instead of the older `signal` function for improved reliability and control.
- **Client-Server Model**: The server prints its PID for the client to send messages to.
- **Performance**: Efficient and quick message handling.
- **Concurrency**: Handles multiple client requests without restarting the server.
- **Bonus Implemented**: Acknowledgment of message reception and support for Unicode characters.

## Getting Started

### Prerequisites

- A C compiler (GCC recommended)
- Make utility for building the project

### Installation

1) git clone [repository-url] minitalk
2) cd minitalk
3) make all


## Usage

First, start the server:
./server
The server will display its PID. Use this PID to run the client:
./client [server PID] "Message to send"
