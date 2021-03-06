# ch1 Go와 첫 만남

## 동시성

* 고루틴 Goroutine
    * 프로그램의 entry point 함수를 비롯하여 다른 고루틴과 함께 동시에 실행되는 함수
    * 여러개의 고루틴이 하나의 스레드에서 동작
    * 스레드보다 적은 메모리를 사용
    * Go 런타임에 설정된 논리 프로세서 개수에 따라 자동으로 고루틴을 실행하기 위한 스케쥴링을 처리
    * `go` 키워드를 이용하여 고루틴을 구현
* 채널 Channel
    * 고루틴 간 데이터 전송을 가능하게 하는 데이터 구조
    * 동시에 발생하는 수정 요청으로부터 데이터를 안전하게 보호하기 위한 패턴을 제공
    * 고루틴 간 데이터 접근을 보호하지는 않는다.

## Go 타입 시스템

* 간결한 타입
    * 사용자가 직접 타입을 정의하는 것도 가능
    * 상속된 데이터 구조를 정의하는 것보다 데이터 타입을 정의한 다음 조금 더 큰 타입으로 합성하여 사용
* 작은 동작을 모델링하는 인터페이스 Interface
    * 타입 동작을 표현하기 위해서 사용
    * 타입의 값이 어떤 인터페이스를 구현한다는 것은 그 값이 일련의 특정한 행동을 수행할 수 있다
    * 다른 언어에서 이런 기법을 duck typing 으로 간주한다.
    