## Factorial(계승)

### [문제]
팩토리얼은 1부터 n까지의 수를 모두 곱하는 것입니다.  
n이 양수일 때 n의 팩토리얼 결과를 구하는 프로그램을 작성하십시오.
<br/>

### [입력]
15 이하 양의 정수
<br/>

### [출력]
팩토리얼의 결과 값
<br/>

### [예시]
[입력]  
5  
[출력]  
120  

[입력]  
10  
[출력]  
3628800
<br/>

### [내 코드]
```javascript
//반복문으로 풀기
const readline = require("readline");
const rl = readline.createInterface({
	input: process.stdin,
	output: process.stdout
});

let n = 0;

rl.on("line", function(line) {
	n = parseInt(line);
	rl.close();
}).on("close", function() {
  
 	let result = 1;
  
 	for (let i = 1; i <= n; i++) {
 		result *= i;
 	}
  
 	console.log(result);
	process.exit();
});
```

```javascript
//재귀함수 이용해서 풀기
const readline = require("readline");
const rl = readline.createInterface({
	input: process.stdin,
	output: process.stdout
});

let n = 0;

rl.on("line", function(line) {
	n = parseInt(line);
	rl.close();
}).on("close", function() {
  
	function factorial (n) {
		if (n === 0) {
			return 1;
		} else {
			return n*factorial(n-1);
		}
	}
	
	console.log(factorial(n));
	process.exit();
});
```
<br/>

### [통과 여부]
통과
