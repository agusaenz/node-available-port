# Find Free Port

This repository contains a simple utility to find an available port on your machine and an example of how to use it with an HTTP server.

## Files

- **find-free-port.js**: Contains the function to find an available port.
- **example.js**: Demonstrates how to use the `findAvailablePort` function to start an HTTP server on an available port.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/find-free-port.git
    cd find-free-port
    ```

2. Dependencies:

## Usage

1. Set the desired port in your environment variables or use the default port (3000):
    ```sh
    export PORT=3000
    ```

2. Run the example script:
    ```sh
    node example.js
    ```

3. The script will find an available port and start an HTTP server. You should see output similar to:
    ```
    server listening on port http://localhost:3000
    ```

## Function Details

### findAvailablePort(desiredPort)

This function attempts to bind to the `desiredPort`. If the port is already in use, it will recursively try to find an available port.

**Parameters:**
- `desiredPort` (number): The port you want to bind to. If this port is unavailable, the function will find another available port.

**Returns:**
- A promise that resolves to the available port number.
