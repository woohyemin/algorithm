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
