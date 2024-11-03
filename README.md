# 💰 로또 발매기

--- 

## 프로젝트 소개
원하는 만큼의 금액을 입력해서 로또를 구매하는 로또 발매기 프로그램입니다. 

📍프로그램 실행시에 사용자는 로또를 구매할 금액을 입력합니다. 금액은 1,000원 단위로 입력합니다.\
로또 한개의 가격은 1,000원 입니다.
```agsl
구입금액을 입력해 주세요.
8000
```
📍입력하고 나면, 로또가 입력한 액수에 맞게 각 로또 번호를 무작위로 생성합니다.
```agsl
8개를 구매했습니다.
[34, 25, 13, 19, 6, 9]
[15, 5, 16, 24, 36, 26]
[30, 33, 3, 12, 19, 27]
[1, 24, 19, 7, 30, 9]
[29, 5, 43, 38, 7, 8]
[21, 7, 6, 24, 20, 35]
[35, 13, 33, 21, 32, 28]
[44, 29, 12, 4, 3, 6]
```

📍생성된 후, 당첨 번호와 보너스 번호를 입력합니다.
```agsl
당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7
```

📍생성된 로또의 번호와 당첨 번호를 비교하여 등수와 수익률을 계산해 줍니다.
```agsl
당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```

📍입력값을 잘못 입력한 경우, 에러 메시지와 함께 다시 입력해야 합니다.\
당첨번호를 잘못 입력한 상황을 예시로 들면 다음과 같습니다.
```agsl
[ERROR] 당첨 번호는 6자리를 입력해야 합니다.

당첨 번호를 입력해 주세요.
1,2,3,4,5,6
```
## 📊 흐름도
프


## 💻 프로젝트 동작 내용
```agsl
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[40, 23, 42, 34, 17, 28]
[9, 45, 35, 32, 22, 24]
[33, 36, 28, 12, 34, 14]
[18, 5, 44, 31, 26, 15]
[34, 18, 6, 30, 9, 3]
[44, 27, 43, 2, 20, 34]
[28, 25, 33, 24, 21, 10]
[44, 22, 38, 33, 16, 31]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
---
3개 일치 (5,000원) - 0개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 0.0%입니다.
```

## ⚙️ 기능 구현 목록
- [x] 구입할 금액을 입력하는 기능
  - [x] 금액이 1,000단위가 아닌 경우 예외 처리
  - [x] 금액이 0원인 경우 예외 처리
  - [x] 금액이 음수인 경우 예외 처리
  - [x] 금액이 아무런 값을 갖지 않는 경우 예외 처리
  - [x] 예외가 발생한 경우 에러 출력 후, 입력을 다시 받기
        
- [x] 로또를 발행하는 기능
  - [x] 구매한 금액에 따른 로또를 발행
  - [x] 발행된 로또 번호는 오름차순으로 정렬
  - [x] 발행된 로또 번호를 출력
  - [x] 발행된 로또 번호 중복시 예외 처리
        
- [x] 당첨 번호를 입력하는 기능
  - [x] 당첨 번호 구분자가 쉼표가 아닌 경우 예외 처리
  - [x] 당첨 번호에 숫자가 아닌 문자가 오는 경우 예외 처리
  - [x] 당첨 번호에 아무런 값이 없는 경우 예외 처리
  - [x] 당첨 번호가 6개가 아닌 경우(이하,이상 포함) 예외 처리
  - [x] 당첨 번호의 범위가 1부터 45까지가 아닌 경우 예외 처리
  - [x] 당첨 번호가 중복되는 경우 예외 처리
  - [x] 예외가 발생한 경우 에러 출력 후, 입력을 다시 받기
        
- [x] 보너스 번호를 입력하는 기능
  - [x] 보너스 번호가 1부터 45까지 아닌 경우 예외 처리
  - [x] 보너스 번호가 숫자가 아닌 문자가 오는 경우 예외 처리
  - [x] 보너스 번호에 음수가 오는 경우 예외 처리
  - [x] 보너스 번호에 아무런 값이 없는 경우 예외 처리
  - [x] 보너스 번호에 여러개의 수를 입력한 경우 예외 처리
  - [x] 예외가 발생한 경우 에러 출력 후, 입력을 다시 받기
        
- [x] 당첨을 통계내는 기능
  - [x] 당첨 내역을 출력
  - [x] 총 수익률 계산
  - [x] 총 수익률 출력

## ✈️ 프로젝트 구조
- Controller : InputView를 통해 입력 받은 문자열을 검증 및 dto 생성 후, Service 계층에 전달
- Service : Repository로 부터 데이터를 가져오고, 대부분의 비즈니스 로직을 처리합니다.
- Repository : 저장이 필요한 데이터를 저장하고, 단순한 쿼리르 제공합니다.
- Domain : Repository로부터 데이터를 가져오거나 저장할때 사용합니다.
- View
  - InputView : 사용자에게 문자열을 입력 받습니다.
  - OutputView : 문자열 입력 받을시 필요한 문자를 출력, 전달받은 dto 출력합니다.


## 프로젝트에 고민하고 적용한 점 

1. Repository에 적용한 싱글턴 패턴\
입력한 데이터를 저장해야 하는 부분을 해겷하기 위해서, Repository 계층을 싱글턴 패턴으로 적용했습니다.
싱글턴 패턴을 사용하는 것이 Repository에 저장된 데이터의 무결성을 지킬 수 있다고 생각하여 구현했습니다.


2. 유효검사를 해주는 validator 클래스 분리\
제가 구성한 프로젝트는 Controller - Service - Repository 구조입니다. Controller는 데이터의 유효성을 검증하고, dto로 변환하여 Service 계층으로 데이터를 넘겨주는 
역할입니다. Controller에서 유효성 검사를 하기 때문에 Domain 내부에서 검사를 해주는 것 보다는 따로 유효성을 검사하는 코드를 분리해주는 것이 가독성을 더 높일 수 있다고 생각하여 구현했습니다.
유효성 검사시 올바르지 않은 경우 에러를 throw 하도록 구현했습니다. 


3. dto를 통해 계층간 데이터 전달\
각 계층간 데이터를 전달할 때, 계층 간 의존성을 줄이기 위해서 dto을 사용했습니다.


4. Service 계층에 비즈니스 로직 작성\
비즈니스 로직에만 집중할 수 있도록 Service 계층에만 작성 싶었고, 하나의 트랜잭션으로 묶고 싶었습니다. 그러나, 비즈니스 로직을 Service 계층에 구현하다보니, Domain이 데이터만 전달하게 되는 
단점이 있습니다. 


5. 예외를 정의하는 클래스 분리\
   예외 상황을 쉽게 파악할 수 있도록 각 예외 상황에 맞는 커스텀 예외 클래스를 정의하였고, 예외 메시지는 중앙에서 관리하는 대신, 각 예외 클래스 내에 해당 예외 상황에 맞는 메시지를 작성하여 메시지의 역할을 예외 상황별로 깔끔하게 분리했습니다. 이를 통해 코드의 응집도가 높아졌고, 예외 처리를 보다 직관적으로 이해하고 관리할 수 있게 되었습니다. 또한, 특정 예외 상황에 대한 메시지 수정이 필요할 때 해당 예외 클래스만 수정하면 되므로 유지보수가 용이해졌습니다.

   
6. throw된 예외는 Controller 계층에서 처리\
   예외 발생 시 해당 부분부터 다시 입력받아야 하는 기능을 각 Validator 클래스가 아닌 Controller 계층에서만 수행하도록 하여, 역할과 책임을 명확히 분리했습니다. 이를 통해 Validator는 검증의 역할에만 집중할 수 있게 되었고, Controller 계층에서 사용자 입력을 제어하는 로직을 일관성 있게 관리할 수 있게 되었습니다.

