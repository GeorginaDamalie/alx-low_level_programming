File Handling Functions in C
This repository contains C functions to perform various file handling operations, including reading a text file, creating a file, appending text to a file, and copying the content of one file to another. Additionally, it includes a program to display information from the ELF header of an ELF file.

Function 1: ssize_t read_textfile(const char *filename, size_t letters)
This function reads a text file and prints its content to the POSIX standard output.

Prototype: ssize_t read_textfile(const char *filename, size_t letters);
Parameters:
filename: The name of the file to be read.
letters: The number of letters to read and print.
Returns:
The actual number of letters read and printed.
If the file cannot be opened or read, it returns 0.
If filename is NULL, it returns 0.
If the write operation fails or does not write the expected amount of bytes, it returns 0.
Function 2: int create_file(const char *filename, char *text_content)
This function creates a new file and writes the provided text content to it.

Prototype: int create_file(const char *filename, char *text_content);
Parameters:
filename: The name of the file to be created.
text_content: A NULL-terminated string to write to the file.
Returns:
1 on success.
-1 on failure (file cannot be created, written, or other errors).
The created file will have permissions rw-------. If the file already exists, its contents will be truncated.

Function 3: int append_text_to_file(const char *filename, char *text_content)
This function appends text at the end of an existing file.

Prototype: int append_text_to_file(const char *filename, char *text_content);
Parameters:
filename: The name of the file to which the text will be appended.
text_content: The NULL-terminated string to add at the end of the file.
Returns:
1 on success.
-1 on failure (file does not exist, or write permissions are not sufficient).
Program: File Copy Utility
This program copies the content of one file to another.

Usage: cp file_from file_to
If the number of arguments is incorrect, the program exits with code 97 and prints Usage: cp file_from file_to on the POSIX standard error.
If the destination file (file_to) already exists, its contents will be truncated.
If the source file (file_from) does not exist or cannot be read, the program exits with code 98 and prints Error: Can't read from file NAME_OF_THE_FILE on the POSIX standard error, where NAME_OF_THE_FILE is the first argument passed to the program.
If the destination file (file_to) cannot be created or writing to it fails, the program exits with code 99 and prints Error: Can't write to NAME_OF_THE_FILE on the POSIX standard error, where NAME_OF_THE_FILE is the second argument passed to the program.
If the program cannot close a file descriptor, it exits with code 100 and prints Error: Can't close fd FD_VALUE on the POSIX standard error, where FD_VALUE is the value of the file descriptor.
The permissions of the created file are set to rw-rw-r--. If the file already exists, its permissions are not changed.
The program reads 1,024 bytes at a time from file_from to minimize system calls, using a buffer.
The program uses dprintf for error messages.
Program: ELF Header Information Display
This program displays the information contained in the ELF header at the start of an ELF file.

Usage: elf_header elf_filename
Displayed Information:
Magic
Class
Data
Version
OS/ABI
ABI Version
Type
Entry point address
The format of the displayed information is the same as readelf -h (version 2.26.1).
If the file is not an ELF file or an error occurs, the program exits with status code 98 and displays a comprehensive error message to stderr.
The program is allowed to use lseek once and read a maximum of 2 times at runtime.
It uses printf to display the information.
The C functions and programs in this repository are designed to provide efficient and reliable file handling capabilities. They can be utilized in various C projects that involve file I/O operations.
