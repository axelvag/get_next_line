# Get_next_line

42 project:

There are 2 versions of this project: With and without the bonuses.

I advise you to compile the one with _bonus to have all the functionality of my gnl.

 The goal of the project is to write a C function that allows you to read a line (up to a newline) from a file descriptor, and return it each time the function is called.

Here is a brief description of the project and its requirements:
Objective of the project :

The main purpose of get_next_line is to allow reading a line terminated by an end-of-line character ('\n') from a given file descriptor (e.g., a file, an input stream, or even the standard input).
Constraints and Requirements:

   - Use of System Functions: Students should use only standard system functions allowed by the statement, such as read, malloc, and free.

   - Memory Management: Memory management is crucial. Students must allocate and free memory correctly to avoid memory leaks.

   - Reentrancy: The get_next_line function must be able to process multiple file descriptors simultaneously without losing state between calls.

   - Advanced Features (Bonus): Advanced features can be added as bonuses, such as handling multiple file descriptors simultaneously, handling other end-of-line characters, etc.

   - Standard 42: The code must comply with school-specific coding standard 42.

Typical Use:

```c

#include "get_next_line.h"

int main() {
    int fd;
    char *line;

    fd = open("exemple.txt", O_RDONLY);
    while (get_next_line(fd, &line) > 0) {
        printf("%s\n", line);
        free(line);
    }
    close(fd);
    return (0);
}
```

Key points :

   The get_next_line function must be able to handle progressive reading of a file until the end of the file.
   It must be able to handle reading several files simultaneously without conflicts.

Successfully completing this project requires a thorough understanding of C input/output operations, memory management, and file manipulation.
