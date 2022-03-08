## 문제 설명

배열 array의 i번째 숫자부터 j번째 숫자까지 자르고 정렬했을 때, k번째에 있는 수를 구하려 합니다.

예를 들어 array가 [1, 5, 2, 6, 3, 7, 4], i = 2, j = 5, k = 3이라면

1. array의 2번째부터 5번째까지 자르면 [5, 2, 6, 3]입니다.
2. 1에서 나온 배열을 정렬하면 [2, 3, 5, 6]입니다.
3. 2에서 나온 배열의 3번째 숫자는 5입니다.

배열 array, [i, j, k]를 원소로 가진 2차원 배열 commands가 매개변수로 주어질 때, commands의 모든 원소에 대해 앞서 설명한 연산을 적용했을 때 나온 결과를 배열에 담아 return 하도록 solution 함수를 작성해주세요.

### 제한 사항

- array의 길이는 1 이상 100 이하입니다.
- array의 각 원소는 1 이상 100 이하입니다.
- commands의 길이는 1 이상 50 이하입니다.
- commands의 각 원소는 길이가 3입니다.

### 입출력 예

|array|commands|return|
|--|--|--|
|[1, 5, 2, 6, 3, 7, 4]|[[2, 5, 3], [4, 4, 1], [1, 7, 3]]|[5, 6, 3]|

### 입출력 예 설명

[1, 5, 2, 6, 3, 7, 4]를 2번째부터 5번째까지 자른 후 정렬합니다. [2, 3, 5, 6]의 세 번째 숫자는 5입니다.
[1, 5, 2, 6, 3, 7, 4]를 4번째부터 4번째까지 자른 후 정렬합니다. [6]의 첫 번째 숫자는 6입니다.
[1, 5, 2, 6, 3, 7, 4]를 1번째부터 7번째까지 자릅니다. [1, 2, 3, 4, 5, 6, 7]의 세 번째 숫자는 3입니다.

## 학습한 풀이 1

### Code
``` java
public int[] solution(int[] array, int[][] commands) {
		int[] answer = new int[commands.length];
		for (int i = 0; i < commands.length; i++) {
			int[] temp = Arrays.copyOfRange(array, commands[i][0] - 1, commands[i][1]);
			Arrays.sort(temp);
			answer[i] = temp[commands[i][2] - 1];
		}
		return answer;
	}
```

### Arrays.sort(Object[])
정의: 배열 원소 타입의 비교 기준에 따라, 해당 배열을 오름차순으로 정렬한다.
#### Arrays.sort(String[]) 예시
##### Code
``` java
String[] arr = {"Apple", "Kiwi", "Orange", "Banana", "Watermelon", "Cherry"};
Arrays.sort(arr);
System.out.println("Sorted arr[] : " + Arrays.toString(arr));
```

#### Output
```Sorted arr[] : [Apple, Banana, Cherry, Kiwi, Orange, Watermelon]```

### Arrays.copyOfRange(object[], int from, int to)
정의: Object[] 배열에서 from 부터 to 까지의 원소를 갖는 배열을 복사한다.</br>
참고). to 값이 object[]의 크기보다 크다면, default(int: 0) 값을 포함하여 복사한다.
#### Code
``` java
public static void main(String[] args) {
	int[] arr1 = { 1, 2, 3, 4, 5 };
	System.out.print("arr1 >>");
	for (int i = 0; i < arr1.length; i++)
		System.out.print(" " + arr1[i]);
	
	int[] arr2 = Arrays.copyOfRange(arr1, 0, 3); 
	System.out.print("\narr2 >>");
	for (int i = 0; i < arr2.length; i++)
		System.out.print(" " + arr2[i]);
	
	int[] arr3 = Arrays.copyOfRange(arr1, 0, 6);
	System.out.print("\narr3 >>");
	for (int i = 0; i < arr3.length; i++)
		System.out.print(" " + arr3[i]);
}
```
### Output
```
arr1 >> 1 2 3 4 5
arr2 >> 3
arr3 >> 1 2 3 4 5 0
```
