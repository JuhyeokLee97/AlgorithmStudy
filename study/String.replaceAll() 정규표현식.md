## 정규표현식(Regular Expressions)
- 정규표현식을 줄여서 영어로 <strong>Regex</strong>라고 한다.
- Regex는 문자열에 어떤 패턴의 문자들이 있는지 찾는데 도움을 준다.

## Meta-characters
 - ``Metacharacters``는 Regex의 패턴에서 어떤 문자가 특별한 의미를 갖는 것을 말한다. 예를 들며느 ``\d``는 0에서 9사이의 숫자를 의미한다.

### 자주 사용되는 ``Metacharacters`` 정리
|No|Regular Expression|Description|
|--|--|--|
|1|.|어떤 문자 1개를 의미|
|2|^abc|``abc``로 line을 시작하는가|
|3|abc$|``abc``로 line이 끝나는가|
|4|[abc]|``a``, ``b``, ``c`` 중 임의의 문자 1개|

### ``Metacharacters`` 사용 예제
#### 1. ``.``
##### Code
``` java
String str = "{ad, abc, abcd, ab@, ab#, aabc, abcabd}";
System.out.println(str.replaceAll("ab.", "AB[ ]"));
```

#### Result
``{ad, AB[ ], AB[ ]d, AB[ ], AB[ ], aAB[ ], AB[ ]AB[ ]} ``
