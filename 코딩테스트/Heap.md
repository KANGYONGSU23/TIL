## 힙(HEAP)

**최솟값**, **최대값**을 빠르게 찾기 위해 고완된 자료형 우선순위 큐를 위해 만들어졌다.

각 노드의 키값이 그 자식의 키 값보다 크거나(최대 힙), 작은(최소 힙) **완전 이진 트리**이다.

**힙에서의 부모 자식 관계**

- 부모의 인덱스 = (자식의 인덱스) / 2
- 왼쪽 자식의 인덱스 = (부모의 인덱스) * 2
- 오른쪽 자식의 인덱스 = (부모의 인덱스) * 2+1

! 코드로 구현 시에 0번 인덱스부터 시작하기 때문에 이 경우에는 식이 변할 수 있다

![image](https://github.com/KANGYONGSU23/TIL/assets/101508006/d9b07cc0-dd52-44d1-83b7-628b475fa246)


```js
class Heap {
    constructor() {
        this.heap = [];
    }
    
    size() {
        return this.heap.length;
	  }
    
    swap(idx1, idx2) {
			  //두 개의 노드를 서로 바꾸기
        [this.heap[idx1], this.heap[idx2]] = [this.heap[idx2], this.heap[idx1]];
    }
    
    add(value) {
        this.heap.push(value);
        this.bubbleUp();
    }
    
    bubbleUp() {
        let index = this.heap.length - 1;
        //부모인덱스 = 자식IDX / 2
        let parent = Math.floor((index - 1) / 2);
        ///부모 노드가 존재하고 부모 노드가 자식 노드보다 더 크다면
        while(this.heap[parent] && this.heap[parent] > this.heap[index]) {
            this.swap(index, parent);
            index = parent;
            parent = Math.floor((index - 1) / 2);
        }
    }
    
    poll() {
        if(this.heap.length === 1){
            return this.heap.pop();
        }
        
        const value = this.heap[0];              
        this.heap[0] = this.heap.pop();
        this.bubbleDown();
        return value;
    }
    
    bubbleDown() {
        let index = 0;
        let leftChildIdx = index * 2 + 1;
        let rightChildIdx = index * 2 + 2;
        
        while(
		        //왼쪽 노드가 존재하고 부모 노드보다 작거나
		        //오르쪽 노드가 존재하고 부모 노드보다 작다면
            (this.heap[leftChildIdx] && this.heap[leftChildIdx] < this.heap[index]) || 
            (this.heap[rightChildIdx] && this.heap[rightChildIdx] < this.heap[index])
        ) {
            let smallerIdx = leftChildIdx;
            //오른쪽 노드가 존재하고 왼쪽 노드보다 작다면 오른쪽 인덱스를 smallerIdx로 할당
            if(this.heap[rightChildIdx] && this.heap[rightChildIdx] < this.heap[smallerIdx]) {
                smallerIdx = rightChildIdx;
            }
            
            this.swap(index, smallerIdx);
            index = smallerIdx;
            leftChildIdx = index * 2 + 1;
            rightChildIdx = index * 2 + 2;
        }
    }
}
```
