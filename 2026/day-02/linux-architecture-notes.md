## The core components of Linux (kernel, user space, init/systemd)

Linux is divided into the **Kernel Space and User Space** and is bridged together at boot time by **systemd**.

**Kernel:** core of the OS that has unrestricted access to hardware. Handles process scheduling, memory management, device drivers, virtual file system, and network stack.

**User Space:** handles user-level programs, services, and applications. Kernel isolates them so if something crashes, it does not crash entire OS. Consists of system libraries (translates code to low-level calls for the kernel), shell and command line, background daemons, and applications



## How processes are created and managed

The kernel invokes **fork()** to copy the **parent process** and create a child process, receiving its own unique PID (process ID).

The **child process** invokes **exec()** to replace its memory space and application code with the new program that needs to be ran.

When Linux boots up, the kernel starts the first process known as **systemd** which always holds a PID of 1. All other processes trace back to this root.

Processes are managed with **process states**



## What systemd does and why it matters

**systemd** is the first process launched by the kernel and stays active until the computer shuts down (PID 1). It starts, stops, and monitors daemons. It handles dependencies, speeds up booting, collects logs, provides core tools, and controls resources. It matters because it is a universal standard across Linux distributions, allows simpler configurations (replaces messy shell scripts), and is reliable (systemd can automatically restart crashed daemons)



## Explain **process states** (running, sleeping, zombie, etc.)

Linux kernel uses **process states** throughout its lifecycle to **manage system resources.**

**TASK_RUNNING (R):** process is actively executing
**TASK_INTERRUPTIBLE (S):** process is blocked (sleeping) while it waits for resource but can wake up early (e.g. kill)
**TASK UNINTERRUPTIBLE (D):** process is blocked (sleeping) and cannot be waken up because it is waiting on critical hardware (network response, disk availability, etc)
**TASK_STOPPED (T):** process is suspended due something like SIGSTOP or Ctrl+Z
**TASK_ZOMBIE (Z):** (defunct) process has finished but entry still remains in system's process table due to parent process needing to read exit status



## List **5 commands** you would use daily

**ls** - lists files in directory
**cd** - change directory
**mkdir** - create folder in directory
**pwd** - print working directory
**cat** - concatenate, lists contents of a text file
**grep** - global regular expression print, prints every line in a file that contains search term (e.g. grep "error" server.log)
**ps** - process status, show status of running processes
**top or htop** - more in depth than ps, shows running processes as well as CPU consumption, memory usage, server health
**kill** - terminates a process

- Keep it **short and practical** (under 1 page)
- Use bullet points and short headings
