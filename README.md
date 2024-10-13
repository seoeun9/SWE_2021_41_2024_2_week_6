# SWE_2021_41_2024_2_week_6
## <Week 4 Assignment>
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
