# Roll Dice Server

A simple HTTP server that generates random dice rolls (1-6) with OpenTelemetry tracing integration. Built with Oat++ web framework and OpenTelemetry C++.

## What it does

- Provides a REST API endpoint at `GET /rolldice` that returns a random number between 1 and 6
- Instruments the dice roll operation with OpenTelemetry spans for observability
- Runs on `localhost:8080`

## Prerequisites

- C++ compiler (C++17 or newer)
- CMake (version >= 3.25)
- Make
- Oat++ Web Framework (installed in `../oatpp`)
- OpenTelemetry C++ (installed in `../otel-cpp`)

## Build and Run

1. Create a build directory and compile:
```bash
mkdir build
cd build
cmake ..
make
```

2. Run the server:
```bash
./dice-server
```

3. Test the endpoint:
```bash
curl http://localhost:8080/rolldice
```

## Based on

This project follows the [OpenTelemetry C++ Getting Started Guide](https://opentelemetry.io/docs/languages/cpp/getting-started/) and demonstrates basic tracing instrumentation in a web service.