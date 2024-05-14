# Circular Structure with Sentinel Node

## Overview
This project encompasses a comprehensive implementation of a circular doubly-linked list in C, featuring a sentinel node to streamline node manipulation processes. The implementation is designed to facilitate efficient operations such as insertion, deletion, traversal, and searching within the list, ensuring high performance and scalability for applications requiring dynamic data management.

## Preparing the Development Environment

### File Setup
Download the `list.c`, `list.h`, and `Makefile` into a secure folder on your development machine accessible only to you.

### Dependencies
Ensure you have the following tools installed:
- GCC compiler (`clang` on macOS)
- Standard C library


## Key Features

- **Sentinel Node**: Simplifies edge cases such as inserting or deleting at the boundaries, using a sentinel node at both the start and end of the list.
- **Circular Structure**: Ensures the last node points back to the sentinel, allowing seamless forward and backward traversal.
- **Dynamic Node Management**: Supports dynamic addition and removal of nodes. Each node holds data and two pointers to link with adjacent nodes.
- **Robust Error Handling**: Provides stability through checks to prevent memory leaks and handle null-pointer situations.
- **Efficiency**: Operations are designed to be constant time \(O(1)\), suitable for real-time applications.


## Implementation Details

### Structures
- `struct node`: Represents the list nodes, containing an integer data field and two pointers (`next` and `prev`).
- `struct list`: Represents the entire list, including a pointer to the sentinel node and other metadata like list size.

### Core Functions
- `newList()`: Initializes a new list with a sentinel node.
- `insertAfter()`, `insertBefore()`: Inserts nodes relative to the current node.
- `deleteNode()`: Removes a node from the list.
- `moveNext()`, `movePrev()`: Moves the current node pointer within the list.
- `freeList()`: Deallocates all nodes in the list, including the sentinel.


## Compilation and Usage
Compile the program using the following command, which includes flags for strict type checking and debugging:
```bash
clang -std=c11 -Wall -pedantic -g -fsanitize=undefined -fsanitize=address list.c -o list_program
```

This implementation is a robust foundation for applications that require efficient and dynamic data management, demonstrating advanced memory and pointer management techniques in C.
