
# Investigating Process Lifecycles and OS Interaction

## Introduction

This project focuses on understanding process lifecycles and operating system interaction using C programming in a Linux environment.

The practical activities were performed using Docker Ubuntu, GCC compiler, and Linux commands.

## Objectives

- To understand how a process is created and executed in Linux.
- To learn how to run a process in the background.
- To identify a process using its Process ID (PID) and Parent Process ID (PPID).
- To understand process termination and exit status codes.
- To demonstrate standard input (stdin) and standard output (stdout).
- To understand conditional execution and process termination using C programming.

## Tools and Technologies Used

- Operating System: Linux (Ubuntu)
- Programming Language: C
- Text Editor: GNU Nano
- Compiler: GCC
- Container Platform: Docker
- Linux Commands: ps, echo, sleep, gcc, nano, ls
- System Calls: getpid(), getppid(), sleep()

## Project Tasks

### Task 1: Long-Running Process

Created a C program that runs for approximately 30 seconds using a loop and sleep() function.

The program was executed in the background using the ampersand (&) symbol.

Commands:
```bash
gcc task1_alive.c -o task1
./task1 &
ps aux | grep task1
```

### Task 2: PID and PPID

Used getpid() and getppid() to retrieve the current process ID and parent process ID.

Commands:
```bash
gcc task2_identity.c -o task2
./task2 &
ps -p <PID> -o pid,ppid,cmd
```

Replace <PID> with the actual process ID displayed by the program.

### Task 3: Exit Codes

Demonstrated successful and unsuccessful program termination using return 0 and return 1.

Commands:
```bash
gcc task3_exit.c -o task3
./task3
echo $?
```

### Task 4: Standard I/O

Used scanf() to receive user input and printf() to display output.

Commands:
```bash
gcc task4_input.c -o task4
./task4
```

### Task 5: Conditional Execution and Termination

Used getpid(), scanf(), if-else statements, sleep(), and return values to control program execution.

Commands:
```bash
gcc task5_control.c -o task5
./task5
echo $?
```

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

Start an Ubuntu Docker container:

```bash
docker run -it --name process-lab ubuntu:latest bash
```

Install required packages:

```bash
apt update
apt install gcc nano procps -y
```

Verify GCC installation:

```bash
gcc --version
```

## Compilation

Each C source file can be compiled using GCC.

Example:

```bash
gcc task1_alive.c -o task1
./task1
```

## Learning Outcomes

This laboratory helped develop practical knowledge of:

- Linux process management.
- Background process execution.
- Process identification using PID and PPID.
- Program exit status verification.
- Standard input and output.
- Conditional execution and process termination.

## Conclusion

The five practical tasks demonstrated different aspects of process management and operating system interaction using C programming in Linux.

The practical use of C functions and Linux commands improved the understanding of how processes are executed, monitored, and terminated.

## Author

BSc (Hons) Ethical Hacking and Cyber Security Student
