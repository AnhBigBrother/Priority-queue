# heap/priority_queue

Heap & priority queue implementation in TypeScript.

## Usage

| Method                          | Description                                                                             | Time complexity |
|-------------------------------- | --------------------------------------------------------------------------------------- | --------------- |
| push()                          | push item into the heap.                                                                | O(logn)         |
| pop()                           | put the first (max priority in MaxHeap / min priority in MinHeap) item out of the heap. | O(logn)         |
| top()                           | get the first (max priority in MaxHeap / min priority in MinHeap) item in the heap.     | O(1)            |
| length()                        | get the length of the heap.                                                             | O(1)            |
| updateByIndex()                 | update the element at a specified index of the heap.                                    | O(logn)         |
| updateByValue()                 | update the first element in the heap with the value "old_val" to "new_val".             | O(nlogn)        |

## Example

**heap:**

``` typescript
import {MinHeap} from './_heap';  

const h = new MinHeap()         // h.heap: []  
h.push(10)  
h.push(2)  
h.push(3)  
h.push(15)  
h.push(0)   
h.push(11)  
h.push(22)  
h.push(1)                       // h.heap: [0, 1, 3, 2, 10, 11, 22, 15]  
h.pop()                         // h.heap: [1, 2, 3, 15, 10, 11, 22]  


h.updateByValue(22, 9)            // h.heap: [1, 2, 3, 15, 10, 11, 9]  

while (h.length() > 0) {  
  console.log(h.pop())         
}  
/* output: 
1 
2 
3 
9 
10 
11 
15 
*/
```

**priority queue:**

``` typescript
import {PriorityQueue} from './_priority_queue';  

const pq = new PriorityQueue<string>((x, y) => x - y) // Max_Queue
pq.push("bro", 1)
pq.push("foo", 2)
pq.push("bar", 5)
pq.push("dummy", 4)
pq.push("wol", 2)

pq.updateByValue("wol", "wololo", 3)

while (pq.length() > 0) {
  console.log(pq.pop())
}
/* output: 
{ value: 'bar', priority: 5 }
{ value: 'dummy', priority: 4 }
{ value: 'wololo', priority: 3 }
{ value: 'foo', priority: 2 }
{ value: 'bro', priority: 1 }
*/
```
