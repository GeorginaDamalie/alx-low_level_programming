This repository contains a dynamic library named libdynamic.so which includes various C functions, as well as a script for creating a dynamic library called liball.so from all the .c files in the current directory. Additionally, it provides a dynamic library with C functions.

Functions Included in libdynamic.so
The libdynamic.so library contains the following functions. If any of these functions have not been implemented, they exist as empty functions with the correct prototypes:

int _putchar(char c);
int _islower(int c);
int _isalpha(int c);
int _abs(int n);
int _isupper(int c);
int _isdigit(int c);
int _strlen(char *s);
void _puts(char *s);
char *_strcpy(char *dest, char *src);
int _atoi(char *s);
char *_strcat(char *dest, char *src);
char *_strncat(char *dest, char *src, int n);
char *_strncpy(char *dest, char *src, int n);
int _strcmp(char *s1, char *s2);
char *_memset(char *s, char b, unsigned int n);
char *_memcpy(char *dest, char *src, unsigned int n);
char *_strchr(char *s, char c);
unsigned int _strspn(char *s, char *accept);
char *_strpbrk(char *s, char *accept);
char *_strstr(char *haystack, char *needle);

C dynamic library containing the function definitions
Header files containing the function prototypes
Bash script that creates a dynamic library called liball.so from all the .c files that are in the current directory
C dynamic library that contains C functions that can be called from Python
C dynamic library to inject in a giga million program
Bash script to inject the libmask.so library, using LD_PRELOAD, in the giga million program


