c_mcp_sdk
=========

This is a C implementation of the Model Context Protocol (MCP) SDK, designed to
help developers create MCP servers in C. The project provides a lightweight,
efficient framework for building MCP-compliant servers with minimal dependencies.

## Implemented specifications

- [Model Context Protocol](https://modelcontextprotocol.io/specification/2025-06-18/basic/transports)
- [JSON-RPC 2.0](https://www.jsonrpc.org/specification)

## Project Purpose

The Model Context Protocol is a specification for AI assistants to communicate
with external tools and data sources. This C SDK enables developers to:

- Create MCP servers in C for high-performance applications
- Handle JSON-RPC communication over stdio
- Manage tool registration and request processing
- Provide efficient memory management through arena allocation

## Included third-party libraries

- [pdjson](https://github.com/skeeto/pdjson) is used for JSON parsing.


## Build

```
cmake -B build
cmake --build build
```


## Demo

```
./build/demo/simple_datetime
```


