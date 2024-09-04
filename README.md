# vue.js-
vue.js 강의

## 설치
1. 크롬 설치
2. Visual Studio Code 설치
3. VSCode Plugins 설치
- korean Language Pack(한국어)
- Indent-Rainbow (코드라인이 길어 졌을때 읽기 편하게 함)
- Auto Rename Tag(태그 이름 변경 시 쌍을 이루는 여는태그 또는 닫는 태그)
- CSS Peek CSS를 금방 찾을 수 있도록 도와줌
- HTML to CSS autocompletion ( class명을 .css파일에서 입력 할 때 자동완성 기능 제공
- HTML CSS Support ( HTML문서에서 CSS의 자동완성 이용
- Live server (html 수정 시 새로고침 없이 즉각 적용
- ESLint (검사기로써 에러가 있는지 검사함
- Prettier 사용 안함 / 코드 포멧터로써 코드를 일관성있고 예쁘게 작성할 수 있도록

## Vue.js devtools
Vue.js 애플리케이션 디버깅을 위한 Chrome 브라우저의 확장 프로그램입니다

## Vue.js를 위한 VSCode Plugins
- Volar
- Vue 3용으로 특별히 제작된 언어 지원 플러그인입니다

## Vue VSCode Snippets
사용구 코드를 빠르게 타이핑 할 수 있도록 도와주는 플러그인



## Vue.js 문법 작성
선언적 렌더링(Declarative Rendering) : Vue는 템플릿 구문({{ 데이터 }})을 활용하여 데이터를 선언적 출력(렌더링) 할 수 있도록 합니다
반응성(Reactivity) : Vue는 JavaScript 상태 변경을 자동으로 추적하고 변경이 발생하면 DOM을 효율적으로 업데이트합니다

<details>
    <summary>코드 보기</summary>
	
```html



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://unpkg.com/vue@3"></script>
    <title>Document</title>
</head>
<body>
    
    <div id="app">
        <button type="button" v-on:click="counter++">counter : {{ counter }}</button>
    </div>


    <script>

        const app = Vue.createApp({

            data(){
                return {
                    counter: 1,
                };
            },
        });
        app.mount("#app");
    </script>
</body>
</html>
```
</details>

- 바인딩

<br>


<details>
    <summary>코드 보기</summary>
	
```html


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://unpkg.com/vue@3"></script>
    <title>Document</title>
</head>
<body>
    
    <div id="app">
        <button type="button" v-on:click="counter++">counter : {{ counter }}</button>
    </div>

    <div id="apps">
        <input type="text" v-bind:placeholder="message">
    </div>


    <script>

        const app = Vue.createApp({

            data(){
                return {
                    counter: 1,
                };
            },
        });
        app.mount("#app");

        const apps = Vue.createApp({
            data(){
                return {
                    message : "값을 입력해주세요!",
                };
            },
        });
        apps.mount("#apps");
    </script>
</body>
</html>
```
</details>
