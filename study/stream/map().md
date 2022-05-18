# Stream.map()이란

## 사용예시: Convert ArrayList To Array
### 사용한 알고리즘 문제
<p>
	
[Programmers/완전탐색/모의고사](https://github.com/JuhyeokLee97/AlgorithmStudy/blob/main/Programmers/%EC%99%84%EC%A0%84%ED%83%90%EC%83%89/%5B2%5D%20%EB%AA%A8%EC%9D%98%EA%B3%A0%EC%82%AC.md)
	</p>
### Code
``` java

	public static void main(String[] args) {
		ArrayList<Integer> list = new ArrayList<>();
		
		list.add(1);
		list.add(2);
		list.add(3);
		
		int[] result = list.stream().mapToInt(i -> i).toArray();
		for (int i = 0; i < result.length; i++) {
			System.out.println("result[" + i + "] : " + result[i]);
		}
	}
```

### 결과
```
result[0] : 1
result[1] : 2
result[2] : 3
```

### IntStream mapToInt(ToIntFunction<? super T> mapper);
#### 정의
- Returns an {@code IntStream} consisting of the results of applying the given function``(mapper)`` to the elements of this stream.
#### 파라미터 ``ToIntFunction<? super T> mapper``
- 
#### 반환형 ``IntStream``
- 새로운 Stream 반환
