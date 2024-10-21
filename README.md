# heap/priority_queue in typescript  

| Method                          | Description                                                                             | Time complexity |
|-------------------------------- | --------------------------------------------------------------------------------------- | --------------- |
| push(item)                      | push item into the heap.                                                                | O(logn)         |
| pop()                           | put the first (max priority in MaxHeap / min priority in MinHeap) item out of the heap. | O(logn)         |
| top()                           | get the first (max priority in MaxHeap / min priority in MinHeap) item in the heap.     | O(1)            |
| length()                        | get the length of the heap.                                                             | O(1)            |
| updateByIndex(idx, item)        | update the element at index "idx".                                                      | O(logn)         |
| updateValue(old_item, new_item) | update first element equal to "old_item" to "new_item" (only in MaxHeap or MinHeap).    | O(nlogn)        |

**heap:**

``` typescript
import {MinHeap} from './_heap';  

const h = new MinHeap()         // h: []  
h.push(10)  
h.push(2)  
h.push(3)  
h.push(15)  
h.push(0)   
h.push(11)  
h.push(22)  
h.push(1)                       // h: [0, 1, 2, 3, 10, 11, 15, 22]  
h.pop()                         // h: [1, 2, 3, 10, 11, 15, 22]  


h.updateValue(22, 9)            // h: [1, 2, 3, 9, 10, 11, 15]  

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

const pq = new PriorityQueue<string>("MIN_HEAP")
pq.push("bro", 1)
pq.push("foo", 2)
pq.push("bar", 5)
pq.push("dummy", 4)
pq.push("wololo", 2)

while (pq.length() > 0) {
  console.log(pq.pop())
}  
/* output: 
{ value: 'bro', priority: 1 }
{ value: 'wololo', priority: 2 }
{ value: 'foo', priority: 2 }
{ value: 'dummy', priority: 4 }
{ value: 'bar', priority: 5 }
*/
```
