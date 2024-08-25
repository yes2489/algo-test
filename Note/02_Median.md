## 중앙값 (Median)
### 중앙값 찾기
 1) 정렬 수행
 2) 배열 크기의 절반에 해당하는 인덱스에 접근해 반환
```java
int median(int[] array){
    int answer = 0;

    Arrays.sort(array);
    
    answer = array[array.length / 2];
}
```
```java
int median(int a, int b, int c) {
		int max = Math.max(Math.max(a, b), c);
		int min = Math.min(Math.min(a, b), c);
		
		// ^ : XOR 연산자, 두 값이 다르면 1 / 같으면 0을 반환
		return a ^ b ^ c ^ max ^ min;
}
```

### 실시간으로 중앙값 찾기 (Running Median)
 - 데이터가 지속적으로 추가/ 삭제될 경우 Heap 이용   
 `Max heap : 최대값`   `Min heap : 최소값`

 - 첫 번째 수는 1개이므로 중앙값은 첫 번째 수
 - 이후 2개 추가 시 현재 중앙값 보다 작은 수 -> max heap에, 현재 중앙값 보다 큰 수 -> min heap에 저장
```java
// max heap과 min heap의 균형이 깨지면 (maxheap.size != minheap.size)   
 if (maxheap.size > minheap.size){
    maxheap.add();
 } else if (maxheap.size < minheap.size){
    minheap.add();0
 }
```

#### 구현
```java
PriorityQueue<Integer> max_heap = new PriorityQueue<>(Collections.reverseOrder());
PriorityQueue<Integer> min_heap = new PriorityQueue<>();
int sum;

max_heap.clear();
min_heap.clear();

sum = 0;

int mid = a;

for(int i = 0; i < 2; i++){
    int b = b;
    if(b > mid){
        min_heap.add(b);
    } else {
        max_heap.add(b);
    }
}

if (max_heap.size() > min_heap.size()){
    int tmp = max_heap.poll();
    min_heap.add(mid);
    mid = tmp;
} else if(min_heap.size() > max_heap.size()){
    int tmp = min_hip.poll();
    max_heap.add(mid);
    mid = tmp;
}
```