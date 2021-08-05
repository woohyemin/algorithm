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

