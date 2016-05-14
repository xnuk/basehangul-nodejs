Node.js로 쓰여진 [BaseHangul](https://github.com/koreapyj/basehangul).

```js
var basehangul=require('./index.js')
basehangul.encode(new Buffer("123d", "utf8")) // 꺽먹꼐빎
basehangul.decode("법멎민깖롬뢰까돈들뒝멓러벨맑민궈룃흐흐흐").toString('utf8') // 경찰청쇠철창살
```

- `.encode(buffer)`: 바이너리를 basehangul로 인코딩합니다. 넘겨주는 인자는 무조건 Buffer여야 합니다. 그렇지 않으면 `SyntaxError`를 뿜습니다.
- `.decode(string)`: basehangul을 바이너리로 디코딩합니다. 넘겨주는 인자는 무조건 basehangul 문자열이여야 합니다. 그렇지 않으면 `SyntaxError`를 뿜습니다.

이 파일은 Node.js의 `Buffer`를 사용하기 때문에 브라우저용 자바스크립트와는 호환되지 않습니다. 브라우저에서 사용하실 경우 [다른 소스를 찾아보시기 바랍니다.](https://github.com/basehangul/basehangul.github.io)

UPDATE: [Node 6의 Buffer API 변경으로 인해](https://nodejs.org/en/blog/release/v6.0.0/#notable-changes) Node 6.0.0 이상의 버전에서는 동작하지 않을 수 있습니다.
