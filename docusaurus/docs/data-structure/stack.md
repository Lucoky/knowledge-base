---
sidebar_position: 3
---

# Stacks

The stack is a linear data structure that follows the Last In First Out 
(LIFO) principle. It has two main operations: push and pop. The push 
operation adds an element to the top of the stack, and the pop operation 
removes the top element from the stack. Most programming languages have 
already a Stack data structure implemented, if that is not the case, you can often use a List or an Array to implement a Stack.

## Push Operation

The push operation adds an element to the top of the stack. The element is added to the top of the stack, and the stack pointer is incremented to point to the new top element.

## Pop Operation

The pop operation removes the top element from the stack. The element is removed from the top of the stack, and the stack pointer is decremented to point to the new top element.

## Algorithms

Some common algorithms that use stacks include:

- Infix to Postfix conversion
- Postfix expression evaluation
- Balanced parentheses

## Implementation

Here is an example of a stack implementation in C#:

```csharp
using System;

public class Stack
{
    private int[] arr;
    private int top;
    private int capacity;

    public Stack(int size)
    {
        arr = new int[size];
        capacity = size;
        top = -1;
    }

    public void Push(int x)
    {
        if (IsFull())
        {
            Console.WriteLine("Stack Overflow");
            return;
        }

        arr[++top] = x;
    }

    public int Pop()
    {
        if (IsEmpty())
        {
            Console.WriteLine("Stack Underflow");
            return -1;
        }

        return arr[top--];
    }

    public int Peek()
    {
        if (IsEmpty())
        {
            Console.WriteLine("Stack is Empty");
            return -1;
        }

        return arr[top];
    }

    public bool IsEmpty()
    {
        return top == -1;
    }

    public bool IsFull()
    {
        return top == capacity - 1;
    }
}
```

## Complexity

The time complexity of the push and pop operations in a stack is O(1).


