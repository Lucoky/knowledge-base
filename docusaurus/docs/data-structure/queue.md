---
sidebar_position: 4
---

# Queues

A queue is a linear data structure that follows the First In First Out (FIFO)
principle. In a queue, elements are inserted at the back (rear) and removed 
from the front (front). The element that is inserted first is the first one 
to be removed. 

Queues are very common in programming, they are use in many algorithms 
and also in architecture of systems. You can find queues in many places, like 
enqueue process, print queues, etc...

For architecture, normally all the service providers have a queue to manage 
like azure, aws, etc...

For data structures, normally you can use a list or an array to implement them.

## Enqueue Operation

The enqueue operation adds an element to the back of the queue. The element 
is added to the rear of the queue, and the rear pointer is incremented to 
point to the new rear element.

## Dequeue Operation 

The dequeue operation removes the front element from the queue.

## Algorithms

Some common algorithms that use queues include:

- Breadth First Search (BFS)
- Level Order Traversal of a Binary Tree
- Implementing a Queue using Stacks
- Sliding Window Maximum

## Implementation

Here is an example of a queue implementation in C#:

```csharp
using System;

public class Queue
{
    private int[] arr;
    private int front;
    private int rear;
    private int capacity;

    public Queue(int size)
    {
        arr = new int[size];
        capacity = size;
        front = 0;
        rear = -1;
    }

    public void Enqueue(int x)
    {
        if (IsFull())
        {
            Console.WriteLine("Queue Overflow");
            return;
        }

        arr[++rear] = x;
    }

    public int Dequeue()
    {
        if (IsEmpty())
        {
            Console.WriteLine("Queue Underflow");
            return -1;
        }

        int x = arr[front];
        front++;
        return x;
    }

    public bool IsEmpty()
    {
        return front > rear;
    }

    public bool IsFull()
    {
        return rear == capacity - 1;
    }
}
```

## Complexity

The time complexity of the enqueue and dequeue operations in a queue is O(1).
