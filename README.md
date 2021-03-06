# Modbus exporter
Fault tolerant exporter which retrieves stats from a modbus system and exports them via HTTP for Prometheus consumption.

## Building
you just need Go installed, simply run hte build in the directory as:
```bash
go build
```

## Getting Started

To run it:

```bash
./modbus_exporter [flags]
```

The configuration will be taken from a configuration file, the exporter will search a fille called `slaves.yml` in the same directory by default.

Setting a different file and a different listen address:
```bash
./modbus_exporter -config.file="path/to/file" -listen-address=":8080"
```

Help on flags:

```bash
./modbus_exporter --help
```

## Configuration File

Check the `examples/` folder to read the information about the configuration file and some examples.

## TODO
- General clean up
- Tons of test coverage
- Improve global log system
