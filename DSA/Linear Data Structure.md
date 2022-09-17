### Applications of Stack Data Structure

Although stack is a simple data structure to implement, it is very powerful. The most common uses of a stack are:

-   **To reverse a word** - Put all the letters in a stack and pop them out. Because of the LIFO order of stack, you will get the letters in reverse order.
-   **In compilers** - Compilers use the stack to calculate the value of expressions like `2 + 4 / 5 * (7 - 9)` by converting the expression to prefix or postfix form.
-   **In browsers** - The back button in a browser saves all the URLs you have visited previously in a stack. Each time you visit a new page, it is added on top of the stack. When you press the back button, the current URL is removed from the stack, and the previous URL is accessed.

### Enqueue Operation

-   check if the queue is full
-   for the first element, set the value of FRONT to 0
-   increase the REAR index by 1
-    add the new element in the position pointed to by REAR

### Dequeue Operation

-   check if the queue is empty
-   return the value pointed by FRONT
-   increase the FRONT index by 1
-   for the last element, reset the values of FRONT and REAR to -1

### Applications of Queue

-   CPU scheduling, Disk Scheduling
-   When data is transferred asynchronously between two processes.The queue is used for synchronization. For example: IO Buffers, pipes, file IO, etc
-   Handling of interrupts in real-time systems.
-   Call Center phone systems use Queues to hold people calling them in order.