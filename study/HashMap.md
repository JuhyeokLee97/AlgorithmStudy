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
desc...
### Code
### Result

## HashMap 데이터 읽기
desc...
### Code
### Result

## HashMap 데이터 업데이트
desc...
### Code
### Result

## HashMap 데이터 삭제
desc...
### Code
### Result
