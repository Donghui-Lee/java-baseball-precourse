# 숫자 야구 게임
## 진행 방법
* 숫자 야구 게임 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 과제를 제출한다.

## 과제 제출 과정
* [과제 제출 방법](https://github.com/next-step/nextstep-docs/tree/master/precourse)



## 기능 요구사항
- 1~9 까지 서로 다른 수로 이루어진 3자리 수를 맞추는 게임
- 같은 수가 같은 자리에 있으면 스트라이크,다른 자리에 있으면 볼, 같은 수가 전혀 없으면 포볼 또는 낫싱 이란 힌트 제공
- 힌트를 이용해 상대방(컴퓨터)의 수를 맞추면 승리
- 숫자 야구 게임에서 상대방의 역할을 컴퓨터가 수행
- 컴퓨터는 1~9 까지 서로 다른 임임의 수 3개를 선택
- 게임 플레이어는 3개의 숫자를 입력하고, 컴퓨터는 입력한 숫자에 대한 결과를 추출
- 이 같은 과정을 반복해 컴퓨터가 선택한 3개의 숫자를 모두 맞히면 게임 종료
- 게임 종료 후 게임을 다시 시작하거나 완전히 종료 할 수 있다.


## 기능 목록
### PitchNumber
- 하나의 숫자에 대해 관리
- 1 ~ 9 숫자를 가지는 클래스
- 유효성 체크


### PitchNumbers
- 서로 다른 3가지의 숫자를 가지며 숫자를 비교하는 역할
- 서로다른 숫자 3개를 가지는 클래스
- Set<PitchNumber> 
- 유효성 체크 (3자리수, 중복 체크)
- 스트라이크, 볼 비교


### PitchResult
- 게임 결과(스트라이크, 볼)를 관리
- 게임 종료 여부 판단
- 스트라이크, 볼 갯수 유효성 체크(볼의 갯수의 합은 3 이하)


### Player
- 하나의 플레이어 역할
- 서로 다른 숫자 3개(PitchNumbers)를 가짐
- 상대방의 숫자에 대해 비교
- 비교 결과(PitchResult)를 가짐


### BaseballGame
- 게임 진행을 관리하는 역할
- 입력/출력 연결
