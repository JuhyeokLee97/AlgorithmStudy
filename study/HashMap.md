# HashMap<K, V>
## 개요
<p>

Map Interface의 해시 테이블 기반으로 구현된 것이다.</br>
``HashMap``은 ``Map(Interface)``를 해시 테이블 기반으로 구현된 것입니다. </br>
``Map<K, V>``이란  ``K(키)``와 ``V(값)`` 두 쌍으로 데이터를 보관하는 자료구조이다.</br>
``K``는 중복 저장되지 않는다.</br>
``V``는 중복 저장될 수 있다.


</p>

## 내장 함수 정리
|반환형|함수|설명|
|----|----|----|
|void|clear()|모든 맵핑을 삭제한다.|
|object|clone()|HashMap의 인스턴스의 얕은 복사본을 반환한다.(키와 값은 복제되지 않는다.)|
|boolean|containsKey(Object key)|HashMap에 해당 key 값을 갖고 있는지에 대한 참/거짓을 반환한다.|
|boolean|containsValue(Object value)|HashMap에 해당 value 값을 갖고 있는지에 대한 참/거짓을 반환한다.|
|V|get(Object value)|HashMap에 해당 키와 맵핑된 value 값을 반환하거나, 맵핑된 value 값이 없다면 null을 반환한다.|
|**V**|**getOfDefault(Object value, V defaultValue)**|**HashMap에 해당 키와 맵핑된 value 값을 반환하거나, 맵핑된 value 값이 없다면 defaultValue를 반환한다.**|

## HashMap 데이터 삽입 
|반환형|함수|설명|
|----|----|----|
|V|put(K key, V value)|Associates the specified value with the specified key in this map.|
| void|putAll<Map<? extends K, ? extends V> m) |Copies all of the mappings from the specified map to this map. |
|Set<K> |KeySet() |Returns a Set view of the keys contained in this map. |
|Collection<V> |values() | Returns a Collection view of the values contained in this map.|


### Code : ``put(K key, V value)``, ``putAll<Map<? extends K, ? extends V> m)``
``` java
	public static void main(String[] args) {
		// Create an empty HashMap For using 'put'
		HashMap<Integer, String> hm = new HashMap<>();

		hm.put(0, "John");
		hm.put(1, "student");
		hm.put(2, "psy");
		hm.put(99, "name");

		// Display the HashMap
		System.out.println("Inital Mappings are: " + hm);

		// Create an empty HashMap For Using 'putAll'
		HashMap<Integer, String> newHm = new HashMap<>();
		
		newHm.putAll(hm);
		// Display the HashMap
		System.out.println("Result of putAll method is : " + newHm);

	}
```
### Output
```
Inital Mappings are: {0=John, 1=student, 2=psy, 99=name}
Result of putAll method is : {0=John, 1=student, 2=psy, 99=name}
```

## HashMap 데이터 읽기
|반환형|함수|설명|
|----|----|----|

### Code: ``get(Object key)``
``` java
	public static void main(String[] args) {
		// Create an empty HashMap For using 'put'
		HashMap<Integer, String> hm = new HashMap<>();

		hm.put(0, "John");
		hm.put(1, "student");
		hm.put(2, "psy");
		hm.put(99, "name");

		// Display the HashMap
		System.out.println("Inital Mappings are: " + hm);

		// HashMap's Data Access
		String val1 = hm.get(0);
		System.out.println("Data Access - hm.get(0) : " + val1);
		String val2 = hm.get(1);
		System.out.println("Data Access - hm.get(1) : " + val2);
		String val3 = hm.get(2);
		System.out.println("Data Access - hm.get(2) : " + val3);
		String val4 = hm.get(99);
		System.out.println("Data Access - hm.get(99) : " + val4);
	}
```
### Result
``` 
Inital Mappings are: {0=John, 1=student, 2=psy, 99=name}
Data Access - hm.get(0) : John
Data Access - hm.get(1) : student
Data Access - hm.get(2) : psy
Data Access - hm.get(99) : name
```

### Code: ``keySet()``, ``values()``
``` java
	public static void main(String[] args) {
		// Create an empty HashMap For using 'put'
		HashMap<Integer, String> hm = new HashMap<>();

		hm.put(0, "John");
		hm.put(1, "student");
		hm.put(2, "psy");
		hm.put(99, "name");
		
		// Display the HashMap values
		System.out.println("hm.keys : " + hm.keySet());

		// Display the HashMap values
		System.out.println("hm.values : " + hm.values());				
	}
```

### Output
```
hm.keys : [0, 1, 2, 99]
hm.values : [John, student, psy, name]
```

## HashMap 데이터 업데이트
desc...
### Code
### Result

## HashMap 데이터 삭제
desc...
### Code
### Result
