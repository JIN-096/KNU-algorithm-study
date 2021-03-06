# 다이나믹 프로그래밍



- **다이나믹 프로그래밍**이란 여러 개의 하위 문제들을 먼저 푼 후 그 결과를 쌓아올려 주어진 문제를 해결하는 알고리즘이다.
  - 문제를 해결하기 위한 점화식을 찾아낸 후 점화식의 항을 밑에서 부터 차례로 구해나가 답을 알아내면 되는 것이다.
- 피보나치의 예를 생각해보면 재귀함수로 구현시 N번째 항을 구할 때 O(1.618<sup>N</sup>) 이지만 DP로 구하면 O(N)에 구할 수 있다.

- 계단 오르기 문제, 타일 채우기 문제 등이 있음



### 분할 정복과의 비교

- 다이나믹 프로그래밍은 처음의 문제를 작은 문제로 나누어 각 문제의 답을 계산하여 원래 문제에 대한 답을 구한다는 점에서 분할 정복(Divide & Conquer)와 비슷하다. 
- 분할 정복과 DP의 차이점은 분할 정복의 경우 나눈 문제들 끼리 답이 **겹치지 않지만**, DP의 경우 답이 **중복**이 된다.
  - 다시 말하면, 분할정복, DP는 **문제를 나누는 방식**에 차이가 있다.

<img src="https://media.vlpt.us/images/polynomeer/post/031441af-5c78-479b-8517-751c0e19217f/DP.png" alt="img" style="zoom:67%;" />

### 다이나믹 프로그래밍의 조건

1. **Overlapping Subproblem : 겹치는 부분 문제**
   - 항상 새로운 부분 문제를 생성해내기 보다는 계속해서 같은 부분 문제를 재사용되는 경우
2. **Optimal Substructure : 최적 부분 구조**
   - 어떤 문제의 최적의 해결책이 그 부분 문제의 최적의 해결책으로부터 설계 될 수 있는 경우
     - 문제의 정답을 부분 문제의 정답으로부터 구할 수 있는 경우를 의미



### 메모이제이션(Memoization)

- 다이나믹 프로그래밍에서는 각 문제는 **한 번만** 풀어야 한다.
  - Optimal substructure를 만족하기 때문에 같은 문제는 구할 때마다 정답이 같다.
- 정답을 한 번 구했으면 그 정답을 저장해놓는다. 이를 **메모이제이션(Memoization)**이라 한다.



### 동적 계획법 구현 방식

1. **Top-down**: 처음 문제를 작은 문제로 쪼개면서 푼다. **재귀**로 구현할 수 있다.

2. **Bottom-up**: 작은 문제부터 차례대로 푼다. **반복문**으로 구현할 수 있다.

   



> 참고링크
>
> https://blog.encrypted.gg/737?category=773649
>
> https://velog.io/@polynomeer/%EB%8F%99%EC%A0%81-%EA%B3%84%ED%9A%8D%EB%B2%95Dynamic-Programming

