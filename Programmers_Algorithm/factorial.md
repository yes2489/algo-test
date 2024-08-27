```java
// n이 주어질 때 n보다 팩토리얼의 값이 작은 최대의 수 구하기
// 1. 재귀 활용

class Solution {
  public int solution(int n) {
    int answer = 0;
    for (int i = 1; i <= 10; i++) {
      if (n >= factorial(i)) {
        answer = i;
      } else {
          break;
      }
    }
    return answer;
  }
  
  public static int factorial(int num) {
    if (num > 1) {
      return num * factorial(num - 1);
    }
    return num;
  }
}
```

```java
// 2. for문 사용
class Solution {
  public int solution(int n) {
    int answer = 0;
    int factorial = 1;

    for (int i = 1; i <= 10; i++) {
      factorial *= i;
      if (factorial == n) {
        answer = i;
        break;
      } else if (n < factorial) {
        answer = (i-1);
        break;
      }
    }
    return answer;
  }
}
```
    
