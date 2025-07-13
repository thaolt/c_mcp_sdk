c_mcp_sdk
=========

This is a C implementation of the Model Context Protocol (MCP) SDK, designed to
help developers create MCP servers in C. The project provides a lightweight,
efficient framework for building MCP-compliant servers with minimal dependencies.

## Implemented specifications

- [Model Context Protocol](https://modelcontextprotocol.io/specification/2025-06-18/)
- [JSON-RPC 2.0](https://www.jsonrpc.org/specification)

## Project Purpose

The Model Context Protocol is a specification for AI assistants to communicate
with external tools and data sources. This C SDK focuses on implementing the MCP
protocol itself, providing the core functionality needed to create MCP-compliant
applications.

### Protocol Implementation

The `c_mcp_sdk` library is specifically designed to handle MCP protocol
implementation, including:

- JSON-RPC message parsing and serialization
- MCP-specific message types and structures
- Tool registration and request processing
- Efficient memory management

### Transportation Layer

While the library focuses on protocol implementation, there are no limitations on
transportation implementations. The SDK provides:

**STDIO Support**: Built-in support for reading and parsing MCP messages over
standard input/output streams, making it easy to create command-line MCP servers.

**HTTP Transportation**: For HTTP-based MCP servers, we recommend using:

- [cesanta/mongoose](https://github.com/cesanta/mongoose) - Lightweight, portable
HTTP server
- [mbedtls](https://github.com/Mbed-TLS/mbedtls) - TLS/SSL library for secure
connections

We will provide examples demonstrating HTTP server implementation using these
libraries to show how to integrate the MCP protocol with HTTP transportation.

## Included third-party libraries

- [pdjson](https://github.com/skeeto/pdjson) is used for JSON parsing.

## Build

```sh
cmake -B build
cmake --build build
```

## Demo

```
npx -y @modelcontextprotocol/inspector ./build/demo/simple_datetime_mcp
```
