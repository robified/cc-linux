# The Big Picture

## Levels/Layers of Abstraction in a Linux System
- Each layer contains multiple components
- General Linux system organization
    - User Processes
        - Graphical User Interface
        - Servers
        - Shell
    - Linux Kernel
        - Systems Calls
        - Process Management
        - Memory Management
        - Device Drivers
    - Hardware
        - Processor (CPU)
        - Main Memory (RAM)
        - Disks
        - Network Ports
## Hardware: Understanding Main Memory
- Storage for 1 and 0 called bits

## The Kernel
- Process Management
    - Every process runs individually
    - Context switch decides when the kernel runs
- Memory Management
    - Memory management unit (MMU) => Virtual Memory
    - Memory address map => Page Table
- Device Drivers and Management
- System Calls and Support
    - Between a process and the kernel
    - System calls (syscalls)
        - fork()
            - Creates another process
        - exec()
            - An entire fam of syscalls
    - Example
        - Shell > fork() > shell
            - > copy of shell > exec(ls) > ls
    - Pseudodevices
        - Random number generator device
            - /dev/random

## User Space
- Kernel allocates main memory for users process
- Process 
    - A state or image in memory
- Components
    - Components that uses the same services are either on the same level or below it
        - Depending on where they’re placed, kind of dictates if you want to perform a specific task or make your own task
    - Application
        - User control
    - Utility Service
        - Mail
        - Print
        - Databases
    - Basic Service
        - Uncomplicated tasks
    - Example
        - Application 
            - User Interface
                - Basic Services
                    - Network Configuration
                    - Communication Bus
        - Web Browser
            - Utility Service
                - Mail Server
            - Basic Services
                - Communication Bus
                - Diagnostic Logging

## Users
- Unix User
    - Can run processes and files
    - Username
        - userids
    - Permissions and boundaries
        - Owner
- Superuser
    - root
        - Administrator
        - root access
            - Can terminate/alter/read globally
    - Try to minimize root access as much as possible
    - Still user mode, !kernel mode
- Groups
    - Sets of users