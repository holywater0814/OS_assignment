# LAB ASSIGNMENT (PAS078BEI003)

## Question: Describe and discuss the use case of the following:

# Explanation of System Calls in Operating Systems

System calls provide the interface between a process and the operating system. They allow user-level processes to request services of the operating system. Here we discuss several important system calls and their use cases.

## 1. fork()
The `fork()` system call is used to create a new process. The new process created by `fork()` is called the child process, and the process that invoked `fork()` is the parent process. The child process is a copy of the parent process, except for different PID and PPID. Both processes will execute the next instruction following the `fork()` system call.

### Use Case:
- Used in implementing multitasking in an operating system.
- Used by a shell to execute commands by creating a new process.

## 2. exec()
The `exec` family of functions replaces the current process image with a new process image. The new process image is constructed from a regular, executable file. This means the current process will terminate, and a new program will run in its place.

### Use Case:
- Commonly used after `fork()` to run a different program in the child process.
- Used to start a new program from within a running program.

## 3. getpid()
The `getpid()` function returns the process ID (PID) of the calling process. It is used to retrieve the unique identifier of the calling process.

### Use Case:
- Useful for logging and debugging to identify which process is running.
- Helps in creating unique temporary file names or generating unique keys for IPC (Inter-Process Communication).

## 4. wait()
The `wait()` system call makes a parent process wait until all of its child processes have terminated. It also returns the PID of the terminated child, and its exit status.

### Use Case:
- Ensures that the parent process executes only after the child process has finished execution.
- Used to clean up the terminated child processes and release resources.

## 5. stat()
The `stat()` system call retrieves information about a file or directory. The information includes file size, permissions, owner, modification times, etc., and is stored in a structure.

### Use Case:
- Used in file management utilities to display file information.
- Helps in implementing commands like `ls`, which lists the details of files and directories.

## 6. opendir()
The `opendir()` function opens a directory stream corresponding to the directory name, and returns a pointer to the directory stream. The directory stream is used to read directory entries.

### Use Case:
- Used in programs that need to read the contents of a directory.
- Helps in implementing file managers and backup utilities.

## 7. readdir()
The `readdir()` function reads the next entry from the directory stream referred to by the `DIR` pointer returned by `opendir()`. It returns a pointer to a `dirent` structure representing the directory entry.

### Use Case:
- Used to iterate through all the entries in a directory.
- Helps in implementing directory listing commands like `ls`.

## 8. close()
The `close()` system call closes a file descriptor, so that it no longer refers to any file and may be reused. This is essential for releasing system resources.

### Use Case:
- Essential in all programs that open files or sockets to ensure resources are released after use.
- Prevents resource leaks in long-running programs.

System calls are crucial for performing operations that require direct communication with the kernel and hardware, making them an integral part of system programming.

