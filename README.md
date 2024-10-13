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
---
## <Week 5 Assignment>
---
### 코드 1
`docker exec Seoeun cat /etc/os-release`
---
1. 설명
  -'Seoeun'이라는 이름의 Docker 컨테이너 내부에서 실행 중인 운영체제 정보를 확인합니다.
2. 실행 결과
```
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
```
### 코드 2
`docker exec Seoeun git --version`
1. 설명
   - Docker 컨테이너 `Seoeun` 내부에서 Git의 버전을 출력합니다.
2. 실행 결과
`git version 2.43.0`
   - git 버전 2.43.0을 사용하고 잇습니다.
### 코드 3
`docker exec Seoeun python3 --version`
1. 설명
   - Docker 컨테이너 `Seoeun` 내부에서 Python의 버전을 출력합니다.
2. 실행 결과
`Python 3.12.3`
   - 파이썬 3.12.3 버전을 사용하고 있습니다.
### 코드 4
`docker inspect --format="{{ .HostConfig.Binds }}" Seoeun`
1. 설명
   -호스트와 'Seoeun' 컨테이너 간에 어떤 디렉토리가 바인딩되어 있는지 출력합니다.
2. 실행 결과
`[/home/user/data:/mnt/data]`
   -호스트의 `/home/user/data` 디렉토리가 컨테이너 내의 `/mnt/data` 디렉토리에 바인딩되어 있습니다.

