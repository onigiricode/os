# OS (0.1.0)

Official "Operating System" plugin for OnigiriCode

## Installation

Add the plugin to your project:

```bash
mizu add os
```

## API Reference

### File System
- `read_file(path: String) -> String`: Reads the content of a file
- `write_file(path: String, content: String) -> Bool`: Writes into a file
- `delete_file(path: String) -> Bool`: Deletes a file
- `file_exists(path: String) -> Bool`: Checks if a file exists
- `create_dir(path: String) -> Bool`: Creates a directory
- `delete_dir(path: String) -> Bool`: Deletes a directory
- `list_dir(path: String) -> List`: Lists content of a directory

### System
- `get_env(name: String) -> String`: Gets a environment variable
- `set_env(name: String, value: String) -> Bool`: Sets a environment variable
- `get_os() -> String`: Gets OS's name
- `get_hostname() -> String`: Gets Hostname
- `get_username() -> String`: Gets username
- `get_home_dir() -> String`: Gets home directory

### Processes
- `execute(command: String) -> String`: Executes a shell command
- `get_pid() -> Number`: Gets PID of the current process
- `sleep(ms: Number) -> Void`: Stops a process for the defined milliseconds

## License

MIT License
