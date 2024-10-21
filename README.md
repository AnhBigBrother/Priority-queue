## heap/priority_queue in typescript  

- push(val: number): push number into the heap.                                     // O(logn)  
- pop(): put the first (max in MaxHeap | min in MinHeap) number out of the heap.    // O(logn)  
- top(): get the first (max in MaxHeap | min in MinHeap) number in the heap.        // O(1)  
- length(): get the length of the heap.                                                                 // O(1)  
- updateByIndex(idx: number, val: number): update the element at index "idx" to value "val"             // O(logn)  
- updateValue(old_val: number, new_val: number): update first element equal to "old_val" to "new_val"   // O(nlogn)  

```
import {MinHeap} from './_heap';  

const pq = new MinHeap()         // pq: []  
pq.push(10)  
pq.push(2)  
pq.push(3)  
pq.push(15)  
pq.push(0)   
pq.push(11)  
pq.push(22)  
pq.push(1)                       // pq: [0, 1, 2, 3, 10, 11, 15, 22]  
pq.pop()                         // pq: [1, 2, 3, 10, 11, 15, 22]  


pq.updateValue(22, 9)            // pq: [1, 2, 3, 9, 10, 11, 15]  

while (pq.length() > 0) {  
	console.log(pq.pop() + " ")    // 1 2 3 9 10 11 15  
}  


```
