연산자(operator)
=================
## 1. 정의
- 프로그램에서 데이터를 처리하여 결과를 산출할 때 사용되는 표시나 기호.

## 2. 종류
- 연산자는 필요로 하는 피연산자의 수에 따라 단항, 이항, 삼항 연산자로 구분된다. 피연산자란 연산되는 데이터를 의미한다.

### 2.1. 단항 연산자
- 증감 연산자  
`++` : 변수의 값을 1 증가시킨다.  
`--` : 변수의 값을 1 감소시킨다.

- 부호 연산자  
`+` : 피연산자의 부호를 유지한다.  
`-` : 피연산자의 부호를 변경한다.

- 비트 연산자  
`~` : 피연산자의 모든 비트값을 반전시킨다.

- 논리 부정 연산자  
`!` : true를 false로, false를 true로 반전시킨다.
#
### 2.2. 이항 연산자
- 산술 연산자  
`*` : 곱셈을 연산한다.  
`/` : 나눗셈을 연산한다.  
`%` : 나머지를 산출한다.  
`+` : 덧셈을 연산한다.  
`-` : 뺄셈을 연산한다.

- 문자열 연결 연산자  
`+` : 피연산자 중 한쪽이 문자열일 경우 피연산자들을 문자열로 결합한다.

- 비트 이동 연산자  
`<<` : 좌측 피연산자를 우측 피연산자만큼 왼쪽으로 이동시키고 빈자리는 0으로 채운다.  
`>>` : 좌측 피연산자를 우측 피연산자만큼 오른쪽으로 이동시키고 빈자리는 최상위 부호 비트와 같은 값으로 채운다  
`>>>` : 좌측 피연산자의 각 비트를 우측 피연산자만큼 오른쪽으로 이동시키고 빈자리를 0으로 채운다.

- 비교 연산자  
`<`, `<=`, `>`, `>=` : 대소를 검사한다.  
`==` : 두 피연산자가 같은지를 검사한다.  
`!=` : 두 피연산자가 다른지를 검사한다.

- 논리곱 연산자  
`&` : 피연산자가 모두 true일 경우 true를 산출한다.

- 배타적 논리합 연산자  
`^` : 피연산자가 하나는 true이고 하나는 false일 경우 연산 결과를 true를 산출한다.  

- 논리합 연산자  
`|` : 피연산자 중 하나 이상 true일 경우 연산 결과를 true를 산출한다.  
`&&`,`||` : `&`,`|`와 산출 결과는 같지만 모든 피연산자를 반드시 평가하고 산출한다.

- 대입 연산자
`=` : 우측의 피연산자를 좌측 변수에 저장  
`+=` : 우측의 피연산자의 값을 좌측 변수의 값과 `+`연산 후에 다시 변수에 저장한다.
> `+`를 `-`, `*`, `/`, `%`, `&`, `|`, `&`, `<<`, `>>`, `>>>`로 치환하여 응용이 가능하다
#
### 2.3. 삼항 연산자  
`?:` : 피연산자1 `?` 피연산자2 `:` 피연산자3 꼴이며 피연산자1 연산결과가 true일시 피연산자2를, false일시 피연산자3을 산출한다.
#  
## 3. 연산 처리 순서
우선순위 | 연산자 
---|---
1 | 증감(++, --), 부호(+, -), 비트(~), 논리(!)
2 | 산술(*, /, %)
3 | 산술(+, -)
4 | 쉬프트(<<, >>, >>>)
5 | 비교(<, >, <=, >=, instanceof)
6 | 비교(==, !=)
7 | 논리(&)
8 | 논리(^)
9 | 논리(&#124;)
10 | 논리(&&)
11 | 논리(&#124;&#124;)
12 | 조건(?:)
13 | 대입(=, +=, ...)
> 위 2.1 ~ 2.3 연산자들 중 대입연산자를 제외하고 위에서 아래순으로 우선순위를 갖는다. 대입연산자는 우선수위가 가장 낮다.  
> 단항 연산자, 부호 연산자, 대입연산자는 오른쪽에서 왼쪽으로, 나머지 연산자는 왼쪽에서 오른쪽으로 연산된다.
