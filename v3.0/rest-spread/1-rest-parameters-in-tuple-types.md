# 1\) rest parameters in tuple types

* rest 형태의 파라미터를 작성시에, 해당 type들을 나열 가능
* 나머지 변수들에 대한 개별 type 설정 가

```javascript
declare function foo(...args: [number, string, boolean]): void;
declare function foo(args_0: number, args_1: string, args_2: boolean): void;
```

