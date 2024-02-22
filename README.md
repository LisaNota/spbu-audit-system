# System Audit Tool

## Description
This project implements a system audit tool for monitoring Linux systems by tracking system calls made by a specified process. The tool utilizes `ptrace` to attach to a target process, intercept system calls, and log them along with relevant information such as the process ID, timestamp, and the name of the system call.

## Features
- **System Call Monitoring**: Tracks system calls made by a specified process in real-time.
- **Logging**: Records system call events to a log file (`audit.log`) for auditing and analysis purposes.
- **Customizable**: Supports customization of the monitored process by specifying its process ID (PID) as a command-line argument.
- **System Call Mapping**: Maps system call numbers to their corresponding names for better readability in the log file.

## Installation
1. Clone the repository: `git clone https://github.com/username/repository.git`
2. Navigate to the project directory: `cd repository`
3. Compile the source code: `g++ -o audit_tool audit_tool.cpp`

## Usage
1. Run the compiled executable with the PID of the target process as a command-line argument: `./audit_tool <PID>`
2. The tool will attach to the specified process, start monitoring its system calls, and log them to `audit.log`.
3. To stop monitoring, terminate the tool or detach it from the process using `Ctrl+C`.
