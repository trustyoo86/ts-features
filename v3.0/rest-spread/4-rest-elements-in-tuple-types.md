# 4\) rest elements in tuple types

* 튜플 유형의 마지막 요소는 `...X` 형식의 나머지 type으로 정의될 수 있음
* X는 배열의 유형\[number, ...string\[\]\]은 number 요소 뒤에 나머지 요소들에 string type 정의 가능함

```typescript
function tuple<T extends any[]>(...args: T): T {
    return args;
}

const numbers: number[] = getArrayOfNumbers();
const t1 = tuple("foo", 1, true);  // [string, number, boolean]
const t2 = tuple("bar", ...numbers);  // [string, ...number[]]
```

