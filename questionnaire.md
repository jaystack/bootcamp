1) Melyik állítás igaz?
    1) A Javascript-et jellemzően gépi kódra fordítjuk és binárisokat állítunk elő belőle.
    1) A Javascript egy interpreter által futtatott nyelv, amelynek az értelmezése runtime történik.
1) Az alábbi típusok közül melyek primitívek?
    1) `Object`
    1) `String`
    1) `Boolean`
    1) `Date`
    1) `Number`
    1) `Array`
    1) `RegExp`
1) Mit logol az alábbi snippet?
    ```js
    const o1 = { a: { b: 1 } }
    const o2 = o1
    o2.a.b = 2
    console.log(o1.a.b)
    ```
    1) `1`
    1) `2`
1) Mit logol az alábbi snippet?
    ```js
    const o1 = { a: 1 }
    const o2 = o1
    o2.a = 2
    console.log(o1.a)
    ```
    1) `1`
    1) `2`
1) Mit logol az alábbi snippet?
    ```js
    let a1 = [ 10, 20, 30 ]
    let a2 = a1
    a2.push(40)
    console.log(a1)
    ```
    1) `[ 10, 20, 30 ]`
    1) `[ 10, 20, 30, 40 ]`
1) Dob-e hibát az alábbi snippet?
    ```js
    let a = [ 10, 20, 30 ]
    a.push(40)
    ```
    1) Igen
    1) Nem
1) Dob-e hibát az alábbi snippet?
    ```js
    const a = [ 10, 20, 30 ]
    a.push(40)
    ```
    1) Igen
    1) Nem
1) Dob-e hibát az alábbi snippet?
    ```js
    const a = [ 10, 20, 30 ]
    a = [ 10, 20, 30, 40 ]
    ```
    1) Igen
    1) Nem
1) Mit logol az alábbi snippet?
    ```js
    const o1 = { a: 1, b: 2 }
    const o2 = { ...o1, b: 3, c: 4 }
    o1.a = 2
    console.log(o2)
    ```
    1) `{ a: 1, b: 3, c: 4 }`
    1) `{ a: 2, b: 3, c: 4 }`
    1) `{ a: 1, b: 2, c: 4 }`
1) Mit logol az alábbi snippet?
    ```js
    const a1 = [ 10, 20, 30 ]
    const a2 = [ 50, ...a1, 40, ...a1 ]
    a1[0] = 0
    console.log(a2)
    ```
    1) `[ 50, 0, 20, 30, 40, 0, 20, 30 ]`
    1) `[ 50, 10, 20, 30, 40, 10, 20, 30 ]`
1) Mi az alábbi kifejezés értéke?
    ```js
    [ ...[3, 4, 5], 6 ]
        .map(x => x**2)
        .filter(x => x%2)
        .reduce((s, x) => s + x)
    ```
    1) `34`
    1) `36`
    1) `52`
1) Az alábbi snippetek közül melyek kifejezések?
    1) `const a = 1`
    1) `[ 10, 20, 30 ]`
    1) `[ 10, 20, 30 ].map(x => x**2)`
    1) `throw new Error('hiba')`
    1) `return 10`
    1) `if (cond) return 1; else return 2;`
    1) `cond ? 1 : 2`
    1) `[ ...[ 10, 20, 30 ] ]`
    1) `{ ...{ a: 1, b: 2 } }`
    1) `export default 10`
    1) `() => { const a = 1 }`
    1) `class A extends B {}`
    1) `function f() {}`
    1) `cond1 === cond2`
    1) `a + b + 1000`
1) Mi az értéke a `10 && 20` kifejezésnek?
    1) `20`
    1) `true`
1) Mi az értéke a `!!0` kifejezésnek?
    1) `0`
    1) `false`
    1) `true`
1) Mi az értéke a `10 && '' ? 'alma' : 'körte'` kifejezénsek?
    1) `'alma'`
    1) `'körte'`
1) Mi az értéke a `0 || 1` kifejezénsek?
    1) `true`
    1) `false`
    1) `1`
1) Igaz-e a `0 === false` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `0 == false` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `'' === false` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `'' == false` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `{ a: 1 } === { a: 1 }` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `{} == {}` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `[ 'alma' ] === [ 'alma' ]` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `[] == []` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `x => x + 1 === x => x + 1` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `() => {} == () => {}` kifejezés?
    1) Igen
    1) Nem
1) Mit logol az alábbi snippet?
    ```js
    const o = {
        f() { return this; }
    }
    console.log(o === o.f())
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const o1 = {
        a: 10,
        f() { return this.a; }
    }
    const o2 = {}
    o2.f = o1.f
    console.log(o2.f() === 10)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const o1 = {
        a: 10,
        f() { return this.a; }
    }
    const o2 = {}
    o2.f = o1.f.bind(o1)
    console.log(o2.f() === 10)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const o1 = {
        a: 10,
        f() { return this.a; }
    }
    const o2 = {}
    o2.f = o1.f
    console.log(o2.f.call(o1) === 10)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const o = {
        a: 10,
        f: () => { return this.a }
    }
    console.log(o.f())
    ```
    1) `10`
    1) `undefined`