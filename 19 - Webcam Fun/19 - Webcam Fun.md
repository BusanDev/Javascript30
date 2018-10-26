## #19 - Webcam Fun

### Webcam

> 수많은 개인용 컴퓨터에 쓰이는 낮은 가격의 웹캠 웹캠(영어: webcam)은 개인용 컴퓨터에 다는 화상 회의 및 화상 채팅용 카메라이다. USB, 이더넷, 와이파이 등을 통해 컴퓨터나 컴퓨터 네트워크로 실시간으로 이미지를 공급한다. (출처: https://ko.wikipedia.org)



### 구현

> 웹 브라우저에서 웹캠을 구현한다.
>
> - localhost 또는 https 환경에서 실행된다.
>
> - 참고: https://webcamtoy.com/



### 환경구성 - browsersync 브라우저 동기화

> https://www.browsersync.io/
>
> Time-saving synchronised browser testing.

```shell
//설치
npm install -g browser-sync

//Start
browser-sync start --server --files "*.css, *.html, *.js"


[Browsersync] Access URLs:
 --------------------------------------
       Local: http://localhost:3000
    External: http://192.168.25.39:3000
 --------------------------------------
          UI: http://localhost:3001
 UI External: http://192.168.25.39:3001
 --------------------------------------
[Browsersync] Serving files from: ./
[Browsersync] Watching files...

```



### canvas

> HTML <canvas> 요소는 스크립트 언어(보통은  자바스크립트를 사용)를 통해 그림을 그리는 데에 사용될 수 있습니다. 예를 들면, 그래프를 그리거나, 사진을 합성하거나, 애니메이션을 만들 때도 사용될 수 있습니다.
>```javascript
><canvas id="tutorial" width="150" height="150"></canvas>
>```

https://developer.mozilla.org/ko/docs/Web/HTML/Element/%EC%BA%94%EB%B2%84%EC%8A%A4

https://developer.mozilla.org/ko/docs/Web/HTML/Canvas/Tutorial



### video

> HTML <video> 요소는 동영상 콘텐츠를 포함하기 위해서 사용됩니다. src속성이나 <source>요소를 이용해 여러개의 동영상 소스를 표시할 수 있고 브라우저가 가장 적정한 것을 선택합니다.
>
> HTML5 이전 버전의 동영상은 플러그인과 같은 블라우저에서만 재생할수 있었습니다.(예:플래시)
>
> HTML <video> 요소는 비디오를 웹페이지에 삽입하는 표준 방법을 지정합니다.

https://developer.mozilla.org/ko/docs/Web/HTML/Element/Video

https://www.w3schools.com/html/html5_video.asp



### navigator.mediaDevices

> Navigator.mediaDevices 읽기 전용 속성을 반환 MediaDevices 연결된 카메라와 마이크 등의 미디어 입력 장치뿐만 아니라, 화면 공유에 대한 액세스를 제공합니다.

https://developer.mozilla.org/en-US/docs/Web/API/Navigator/mediaDevices



### setInterval()

> setInterval() 메서드는 지정된 간격(밀로 초)으로 함수를 호출하거나 표현식을 평가합니다.
>
> ``` javascript
> setInterval(function(){ console.log('hello!!') }, 3000);
> ```

https://www.w3schools.com/jsref/met_win_setinterval.asp



### CanvasRenderingContext2D.drawImage()

> 캔버스에 이미지를 그리는 여러가지 방법을 제공합니다.
>
> ```java
> void ctx.drawImage(image, dx, dy);
> void ctx.drawImage(image, dx, dy, dWidth, dHeight);
> void ctx.drawImage(image, sx, sy, sWidth, sHeight, dx, dy, dWidth, dHeight);
> ```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/drawImage



### CanvasRenderingContext2D.**getImageData**()

> 캔버스 ImageData의 지정된 부분에 대한 기본 필셀 데이터를 나타내는 객체를 반환합니다.
>
> ```javascript
> let pixels = ctx.getImageData ( sx , sy , sw , sh );
> ```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/getImageData



### CanvasRenderingContext2D.**putImageData**()

> 주어진 ImageData 객체의 데이터를 비트 맵에 페인팅합니다.
>
> ```javascript
> void ctx .putImageData (imagedata, dx, dy);
> void ctx .putImageData (imagedata, dx, dy, dirtyX, dirtyY, dirtyWidth, dirtyHeight);
> ```

https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/putImageData