# 💡Quiz 1. 피보나치 수열 부호 번갈아서 계산 출력
## 📝 의사 코드 설계

1. 규칙 찾기
- 피보나치수열이 어떤 규칙을 가지고 있는지 파악하기
- 첫번째 값과 두 번째 값을 더하면 세번째 값이 나오고 네번째 값은 두번째 값과 세번째 값을 더한 것. 즉, 이전 값과 현재값을 더하면 다음 값이 출력되는 규칙

2. 부호 번갈아가면서 계산
- 부호 번갈아가면서 계산하게 되면 어떤 규칙이 있는지 파악하기
- 홀수 번째에 있는 수열은 -, 짝수번째에 있는 수열은 더하는 규칙

3. 규칙을 출력에 적용
- for 반복을 이용하면하여 count가 홀수일 때는 -, 짝수일 때는 +
- 첫번째 값을 1로 선언, 두번째 값을 2로 선언하고 토탈값을 0으로 초기화
- 10번째 수열까지의 합을 출력해야하니까 반복은 10번하기
- 토탈 값을 누적하며 홀수일 때는 토탈 값에서 -, 짝수일 때는 +
