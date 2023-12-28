# Blob
Binary Large OBject, 블랍

이진 데이터를 담고 있는 큰 객체

이미지, 사운드, 비디오 같은 멀티미디어 데이터를 관리 할 때 사용

데이터 자체라기보다는 데이터를 간접적으로 접근하기 위한 객체(대용량의 멀티미디어 데이터를 하나의 엔티티로 관리할 수 있도록 도와주는 역할)

```js
const obj = { hello: "world" };
// blob 생성
// 인수는 array와 options
// Blob(array, options);
const blob = new Blob([JSON.stringify(obj, null, 2)], {
  type: "application/json",
});
```

---
# 출처

[Blob](https://developer.mozilla.org/ko/docs/Web/API/Blob)
[Blob(블랍) 이해하기](https://heropy.blog/2019/02/28/blob/)