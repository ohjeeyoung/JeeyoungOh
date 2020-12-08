## 정렬(Sort)


1. 선택정렬(Selection Sort)
> 선택정렬은 리스트에서 아직 정렬 안된 부분의 원소들 중에서 최솟값을 '선택'하여 정렬 안된 부분의
> 가장 왼쪽의 원소와 교환하는 정렬 알고리즘

```python
# 선택 정렬

def selection_sort(a):
    for i in range(0, len(a)-1):
        minimum = i
        for j in range(i, len(a)):
            if a[minimum] > a[j]:
                minimum = j
        a[i], a[minimum] = a[minimum], a[i]

a = [54, 88, 77, 26, 93, 17, 49, 10, 17, 77, 11, 31, 22, 44, 17, 20]

selection_sort(a)
print(a)
```
- Time Complexity

(N-1) + (N-2) + ... + 2 + 1 = N(N-1)/2 = O(N^2)

- 공간복잡도 

주어진 배열 안에서 교환(swap)을 통해 정렬이 수행되므로 O(n)

- 특징

항상 O(N^2) 수행시간이 소요

입력에 민감하지 않은(Input Insensitive) 알고리즘

불안정 정렬(Unstable Sort)

2. 삽입정렬(Insertion Sort)
> 삽입정렬은 리스트가 정렬된 부분과 정렬 안된 부분으로 나뉘며,
> 정렬 안된 부분의 가장 왼쪽 원소를 정렬된 부분에 '삽입'하는 방식의 정렬 알고리즘

```python
# 삽입정렬

def insertion_sort(a):
    for i in range(1, len(a)):
        for j in range(i, 0, -1):
            if a[j-1] > a[j]:
                a[j], a[j-1] = a[j-1], a[j]

a = [54, 88, 77, 26, 93, 17, 49, 10, 17, 77, 11, 31, 22, 44, 17, 20]

insertion_sort(a)
print(a)
```

- Time Complexity

입력이 이미 정렬된 경우: N-1번

Worst Case: 1 + 2 + ... + (N-2) + (N-1) = N(N-1)/2 = O(N^2)

- 공간복잡도

주어진 배열 안에서 교환(swap)을 통해 정렬이 수행되므로 O(n)

- 특징

입력에 민감한(Input Sensitive) 알고리즘

안정 정렬(Stable Sort)

Worst Case: 선택정렬 > 삽입정렬

입력 크기가 작은 경우, 거의 정렬이 되어있는 경우에는 매우 좋은 성능을 보임

-> 재귀호출을 하지 않으며, 프로그램도 간단하기 때문


3. 힙정렬(Heap Sort)
> 힙정렬은 최대힙을 이용하여 루트를 힙의 가장 마지막 노드와 교환한 후 힙 크기를 1 감소시키고,
> 루트로부터 downheap 연산으로 힙 속성을 복원하는 과정을 반복하여 정렬하는 알고리즘

```python
# 힙정렬


```

- Time Complexity


- 공간복잡도


- 특징