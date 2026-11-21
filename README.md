
# Investigating Process Lifecycles and OS Interaction

## About the Project

This project explores process lifecycles and operating system interaction using C programming in a Linux environment.

The practical activities were performed using Docker Ubuntu and basic Linux commands.

## Objectives

- Understand how processes are created and executed.
- Identify Process ID (PID) and Parent Process ID (PPID).
- Understand program exit codes.
- Practise standard input and output.
- Explore conditional execution and process termination.

## Tasks

### Task 1: Long-Running Process
Demonstrates background process execution and process monitoring using Linux commands.

### Task 2: PID and PPID
Uses `getpid()` and `getppid()` to identify process and parent process IDs.

### Task 3: Exit Codes
Demonstrates successful and unsuccessful program termination using return values and `echo $?`.

### Task 4: Standard I/O
Uses `scanf()` and `printf()` to accept and display user input.

### Task 5: Conditional Execution and Termination
Uses user input and conditional statements to control program execution and termination.

## Technologies and Tools

- C Programming
- Docker Ubuntu
- GCC Compiler
- Linux Terminal
- GNU Nano
- Linux Process Commands

## Project Structure

```text
Investigating-Process-Lifecycles/
│
├── README.md
├── .gitignore
│
├── src/
│   ├── task1_alive.c
│   ├── task2_identity.c
│   ├── task3_exit.c
│   ├── task4_input.c
│   └── task5_control.c
│
├── screenshots/
│   ├── task1/
│   ├── task2/
│   ├── task3/
│   ├── task4/
│   └── task5/
│
└── report/
    └── laboratory-report.docx
```

## Environment Setup

Start an Ubuntu container:

```bash
docker run -it --name process-lab ubuntu:latest bash
```

Install the required tools inside Ubuntu:

```bash
apt update
apt install gcc nano procps -y
```

Check GCC installation:

```bash
gcc --version
```

## Compilation and Execution

Example:

```bash
gcc src/task1_alive.c -o task1
./task1
```

Refer to the individual source files for each practical task.

## Learning Outcomes

This laboratory improved my understanding of Linux processes, process identification, exit status, standard input/output, and conditional execution using C programming.

## Author

BSc (Hons) Ethical Hacking and Cyber Security Student
