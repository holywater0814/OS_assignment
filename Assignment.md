# LAB ASSIGNMENT (PAS078BEI003)

## Question: Describe and discuss the use case of the following:

### 1. fork()
The `fork()` system call is a fundamental operation in operating systems used to create a new process by duplicating the calling process. The new process is called the child process, while the calling process is referred to as the parent process. `fork()` is used to create a new process that runs concurrently with the parent process. After the new child process is created, both processes will execute the next instruction following the `fork()` system call.

### 2. exec()
The `exec` family of functions is used to run an executable file in the context of an already existing process, replacing the previous executable. This means that when the `exec` function is used, the current process terminates, and a new process starts, effectively replacing the current process's image with a new one.

### 3. getpid()
The `getpid()` function is used to retrieve the process ID (PID) of the calling process. It is a simple function that does not take any arguments. When a parent process creates a child process using `fork()`, it can use `getpid()` to get the PID of the child process and `getppid()` to get the parent process ID, helping in managing and coordinating between the two processes.

### 4. wait()
The `wait()` function is used by a parent process to wait for its child processes to terminate. When a parent process calls `wait()`, it pauses execution until one of its child processes exits or a signal is received. This is useful in scenarios where a parent process spawns multiple child processes, as `wait()` helps manage the lifecycle of each child process by waiting for their termination one by one.

### 5. stat()
The `stat()` function is used to retrieve information about a file or directory, providing details such as the file's size, permissions, owner, and timestamps. This function is commonly used in file management and system programming to retrieve the status of a file and store it in a structure containing various fields representing different attributes of the file.

### 6. opendir()
The `opendir()` function is used to open a directory stream, which can then be used to read the contents of the directory using functions like `readdir()` and to close the directory stream with `closedir()`. `opendir()` is commonly used in utilities that need to manage or analyze directory contents, such as backup tools, file managers, or custom scripts.

### 7. readdir()
The `readdir()` function is used to read directory entries from a directory stream opened with `opendir()`. It allows you to iterate through the contents of a directory and retrieve information about each file or subdirectory within it.

### 8. close()
The `close()` function is used to close a file descriptor, which is an integer handle used by the operating system to identify an open file, socket, or other I/O resource. Closing a file descriptor releases the associated resources and marks it as no longer in use.
