## 문자열
### replace
- 자신이 바꾸고싶은 문자로 문자열을 치환
```java
replace([기존문자], [바꿀문자])
```
### replaceAll
- 정규식을 통해 자신이 바꾸고싶은 문자로 문자열을 전부 치환 (특수문자로 치환 불가)
```java
replaceAll([정규식], [바꿀문자])
```
### replaceFirst
- 자신이 바꾸고 싶은 문자열을 가장 처음 해당하는 한 번만 치환
```java
replaceFirst([기존문자], [바꿀문자])
```
### substring
- 문자열 자르기
```java
substring([startIdx]); // 시작 idx부터 끝까지
substring([startIdx],[endIdx]); // 시작 idx위치부터 끝 idx 전까지
```
### split
- 특정 문자를 기준으로 문자열을 잘라서 배열에 넣음
```java
문자열배열 = 대상문자열.split("[기준문자]");
```
### repeat
- 문자열 반복
```java
repeat([반복횟수]);
```
### toUpperCase | toLowerCase
- 소문자를 대문자로 | 대문자를 소문자로 변환
```java
str.toLowerCase();
str.toUpperCase();

Character.toUpperCase('[char]');
Character.toLowerCase('[char]');
```
### indexOf | lastIndexOf
- indexOf : 특정 문자나 문자열이 __앞에서__ 부터 처음 발견되는 인덱스를 반환, 찾지 못하였을 경우 '-1' 반환
- lastIndexOf : 특정 문자나 문자열이 __뒤에서__ 부터 처음 발견되는 인덱스를 반환, 찾지 못하였을 경우 '-1' 반
```java
indexOf([str]);
indexOf([int]);
lastIndexOf([str]);
lastIndexOf([int]);
```

## 형변환
### String to Int
```java
Integer.parseInt([String 값]);
Integer.valueOf([String 값]);
```
### Int to String
```java
String.valueOf([String 값]);
Integer.toString([String 값]);
```
