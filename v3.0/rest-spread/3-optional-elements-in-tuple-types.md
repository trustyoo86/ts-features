# 3\) Optional elements in tuple types

* Array type에서 `?`을 이용하여 optional하게 타입 지정 가능

```typescript
let t: [number, string?, boolean?];
t = [42, "hello", true];
t = [42, "hello"];
t = [42];
```

* `--strictNullChecks` 모드에서, `?`는 `undefined`를 동시에 포함함.



