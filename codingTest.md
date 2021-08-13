## 리그 경기 횟수 구하기

### [문제]

리그에 속해있는 팀의 수 n이 주어지고 각 팀은 자신을 제외한 모든 팀과 한 경기씩 치루어 순위를 가리는  
스포츠 리그전에서 치루어지는 경기의 수를 구하는 프로그램을 작성하십시오.

2팀이면 1경기, 3팀이면 3경기, 4팀이면 6경기가 치루어 집니다.  
**2명 => 1번 &nbsp;&nbsp;&nbsp;&nbsp; 3명 => 1 + 2 = 3(번) &nbsp;&nbsp;&nbsp;&nbsp; 4명 => 1 + 2 + 3 = 6(번)**  
<br/>

### [입력]
리그에 참여하는 팀의 수  
<br/>

### [출력]
리그에서 치루어 지는 경기의 수  
<br/>

### [예시]
1) 입력 : 4  /  출력 : 6
2) 입력 : 10  /  출력 : 45
<br/>

### [내 코드]
```kotlin
import java.util.Scanner
fun main(args: Array<String>) {
  val reader = Scanner(System.`in`)
  var integer:Int = reader.nextInt()
  var sum:Int = 0
      
  for (i in 1..(integer-1)) {
    sum += i
  }
    
  print(sum)	
}
```
<br/>

### [통과 여부]
통과

<br/>
<br/>
<br/>

## 3과 5의 배수

### [문제]

N(1000 이하의 자연수)을 입력하고 N 이하의 자연수 중 3의 배수, 5의 배수의 합을 구하는 프로그램을 작성하십시오.

<br/>

### [입력]
1000 이하의 자연수 
<br/>

### [출력]
N 이하의 자연수 중 모든 3의 배수 그리고 5의 배수의 합  
<br/>

### [예시]
1) 입력 : 1000  /  출력 : 234168
2) 입력 : 50  /  출력 : 593
<br/>

### [내 코드]
```kotlin
import java.util.Scanner
fun main(args: Array<String>) {
	val reader = Scanner(System.`in`)
	var integer: Int = 0
	var sum: Int = 0

	while (true) {
		// println("1000 이하의 자연수로 입력해주세요!")
		integer = reader.nextInt()
		
		if (integer <= 1000) {
			break
		} // else{
			// println("1000 초과 입력! 다시 입력해주세요!!")
		// }
		
	}
	
	for (i in 1..integer) {
		if ((i%3) == 0) { // 3의 배수일 때 sum에 i 더하기 (3의 배수이면서 5의 배수인 경우 3의 배수일 때 i에 더해지고 if문 나감)
			sum += i
		} else if ((i%5) == 0) { // 5의 배수일 때 sum에 i 더하기
			sum += i
		}
	}
	
	println(sum)

}
```
<br/>

### [통과 여부]
통과

<br/>
<br/>
<br/>

## Min 함수

### [문제]

함수의 정의와 호출을 실습할 수 있는 아주 간단한 문제입니다.  
서로 다른 두 정수를 비교하여 더 작은 값을 출력해내는 Min 함수를 작성하시면 됩니다.

<br/>

### [입력]
서로 다른 두 정수
<br/>

### [출력]
두 정수 중 값이 작은 정수  
<br/>

### [예시]
1) 입력 : 10 20  /  출력 : 10
2) 입력 : -5 -30  /  출력 : -30
<br/>

### [내 코드]
```kotlin
import java.util.Scanner
fun main(args: Array<String>) {
	// 공백을 기준으로 한번에 여러 값을 입력받으려면 이렇게
	val reader = Scanner(System.`in`)
	var num1:Int = reader.nextInt()
	var num2:Int = reader.nextInt()
	
	fun Min(num1: Int, num2: Int) {
		if (num1 < num2) {
			print(num1)
		} else if (num1 > num2) {
			print(num2)
		} else {
			print("두 정수는 같은 수인 것 같습니다")
		}
	}
	
	Min(num1, num2)

}
```
<br/>

### [통과 여부]
통과

<br/>
<br/>
<br/>

## 부족한 금액 계산하기

### [문제]

새로 생긴 놀이기구는 인기가 매우 많아 줄이 끊이질 않습니다.  
이 놀이기구의 원래 이용료는 price원 인데, 놀이기구를 N 번 째 이용한다면 원래 이용료의 N배를 받기로 하였습니다.  
즉, 처음 이용료가 100이었다면 2번째에는 200, 3번째에는 300으로 요금이 인상됩니다.  
놀이기구를 count번 타게 되면 현재 자신이 가지고 있는 금액에서 얼마가 모자라는지를 return 하도록 solution 함수를 완성하세요.  
단, 금액이 부족하지 않으면 0을 return 하세요.  
<br/>
#### 제한사항
* 놀이기구의 이용료 price : 1 ≤ price ≤ 2,500, price는 자연수
* 처음 가지고 있던 금액 money : 1 ≤ money ≤ 1,000,000,000, money는 자연수
* 놀이기구의 이용 횟수 count : 1 ≤ count ≤ 2,500, count는 자연수

<br/>

### [입출력 예]
| price   |   money |  count   |  result  |
|:-------:|:-------:|:--------:|:--------:|
|   3     |  20     |    4     |  10      |  

<br/>
이용금액이 3인 놀이기구를 4번 타고 싶은 고객이 현재 가진 금액이 20이라면, 총 필요한 놀이기구의 이용 금액은 30 (= 3+6+9+12) 이 되어 10만큼 부족하므로 10을 return 합니다.

<br/>

### [내 코드]
```javascript
//JavaScript
function solution(price, money, count) {
  var sum = 0;
  for (let i = 1; i <= count; i++) {
    sum += (price * i);
  }
  if (sum > money) {
    return (sum - money);
  } else {
    return 0;
  }
}
```
```kotlin
//Kotlin
class Solution {
    fun solution(price: Int, money: Int, count: Int): Long {
        var total: Long = 0
        for (i in 1..count) {
            total += (price*i)
        }
        if (total > money) {
            return (total - money)
        } else {
            return 0
        }
    }
}
```


<br/>

### [통과 여부]
통과

