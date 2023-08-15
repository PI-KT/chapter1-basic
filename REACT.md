# CH 1. 모던 자바스크립트 기초

## 1.1 개요
- 지금은 프런트엔드뿐만 아니라 벡엔드도 구현할 수 있다.
- 장점이자 단점이기도 하지만 프런트엔드는 기술 변화가 매우 빠르다.

## 1.2 DOM, 가상 DOM
- Document Object Model
- DOM은 HTML을 해석해서 트리 구조로 나타낸 것이다.
- 기존 자스에서는 화면 요소를 변경할 때 DOM을 직접 지정해서 바꿔 쓰는 처리를 했다.
```Javascript
// Javascript
var textElement = document.createElement("p");
textElement.textContent = "Hello World!!";
document.getElementById("nushida").appendChild(textElement);

// jQuery
var textElement = $("<p>").text("Hello World!!");
$("#nushida").append(textElement);
```
- 이런 코드는 순차적이서 이해하기 쉽지만 렌더링 비용에 문제가 발생하기 쉽고, 코드가 비대해져 어디에서 무엇을 하고 있는지 쉽게 파악하기 어려운 단점이 있다. 이를 해결하기 위해 만들어진 것이 가상 DOM이다.

### 가상 DOM
- 가상의 DOM을 이용해 실제 DOM과의 차이를 비교하고 변경된 부분만을 실제 DOM에 반영

## 1.3 패키지 관리자
- 예전에는 자스 개발할 때 모든 처리를 파일 하나에 기술했다.
- 이제는 npm, yarn과 같은 패키지 관리자를 사용함으로써 앞에서 설명한 문제점들이 개선되었다.
- 이미 만들어진 것이 있는데 굳이 0부터 개발하는 것보다는 사용 가능하고 편리한 것은 활용하고, 프로젝트에 필요한 시간과 에너지를 꼭 쏟아야 할 부분에 집중하는 것이 낫다.
```bash
npm install [패키지명]
yarn add [패키지명]
```