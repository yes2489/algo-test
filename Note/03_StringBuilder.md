## StringBuilder (java.lang.StringBuilder)
- String은 immutable 객체라 한 번 생성되면 변경할 수 없음. 따라서 + 연산자를 통해 문자열을 연결 시 연결할 때 마다 새로운 문자열 객체가 생성됨
- 이를 해결하기 위해 StringBuilder 등장
- mutable한 성질을 가지고 있으며, 문자열 연산 시 새로운 객체를 생성하는 것이 아닌 기존 데이터에 더하는 방식을 사용하여 속도도 빠르고 상대적으로 부하가 적음

### 생성자
```java
// 1. 기본 생성자
StringBuilder sb = new StringBuilder();

// 2. int size 값을 인자로 하는 생성자
// int 타입의 값으로 buffer의 사이즈를 지정
StringBuilder sb = new StringBuilder(20);

// 3. String 문자열을 인자로 하는 생성자
StringBuilder sb = new StringBuilder("abc");
```

### 주요 메서드
#### append
- 문자열 추가
```java
sb.append("abc");
```
#### insert
- offset 위치에 str 추가
```java
sb.insert(int offset, String str);
```
#### replace
- 첫 번째와 두 번째 파라미터로 받는 숫자 인덱스에 위치한 문자열을 대체
```java
sb.replace(int idx1, int idx2, String str);
```
#### substring
- 인덱싱
- 파라미터 1개 : 해당 인덱스부터 끝까지 | 파라미터 2개 : `start`부터 `end - 1` 까지
```java
sb.substring(int start);
sb.substring(int start, int end);
```
#### deleteCharAt
- 인덱스에 위치한 문자 하나를 삭제 | `start`부터 `end - 1` 까지 문자를 삭제
```java
sb.deleteCharAt(int idx);
sb.deleteCharAt(int idx, int end);
```
#### toString
- String으로 변환
```java
sb.toString();
```
#### reverse
- 해당 문자를 전체 뒤집기
```java
sb.reverse();
```
#### setCharAt
- index 위치의 문자를 s로 변경
```java
sb.setCharAt(int idx, String s);
```
#### setLength
- 현재 문자열 기준 길게 조정하면 공백으로 채워짐, 짧게 조정하면 나머지 문자 삭제
```java
sb.setLength(int len)
```
#### trimToSize
- 문자열이 저장된 char[]배열 사이즈를 현재 문자열 길이와 동일하게 조정 (문자열 뒷부분의 공백을 모두 제거)
```java
sb.trimToSize();
```
