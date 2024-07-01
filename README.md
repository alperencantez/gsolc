# gsolc

This Go package provides a basic Solidity compiler by leveraging the existing Solidity compiler package in Node.js. It uses the V8 engine bindings from Chromium to run the Node.js compiler within the Go environment.

## Table of Contents

- [Installation](#installation)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Installation

### Prerequisites

Ensure you have the following installed:

- Go (1.19+)

### Steps

1. **Clone the repository:**

    ```sh
    git clone https://github.com/alperencantez/gsolc.git
    cd gsolc
    ```

2. **Build the Go package:**

    ```sh
    cd ..
    go build
    ```

## Usage

Here's a basic example of how to use the package:

```go
package main

import (
    "fmt"
    "log"
    "github.com/alperencantez/gsolc"
)

func main() {
    source := `pragma solidity ^0.8.0; contract HelloWorld { string public message = "Hello, World!"; }`
    compiled, err := gscolc.Compile(source)
    if err != nil {
        log.Fatalf("Compilation error: %v", err)
    }
    fmt.Println("Compiled bytecode:", compiled.Bytecode)
}
```

## Dependencies

This project relies on the following dependencies:

- [Golang V8 Engine Bindings](https://github.com/rogchap/v8go)
- [Solidity Compiler (solc-js)](https://www.npmjs.com/package/solc)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
