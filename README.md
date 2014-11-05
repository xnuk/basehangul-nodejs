Node.js로 쓰여진 [BaseHangul](https://github.com/koreapyj/basehangul).

```js
var basehangul=require('./index.js')
basehangul.encode(new Buffer("123d", "utf8")) // 꺽먹꼐빎
basehangul.decode("법멎민깖롬뢰까돈들뒝멓러벨맑민궈룃흐흐흐").toString('utf8') // 경찰청쇠철창살
```

- `.encode(buffer)`: 바이너리를 basehangul로 인코딩합니다. 넘겨주는 인자는 무조건 Buffer여야 합니다. 그렇지 않으면 `SyntaxError`를 뿜습니다.
- `.decode(string)`: basehangul을 바이너리로 디코딩합니다. 넘겨주는 인자는 무조건 basehangul 문자열이여야 합니다. 그렇지 않으면 `SyntaxError`를 뿜습니다.