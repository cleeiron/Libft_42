# Libft

*This project has been created as part of the 42 curriculum by clpincho.*

## Description

**Libft** is a project from the 42 curriculum that consists of creating a personal C library by reimplementing standard C library functions and developing additional utility functions.

The goal of this project is to gain a deeper understanding of C programming, memory management, pointers, strings, and linked lists.

The library is compiled into a static archive named `libft.a`, which can be reused in future C projects.

The project is divided into three parts:

- **Part 1 – Libc functions:** Reimplementation of standard C library functions.
- **Part 2 – Additional functions:** Implementation of useful functions for string manipulation, memory allocation, and file descriptor output.
- **Bonus – Linked lists:** Implementation of functions to create, manipulate, iterate through, and free linked lists.

## Instructions

### Compilation

Clone the repository and enter the project directory:

```bash
git clone <repository_url>
cd libft
```

Compile the library using:

```bash
make
```

This command generates the static library `libft.a`.

To compile the bonus functions:

```bash
make bonus
```

Other available Makefile commands:

| Command | Description |
|---|---|
| `make` | Compiles the mandatory library |
| `make bonus` | Compiles the library with bonus functions |
| `make clean` | Removes object files |
| `make fclean` | Removes object files and `libft.a` |
| `make re` | Recompiles the library from scratch |

### Usage

Include the `libft.h` header in your C program:

```c
#include "libft.h"
```

Example:

```c
#include "libft.h"

int main(void)
{
    char *str;

    str = ft_strdup("Hello, 42!");
    if (!str)
        return (1);
    ft_putendl_fd(str, 1);
    free(str);
    return (0);
}
```

Compile your program with the library:

```bash
cc -Wall -Wextra -Werror main.c libft.a -o program
```

Then execute:

```bash
./program
```

## Implemented Functions

### Part 1 – Libc Functions

| Category | Functions |
|---|---|
| Character checks | `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint` |
| Character conversion | `ft_toupper`, `ft_tolower` |
| String manipulation | `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`, `ft_strdup` |
| Memory manipulation | `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, `ft_calloc` |
| Conversion | `ft_atoi` |

### Part 2 – Additional Functions

| Function | Description |
|---|---|
| `ft_substr` | Extracts a substring from a string |
| `ft_strjoin` | Concatenates two strings into a new string |
| `ft_strtrim` | Removes specified characters from both ends of a string |
| `ft_split` | Splits a string using a delimiter |
| `ft_itoa` | Converts an integer into a string |
| `ft_strmapi` | Applies a function to each character of a string |
| `ft_striteri` | Applies a function to each character by reference |
| `ft_putchar_fd` | Writes a character to a file descriptor |
| `ft_putstr_fd` | Writes a string to a file descriptor |
| `ft_putendl_fd` | Writes a string followed by a newline |
| `ft_putnbr_fd` | Writes an integer to a file descriptor |

### Bonus – Linked List Functions

The bonus part introduces singly linked lists using the `t_list` structure.

| Function | Description |
|---|---|
| `ft_lstnew` | Creates a new list node |
| `ft_lstadd_front` | Adds a node at the beginning of a list |
| `ft_lstsize` | Counts the number of nodes |
| `ft_lstlast` | Returns the last node |
| `ft_lstadd_back` | Adds a node at the end of a list |
| `ft_lstdelone` | Deletes a single node |
| `ft_lstclear` | Deletes and frees an entire list |
| `ft_lstiter` | Applies a function to each node's content |
| `ft_lstmap` | Creates a new list by applying a function to each node's content |

## Resources

The following resources are useful for understanding the concepts covered in this project:

- [C language reference – cppreference](https://en.cppreference.com/w/c)
- [Linux manual pages](https://man7.org/linux/man-pages/)
- [GNU Make documentation](https://www.gnu.org/software/make/manual/)
- [42 Norm documentation](https://github.com/42School/norminette)

The main concepts studied include:

- Memory allocation and deallocation
- Pointer manipulation
- String and memory operations
- Static libraries and Makefiles
- Singly linked lists
- Defensive programming and edge-case handling

### AI Usage

AI assistance was used to help structure and write this README file, including organizing the project documentation and improving its clarity.

The implementation of the library functions should be understood and explained independently, in accordance with the project's learning objectives.

## Author

**clpincho** – 42 School