# 💡[Weekly] 회고 시스템
## 📝 의사 코드 설계

1. 시스템 설명문 출력 
- print() 사용해서 오늘의 회고, 메뉴 목록 출력하기

2. 회고 추가
- 가장 큰 틀을 while 문 무한루프로 잡기
- if 사용해서 회고 추가 선택하면 실행되게 하기
- 날짜를 입력할 수 있게 readLine() 사용하기
- 내용을 입력할 수 있게 readLine() 사용하기
- 날짜는 키, 값은 회고 내용임
- 추가하면 “회고가 추가되었습니다.” 문구 출력하기

3. 회고 조회
- if 사용해서 회고 조회 선택하면 실행되게 하기
- 날짜를 입력할 수 있게 readLine() 사용하기
- 입력한 날짜(키)에 맞는 값을 딕셔너리에서 호출해서 출력하기

4. 회고 수정
- if 사용해서 회고 수정 선택하면 실행되게 하기
- 날짜를 입력할 수 있게 readLine() 사용하기
- 내용을 입력할 수 있게 readLine() 사용하기
- 딕셔너리에 있는 값을 수정할 수 있게 키를 사용해서 값을 수정하기
- 수정하면 “회고가 수정되었습니다.” 문구 출력하기

5. 회고 삭제
- if 사용해서 회고 삭제 선택하면 실행되게 하기
- 날짜를 입력할 수 있게 readLine() 사용하기
- 딕셔너리에 있는 값을 삭제할 수 있게 removeValue(forKey:) 사용하기
- 삭제하면 “회고가 삭제되었습니다.” 문구 출력하기

6. 전체 조회
- if 사용해서 전체 조회 선택하면 실행되게 하기
- 딕셔너리에 있는 값을 전체 다 가져올 수 있게 print(”딕셔너리 이름”)

7. 종료
- if 사용해서 종료 선택하면 실행되게 하기
- “회고 시스템이 종료됩니다.” 출력하기
- while문의 무한루프를 즉시 종료해주는 break 사용하기

## 🤯 느낀점
1. 구현하는데 정말 오랜 시간이 걸렸다… 아직 이해하기에 어려운 것들이 너무 많다…

2. 의사 코드 설계 단계에서 어떤 루트로 코드가 실행되어야 하는지를 제일 먼저 고민했다. 
- 메뉴를 선택하면 해당 메뉴로 이동
- 종료하기 전까지는 입력한 데이터들이 하나의 그릇에 저장
- 데이터를 삭제하고 수정하고 조회할 수 있게 데이터를 불러올 수 있어야 함
- 메뉴를 선택하여 데이터를 저장하고 그 다음으로 종료를 누르면 바로 시스템이 종료

 이 네 가지를 충족시킬 수 있는 답을 찾기 위해서 교안을 읽으면서 계속 고민했다.
 ”메뉴 이동은 배열로 해야 하나? 저장하려면 딕셔너리를 써야 하는데? 
 삭제, 수정, 조회도 딕셔너리를 써야 하는데… 
 종료 선택하면 시스템이 종료되는건 대체 뭘 써야 하는 거지?”하며 계속 생각하니까
 결국 “while문 무한루프로 메뉴 이동을 가능하게 만들고, break로 종료시키고, 
 그리고 딕셔너리 조회, 수정, 삭제를 이용하면 되겠다.”라고 결론 지을 수 있었다…
 
- 머리로는 이해했는데 실제 응용을 하려고 하니, 딕셔너리를 처음 써봐서 처음에는 모든 메뉴에 딕셔너리를 한 번씩 다 선언해서 값을 저장하려 했다. 실행은 되는데 계속 데이터가 날아가서 정말 눈 앞이 캄캄했다. 근데 while문은 각 조건마다 전부 다시 시작되는 개념이라 딕셔너리를 개별적으로 선언하면 값이 메뉴를 옮길 때마다 날아간다는 걸 깨달았고, 그래서 하나의 딕셔너리에 모든 값을 저장해야 한다고 판단했다. 그 결과 딕셔너리 하나에 모두 저장하려고 while문 밖에 딕셔너리를 선언했더니 됐다.

- 의사코드 짜는 걸 습관화했더니 의사코드를 바탕으로 코드를 짜면 시간을 정말 효율적으로 쓸 수 있다는 걸 몸소 느꼈다. 근데 설계대로 코드를 짰는데 오류가 발생하는 순간 머리가 초기화된다… 그래서 눈앞이 캄캄해지지만 오류 코드를 서치 해보고 교안이랑 다른 분들의 코드를 비교해 보면 **언젠가는** 문제점을 찾을 수 있다는 걸 알게 됐다.

- 완벽하게 이해하지 못한 개념을 가지고 구현하는 거라서 교안 정독 및 의사 코드 설계에 정말 많은 시간을 쏟았다. 그 결과 어느 상황에서는 어떤 코드를 쓰면 좋을지 (머리로)떠올릴 수는 있게됐다. 근데 실제로 구현하려면 정말 오랜 시간이 걸린다…
