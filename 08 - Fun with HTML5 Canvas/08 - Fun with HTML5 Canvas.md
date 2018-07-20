​																		**2018.07.21 Park Jun**


#08 - Fun with HTML5 Canvas			

- 실습강좌 url : [https://javascript30.com](https://javascript30.com/)													




### Canvas

> HTML <canvas> 요소는 스크립트 언어(보통은  자바스크립트를 사용)를 통해 그림을 그리는 데에 사용될 수 있습니다. 예를 들면, 그래프를 그리거나, 사진을 합성하거나, 애니메이션을 만들 때도 사용될 수 있습니다.

```javascript
<canvas id="tutorial" width="150" height="150"></canvas>
```

https://developer.mozilla.org/ko/docs/Web/HTML/Element/%EC%BA%94%EB%B2%84%EC%8A%A4

https://developer.mozilla.org/ko/docs/Web/HTML/Canvas/Tutorial



#### HTMLCanvasElement.getContext()

> 캔버스에서 드로잉 컨텍스트를 반환합니다.

```javascript
var canvas = document.getElementById('tutorial');

//CanvasRenderingContext2D을 얻기위해 "2d"로 지정합니다.
var ctx = canvas.getContext('2d');
```

https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/getContext

https://developer.mozilla.org/ko/docs/Web/HTML/Canvas/Tutorial/Basic_usage

https://developer.mozilla.org/ko/docs/Web/API/CanvasRenderingContext2D



#### CanvasRenderingContext2D.beginPath()

> Canvas 2D API 의 beginPath()  메소드는 하위 경로 목록을 비워서 새 경로를 시작합니다. 새 경로를 만들 때이 메서드를 호출합니다.

```javascript
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');

ctx.beginPath();
```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/beginPath



#### CanvasRenderingContext2D.strokeStyle

> 캔버스 2D API 의 strokeStyle 속성은 도형 주위의 선에 사용할 색상이나 스타일을 지정합니다. 기본값은#000(검은 색)입니다.

```javascript
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
ctx.beginPath();

ctx.strokeStyle = 'blue';
ctx.strokeStyle = "rgb(200,0,0)";
```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/strokeStyle



#### CanvasRenderingContext2D.lineJoin

> 캔버스 2D API 의 lineJoin 속성은 모양에서 길이가 0이 아닌 두 개의 연결 세그먼트 (선, 호 또는 곡선)가 어떻게 결합되는지를 결정합니다.

```javascript
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
ctx.beginPath();
ctx.strokeStyle = 'blue';
ctx.strokeStyle = "rgb(200,0,0)";

// 'round' || 'bevel' || 'miter'
ctx.lineJoin = 'round'; 
```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/lineJoin



#### CanvasRenderingContext2D.lineCap

> 캔버스 2D API 의 lineCap 속성은 모든 선의 끝점을 그리는 방법이 결정됩니다. 

```javascript
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
ctx.beginPath();
ctx.strokeStyle = 'blue';
ctx.strokeStyle = "rgb(200,0,0)";
ctx.lineJoin = 'round'; 

// 'butt' || 'round' || 'square'
ctx.lineCap = 'round'; 
```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/lineJoin



#### CanvasRenderingContext2D.moveTo()

> Canvas 2D API 의 moveTo() 메소드는 새 하위 경로의 시작점을 (x, y)좌표 로 이동합니다.

```javascript
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
ctx.beginPath();
ctx.strokeStyle = 'blue';
ctx.lineJoin = 'round'; 
ctx.lineCap = 'round'; 

ctx.moveTo(50, 50);
```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/moveTo



#### CanvasRenderingContext2D.lineTo()

> 캔버스 2D API 의 lineTo() 메소드는 서브 경로의 마지막 점을 x, y직선 이있는 좌표에 연결합니다 (실제로 그리지는 않습니다).

```javascript
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
ctx.beginPath();
ctx.strokeStyle = 'blue';
ctx.lineJoin = 'round'; 
ctx.lineCap = 'round'; 
ctx.moeTo(50, 50);

ctx.lineTo(100, 50);
```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/lineTo



#### CanvasRenderingContext2D.stroke()

> Canvas 2D API 의 stroke() 메소드는 0이 아닌 굴곡 규칙을 사용하여 현재 스트로크 스타일로 현재 또는 지정된 경로를 스트로크합니다.

```javascript
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
ctx.beginPath();
ctx.strokeStyle = 'blue';
ctx.lineJoin = 'round'; 
ctx.lineCap = 'round'; 
ctx.moveTo(50, 50);
ctx.lineTo(50, 50);
ctx.stroke();
```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/stroke
