# Simple Load Balancer in Go

This is a simple implementation of a load balancer in Go, capable of distributing HTTP requests among multiple backend servers. The load balancer uses round-robin scheduling to evenly distribute requests among the available servers.

## Usage

1. **Clone the Repository**: Clone this repository to your local machine.

2. **Build and Run**: Navigate to the directory containing the `main.go` file and build the project using the following command:

    ```bash
    go build main.go
    ```

    Then, run the executable:

    ```bash
    ./main
    ```

    Alternatively, you can run the application directly without building:

    ```bash
    go run main.go
    ```

3. **Accessing the Load Balancer**: The load balancer listens on port 8000 by default. You can access it through `http://localhost:8000`.

## Code Explanation

The main components of the load balancer include:

- **Server Interface**: Defines the methods required for a server.
- **Simple Server**: Implements the `Server` interface and represents a backend server.
- **Load Balancer**: Manages multiple backend servers and distributes incoming requests.
- **getNextAvailableServer()**: Determines the next available server to handle the request using round-robin scheduling.
- **serveProxy()**: Forwards incoming requests to the appropriate backend server.
- **Main Function**: Initializes the load balancer with sample backend servers and starts the HTTP server to listen for incoming requests.

## Sample Backend Servers

The load balancer is initialized with the following sample backend servers:

- [YouTube](https://www.youtube.com)
- [DuckDuckGo](https://www.duckduckgo.com)
- [Bing](https://www.bing.com)

## Dependencies

This project utilizes standard Go libraries and does not require any external dependencies.

## Contributing

Contributions are welcome! Feel free to fork this repository and submit pull requests for any improvements or features you'd like to add.
