# SWE_2021_41_2024_2_week_6
## <Week 4 Assignment>
### Code
```
// 입력 받은 정수 'n'이 Happy Number인지 판단합니다.
def isHappy(n):

  tmp = set()

  while n != 1:
    num = 0
    for i in str(n):
      num += int(i)**2
    if num in tmp:
      return False
    tmp.add(num)
    n = num

  return True
```
### Explanation
1. **Happy Number란?**
   - 각 자리 숫자를 제곱한 값을 더하고, 그 결과값으로 다시 같은 과정을 반복할 때 총 합이 1이 된다면 **Happy Number**입니다.
   - 만약 무한 루프에 빠지게 된다면, Happy Number가 아닙니다.
 2. **코드 설명**
    - tmp라는 set을 만들어 각 자리 숫자 제곱한 값의 합들을 저장합니다.
    - while문 내에서 제곱과 덧셈을 수행하고, 합이 1인 경우 빠져나옵니다. 이 경우 Happy Number이므로 True를 리턴합니다.
    - 만약 결과가 tmp 내에 이미 기록된 합들 중에 하나라면 무한 루프이므로, False를 반환해 빠져나옵니다.

## <Week 5 Assignment>
