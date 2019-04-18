# 2\) Generic rest parameters

* rest 매개변수를 배열 형식으로 Generic 형태에서 사용 가능

```typescript
declare function bind<T, U extends any[], V>(f: (x: T, ...args: U) => V, x: T): (...args: U) => V;

declare function f3(x: number, y: string, z: boolean): void;

const f2 = bind(f3, 42);  // (y: string, z: boolean) => void
const f1 = bind(f2, "hello");  // (z: boolean) => void
const f0 = bind(f1, true);  // () => void

f3(42, "hello", true);
f2("hello", true);
f1(true);
f0();
```

