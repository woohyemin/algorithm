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
