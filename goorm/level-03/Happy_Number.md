## Happy Number

### [문제]
양의 정수 S0의 각 아라비아 숫자들의 제곱의 합으로 양의 정수 S1을 만든다고 하자.  
동일한 방법이라면, S1으로 S2를 만들 수 있고, 그 이후로도 계속 만들 수 있다.  
만약 어떤 i(i>=1)에 대해서 Si=1 이라면, 최초의 S0를 Happy Number라고 부른다.  
Happy Number가 아닌 수를 Unhappy Number라고 부른다.  
위와 같은 결과값을 갖도록 하는 프로그램을 작성하십시오.  
예를 들어, 7에서 시작하게 되면 다음과 같은 일련의 순서를 가지게 되며  
7, 49(=7^2), 97(=4^2+9^2), 130(=9^2+7^2), 10(=1^2+3^2), 1(=1^2),  
따라서 7은 Happy Number이다.
<br/>

### [입력]
첫 라인은 인풋 케이스의 수 n이 주어지며 이후 n라인의 케이스가 주어진다.  
각 테스트 케이스는 한 개의 양의 정수 N으로 구성되며 N은 10^9보다 작다.
<br/>

### [출력]
출력은 주어진 수 N이 Happy Number인지 Unhappy Number인지 여부에 따라 다음과 같이 출력한다.  
N이 Happy Number라면 "N is a Happy Number."  
N이 Unhappy Number라면 "N is an Unhappy Number."  
p는 1부터 시작하는 케이스의 번호이며 각각의 케이스는 한 줄에 결과를 표시한다.
<br/>

### [예시]
[입력] 7  
[출력] 7 is a Happy Number.  

[입력] 66  
[출력] 66 is an Unhappy Number.  


<br/>

### [내 코드]
```javascript
const readline = require("readline");
const rl = readline.createInterface({
	input: process.stdin,
	output: process.stdout
});

let N = 0;

rl.on("line", function(line) {
	N = parseInt(line);
	rl.close();
}).on("close", function() {
	if (N === 1) {
		console.log(`${N} is Happy Number.`);
	} else {
		
		let nextNumber = 0;
		let temp = String(N).split('').map(el => parseInt(el));
		
		for (let i = 0; i < (N**2); i++) {
			
			nextNumber = 0;
			
			for (let j = 0; j < temp.length; j++) {
				nextNumber += temp[j]**2;
			}
			
			temp = String(nextNumber).split('').map(el => parseInt(el));
			
			if (nextNumber === 1) {
				console.log(`${N} is Happy Number.`);
				break;
			} else if (nextNumber === N) {
				console.log(`${N} is an Uhappy Number.`);
				break;
			} else {
				if (i === (N**2)-1) {
					console.log(`${N} is Unhappy Number.`);
					break;
				}
			}
		}
	}
	
	process.exit();
});
```
<br/>

### [통과 여부]
통과
