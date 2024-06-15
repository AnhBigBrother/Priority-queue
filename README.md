## Priority queue data structure in TypeScript and JavaScript  

Useful utility class for solving heap/priority_queue problems.  

- push(): push number into queue.                           // O(logn)  
- pop(): put the last (biggest) element out of the queue.   // O(1)  
- toArray(): convert queue into an array.                   // O(n)  
- top(): get the last (biggest) number in the queue.        // O(1)  
- front(): get the first (smallest) number in the queue.    // O(1)  
- length(): get the length of the queue.                    // O(1)  

```
import PriorityQueue from './__PriorityQueue';  

const myPQueue = new PriorityQueue()
myPQueue.push(1, 4, 5, 3, 0, 2, 8, -1, -7);
console.log('myPQueue:', myPQueue.toArray());    // myPQueue: [-7, -1, 0, 1, 2, 3,  4, 5, 8]
console.log('length:', myPQueue.length());       // length: 9
console.log('front:', myPQueue.front());         // front: -7
console.log('top:', myPQueue.top());             // top: 8

myPQueue.pop();
myPQueue.pop();
console.log(myPQueue.toArray());                 // myPQueue: [-7, -1, 0, 1, 2,  3, 4]
myPQueue.push(3);
console.log(myPQueue.toArray());                 // myPQueue: [-7, -1, 0, 1, 2,  3, 3, 4]

```
