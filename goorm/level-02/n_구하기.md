## n 구하기

### [문제]
1+2+3+...+n 인 수가 입력받은 수를 넘어서는 시점에서의 n을 구하는 프로그램을 작성하세요.
<br/>

### [입력]
자연수 (100000 이하)
<br/>

### [출력]
입력 받은 수를 넘어서는 시점에서 마지막으로 추가된 숫자 n
<br/>

### [예시]
[입력] 1000  
[출력] 45  

[입력] 200  
[출력] 20

<br/>

### [내 코드]
```javascript
const readline = require("readline");
const rl = readline.createInterface({
	input: process.stdin,
	output: process.stdout
});

let number;
let sum = 0;

rl.on("line", function(line) {
	number = parseInt(line);
	rl.close();
}).on("close", function() {
	let i = 1;
	while(sum <= number) {
		i++;
		sum += i;
	}
	console.log(i);
	
	process.exit();
});
```
<br/>

### [통과 여부]
통과
