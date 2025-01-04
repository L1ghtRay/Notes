# Introduction to Operating Systems

Software that manages computer hardware, provides basis for application programs and acts as intermediary between user and hardware is called a operating system.

Goals of a OS:
- Execute user programs and make solving user problems easier
- Make the computer system convenient to use
- Use computer hardware in an efficient manner
### Computer System Structure

- **Hardware**: Provides basic computing resources.
- **Operating System**: Controls and co-ordinates use of hardware among various applications and users.
- **Application Program**: Define the ways in which the system resources are used to solve the computing problems of the user.
- **Users**: People, machines or other computers.

### Abstract View of Components

![300](../Reference/Pasted%20image%2020241225200227.png)
### What Does an Operating System (OS) Do?

The role of an Operating System (OS) depends on the perspective:

1. **For Users**:   
	- Focus is on convenience, ease of use, and performance.
	- Users typically do not concern themselves with resource allocation or system management.
2. **For Shared Computers (e.g., Mainframes, Servers)**:  
    - The OS acts as a resource allocator and control program.
    - It ensures efficient use of hardware resources and manages the execution of user programs, keeping all users satisfied and preventing conflicts.
3. **For Mobile Devices (e.g., Smartphones, Tablets)**:
    - Optimized for usability and battery life.
    - The OS prioritizes a smooth user experience while balancing power efficiency.
4. **For Embedded Systems**:
    - These systems typically have minimal or no user interface.
    - The OS operates primarily without user intervention, focusing on reliability and task-specific functions.
### Computer System Operation

One or more CPUs, device controllers connect through common bus providing access to shared memory.

![](../Reference/Pasted%20image%2020241225211741.png)

Device drivers interact with the device controller and provide the rest of the OS with a uniform interface to the devices. The CPU and device controllers can execute in parallel, competing for memory cycles to ensure orderly access to shared memory. A memory controller synchronizes access to the memory.

- Each type of device controller has an operating system driver that manages the device.
- Each device has a local buffer.
- CPU moves data from/to main memory to/from local buffers.
- I/O sends data form device to local buffers.
- Device controller informs the CPU that it has finished its operation using an interrupt.
### Interrupt Handling

1. **Initialize I/O operations**: The system prepares to handle input/output operations.
2. **Program requests an I/O operation**: A program issues a request to perform an I/O operation (e.g., reading or writing data).
3. **OS invokes the device driver**: The operating system calls the appropriate device driver to handle the operation.
4. **Device driver configures necessary registers**: The device driver sets up the appropriate registers in the device controller to prepare it for the I/O operation.
5. **Device controller initiates data transfer**: The device controller starts transferring data to/from its local buffer.
6. **Suspends the program**: The program that requested the I/O operation is suspended (usually in a waiting state) until the operation is completed.
7. **Interrupt is sent upon completion**: Once the I/O operation is finished, the device controller sends an interrupt to notify the OS that the operation is complete.
8. **Interrupt is processed**: Upon receiving the interrupt, the OS processes it by handling the completion of the I/O operation and resuming the suspended program.

![600](../Reference/Pasted%20image%2020241226120844.png)
### Multi-Processors

aka. parallel systems, tightly coupled systems.


## Virtualizing the CPU
## Virtualizing the memory
## Concurrency
## Persistence
## Design Goals
# Components of an OS
# Types of OS
# Operating System structure
## Simple structure

Many OSs do not have well defined structures. Eg: MS-DOS

Application programs scan directly access low level hardware. This can cause errors in the system.

The design of an OS is closely depended on the processor it is intended to run on.

Due to this it’s functionality is limited. We cannot use duel mode.

MS-DOS was for Intel 8088 processor.

Interface and levels of functionality are not well separated.

Leaves vulnerabilities or errant (malicious) programs causes entire system to crash when user program fails.

Another simple structure OS is original UNIX OS
## Layered approach

The IS is broken into a number of layers (levels). The bottom layer (layer 0) is the hardware and the highest layer (layer $N$) is the user interface.

An OS layer is an implementation of an abstract object made up of data and the operations that can manipulate those data.

A typical OS layer - say, layer $M$ - consists of data structures and a set of routines that can be invoked by higher level layers.

Layer $M$, in turn, can invoke operations on lower-level layers.
### Advantages

- Modularity
- Easy debugging
- Easy update
- No direct access to hardware
- Abstraction
### Disadvantages

- Complex and careful implementation
- Slower in execution due to system call overhead
## Microkernel

This method structure the OS by removing the non-essential components from the kernel and implementing them as system and user-level programs. The result is a smaller kernel.

The main function of the microkernel is to provide communication between the client program and the various services that are also running in user space.

The client program and service never interact directly. Rather, they communicate indirectly by exchanging message with the microkernel. This is called **Message Passing**.
### Advantages

- It enables portability
- It is reliable and secure
- The reduced size of microkernels allows for successful testing.
- The remaining OS remains unaffected and keeps running properly even if a component of microkernel fails.
### Disadvantages

- The performance of the system is decreased by increased inter-modular communication.
- The construction of the system is complicated.
## Modules

The kernel has a set of core components and links in additional services via modules, either at boot time or during run-time.

This type of design is common in modern implementations of UNIX, such as Solaris, Linus and Mac OS X; as well as Windows.
## Hybrid structure

Very few OSs adopt a single, strictly defined structure. Instead, they combine different structures resulting in hybrid systems that address performance, security and usability issues.
# Generalized view of System Calls

A system call is a method for a computer program to request a service from the kernel of the OS on which it is running.

A system call is a method of interacting with the OS via programs.

These calls are generally available as routines written in C and C++.
### Types of System Calls

- Process Control
- File Management
- Device Management
- Information Maintenance
- Protection
- Communication

Typically a number is assigned to each system call and the system call interface maintains a table indexed according to these numbers.
# System boot process

The booting process refers to the sequence of events that occurs when a computer is powered on or restarted, leading to the loading of the OS into memory and preparing the system for use.

1. Power-On Self-Test (POST)
2. Loading the Bootloader
3. Executing the Bootloader
4. Kernel initialization
5. Starting System Services and User Space
6. Displaying the Login Screen / Desktop Environment

**BIOS**: Firmware, or Software associated with hardware
**MBR**: Master Boot Recorder (Old)
**GPT**: GUID Partition Table
## 1) POST

When the computer is turned on, the processor begins executing firmware instructions stored in the Basic Input/Output System (BIOS)

The system performs a hardware check to ensure that all hardware components are working properly.

If an error occurs, the system may display an error message or emit a series of beeps, known as beep code.
## 2) Loading the Bootloader

The BIOS looks for a bootable device.

Locates MBR or GPT.

Bootloader is loaded into memory.
## 3) Executing the Bootloader

The bootloader loads OS kernel into memory.

If multiple OS are installed, the bootloader may present a menu to select between them

Once OS kernel is selected, bootloader passes control to it.
## 4) Kernel initialization

The kernel is loaded into memory.

It initializes system components including:

- Memory Management
- Process Management
- Device Drivers, etc.

The kernel mounts the root file system, which contains the OS environment.
## 5) Starting System Services and User Space

Initialize essential services:

- Networking
- Printing
- Logging

The “init” process executes the start-up script and setup user environment.
## 6) Display the Login Screen / Desktop Env.

System loads GUI and CLI depending on system configuration. User is presented with login screen to enter credentials.