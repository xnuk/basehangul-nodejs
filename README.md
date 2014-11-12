Node.js로 쓰여진 [BaseHangul](https://github.com/koreapyj/basehangul).

```js
var basehangul=require('./index.js')
basehangul.encode(new Buffer("123d", "utf8")) // 꺽먹꼐빎
basehangul.decode("법멎민깖롬뢰까돈들뒝멓러벨맑민궈룃흐흐흐").toString('utf8') // 경찰청쇠철창살
```

- `.encode(buffer)`: 바이너리를 basehangul로 인코딩합니다. 넘겨주는 인자는 무조건 Buffer여야 합니다. 그렇지 않으면 `SyntaxError`를 뿜습니다.
- `.decode(string)`: basehangul을 바이너리로 디코딩합니다. 넘겨주는 인자는 무조건 basehangul 문자열이여야 합니다. 그렇지 않으면 `SyntaxError`를 뿜습니다.

이 파일은 Node.js의 `Buffer`를 사용하기 때문에 브라우저용 자바스크립트와는 호환되지 않습니다. 브라우저에서 사용하실 경우 [다른 소스를 찾아보시기 바랍니다.](https://github.com/basehangul/basehangul.github.io)
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/xnuk/basehangul-nodejs?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)