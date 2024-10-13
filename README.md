# SWE_2021_41_2024_2_week_6
## <Week 4 Assignment>
### Code
```
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
1. **함수 설명**:
   - 입력 받은 정수 'n'이 Happy Number인지 판단합니다. 각 자리 숫자를 제곱한 값을 더하고, 그 결과값으로 다시 같은 과정을 반복하면서 총 합이 1이 되는지 판명합니다. 만약 1이 된다면 **Happy Number**이고 무한 루프에 빠진다면 Happy Number가 아닙니다.
