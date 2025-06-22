# String+

**Custom implementation of the `string.h` library with extensions, including `sprintf` functions.**

## Project Overview

This project is a custom implementation of the standard C `string.h` library with additional string manipulation features. The library includes:

- All major functions from the standard `string.h`
- Partial implementation of `sprintf`
- Additional string functions inspired by the C# `String` class

---

## Implemented Functions

### Standard `string.h` Functions

| Function   | Description                            |
|------------|----------------------------------------|
| `memchr`   | Search for the first occurrence of a character |
| `memcmp`   | Compare blocks of memory               |
| `memcpy`   | Copy memory blocks                     |
| `memset`   | Fill memory with a constant byte       |
| `strncat`  | Concatenate strings (with limit)       |
| `strchr`   | Find the first occurrence of a character |
| `strncmp`  | Compare strings (with limit)           |
| `strncpy`  | Copy strings (with limit)              |
| `strcspn`  | Get the length of a segment not containing chars |
| `strerror` | Return string describing error code    |
| `strlen`   | Get string length                      |
| `strpbrk`  | Search for any of a set of characters  |
| `strrchr`  | Find the last occurrence of a character |
| `strstr`   | Locate a substring                     |
| `strtok`   | Tokenize a string                      |

---

### `sprintf` Function

Implemented with support for:

- **Specifiers:** `c`, `d`, `f`, `s`, `u`, `%`
- **Flags:** `-`, `+`, space
- **Width:** numeric value
- **Precision:** `.` followed by number
- **Length modifiers:** `h`, `l`

---

### Additional Functions

| Function    | Description                        |
|-------------|------------------------------------|
| `to_upper`  | Convert string to uppercase        |
| `to_lower`  | Convert string to lowercase        |
| `insert`    | Insert a substring into a string   |
| `trim`      | Remove leading/trailing characters |

---

## Project Structure

```text
s21_string/
├── Makefile             # Build script
├── s21_string.h         # Main header file
├── s21_sprintf.h        # Header for sprintf
├── s21_memchr.c         # Implementation of memchr
├── s21_memcmp.c         # Implementation of memcmp
├── s21_memcpy.c         # Implementation of memcpy
├── s21_memset.c         # Implementation of memset
├── s21_strncat.c        # Implementation of strncat
├── s21_strchr.c         # Implementation of strchr
├── s21_strncmp.c        # Implementation of strncmp
├── s21_strncpy.c        # Implementation of strncpy
├── s21_strcspn.c        # Implementation of strcspn
├── s21_strerror.c       # Implementation of strerror
├── s21_strlen.c         # Implementation of strlen
├── s21_strpbrk.c        # Implementation of strpbrk
├── s21_strrchr.c        # Implementation of strrchr
├── s21_strstr.c         # Implementation of strstr
├── s21_strtok.c         # Implementation of strtok
├── s21_to_upper.c       # Implementation of to_upper
├── s21_to_lower.c       # Implementation of to_lower
├── s21_insert.c         # Implementation of insert
├── s21_trim.c           # Implementation of trim
├── s21_sprintf.c        # Implementation of sprintf
├── s21_sprintf_parser.c # Format parser for sprintf
├── s21_sprintf_buf.c    # Buffer management for sprintf
└── tests/
    └── test_s21_string.c # Unit tests
```

---

## Requirements

- GCC compiler (C11 standard support)
- Check library for unit testing
- Supported systems: Linux, macOS

---

## Build and Test Instructions

### Build the library
```bash
make s21_string.a
```

### Run tests
```bash
make test
```

### Generate coverage report
```bash
make gcov_report
```

### Clean the project
```bash
make clean
```

---

## Implementation Highlights

- Full compliance with the C11 standard  
- Follows **Google C Style Guide**  
- Static code analysis  
- Unit test coverage >80%  
- Cross-platform support (Linux and macOS)  
- Robust error handling  
- Optimized string processing algorithms  

---

### Design Priorities

- Efficient memory management  
- Accurate edge case handling  
- Behavioral compatibility with standard library functions  
- Code readability and maintainability  

All functions are implemented **without using the standard `string.h`**, ensuring full independence from system libraries.
