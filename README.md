# Queue
## Overview

This repository contains two implementations of a Queue:
1. **Queue Implementation Using Array**
2. **Queue Implementation Using C++ STL (Standard Template Library)**

A queue is a linear data structure that follows the First-In-First-Out (FIFO) principle, meaning the element inserted first will be the first to be removed. Queues are commonly used in many real-life applications like scheduling tasks, handling requests in web servers, or managing processes in operating systems.

## Advantages of Queues in C++:
- **FIFO Structure:** The First-In-First-Out nature of queues is essential in scenarios like task scheduling, resource management, and processing requests in the order they arrive.
- **Efficient Enqueue and Dequeue Operations (O(1)):** The constant time complexity for enqueueing and dequeueing makes queues highly efficient for sequential data processing.
- **Dynamic Memory Management (Using STL):** The dynamic memory management provided by C++'s STL queue eliminates concerns over memory overflow, making it easier to work with growing or shrinking data without manual resizing.
- **Real-time Applications:** Queues are critical in real-time systems such as operating systems (task scheduling) and networking (packet management), ensuring proper order of execution.

## Disadvantages of Queues in C++:
- **No Random Access:** The inability to directly access or modify elements in the middle or at arbitrary positions limits the flexibility of queues, especially when compared to data structures like arrays or vectors.
- **Fixed Size (In Array-based Implementations):** In array-based implementations, the fixed size can lead to overflow problems if the queue exceeds its capacity, which introduces inefficiency when resizing is necessary.
- **Inefficient Deletion in Array Implementations:** Deleting elements from an array-based queue can be inefficient due to the need for shifting elements, which takes linear time (O(n)).
- **Memory Overhead in Linked List Implementation:** Linked list-based queues introduce additional memory overhead because each node requires extra memory for pointers.

## Queue Implementations

### 1. Queue Implementation Using Array

**Description:**

In this approach, a queue is manually implemented using an array. We maintain two pointers, `front` and `rear`, to keep track of the first and last elements in the queue, respectively. The queue supports the following operations:
- `Enqueue`: Adds an element to the rear of the queue.
- `Dequeue`: Removes the element from the front of the queue.
- `Display`: Displays the elements currently in the queue.
- `isFull` and `isEmpty`: Checks if the queue is full or empty.

**Algorithm:**

1. **Enqueue Operation:**
   - Check if the queue is full by checking if `rear == size - 1`.
   - If not full, increment `rear` and insert the new element at `arr[rear]`.
   - If the queue is initially empty (`front == -1`), set `front = 0`.

2. **Dequeue Operation:**
   - Check if the queue is empty by checking if `front == -1` or `front > rear`.
   - If not empty, remove the element at `arr[front]` and increment `front`.
   - If after removal, `front` exceeds `rear`, reset both `front` and `rear` to -1.

3. **Display Operation:**
   - Traverse the queue from `front` to `rear` and print each element.

**Time Complexity:**
- Enqueue: O(1)
- Dequeue: O(1)
- Display: O(n)

### 2. Queue Implementation Using C++ STL

**Description:**

The C++ Standard Template Library (STL) provides a built-in `queue` class which simplifies queue operations. This implementation handles everything internally, allowing us to focus on high-level operations. The `queue` class provides the following member functions:
- `push`: Adds an element to the rear of the queue.
- `pop`: Removes an element from the front.
- `front`: Returns the element at the front of the queue.
- `back`: Returns the element at the rear of the queue.
- `empty`: Checks if the queue is empty.

**Algorithm:**

1. **Enqueue Operation (push):**
   - Use `q.push(value)` to insert an element at the rear of the queue.

2. **Dequeue Operation (pop):**
   - Use `q.pop()` to remove the front element from the queue.

3. **Access Front and Rear:**
   - Use `q.front()` to get the element at the front.
   - Use `q.back()` to get the element at the rear.

4. **Check If Queue is Empty:**
   - Use `q.empty()` to check if the queue has no elements.

**Time Complexity:**
- Enqueue: O(1)
- Dequeue: O(1)
- Access front/back: O(1)
