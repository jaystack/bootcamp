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
    1) `Symbol`
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
    const o1 = { a: 1, b: { c: 2 } }
    const o2 = { ...o1, a: 2 }
    o1.b.c = 3
    console.log(o2)
    ```
    1) `{ a: 1, b: { c: 2 } }`
    1) `{ a: 2, b: { c: 2 } }`
    1) `{ a: 1, b: { c: 3 } }`
    1) `{ a: 2, b: { c: 3 } }`
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
    1) `delete o.a`
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
1) Mely állítások igazak a `.map(f)` függvényre?
    1) Leképezi a tömböt egy másik tömbre az `f` függvény alapján.
    1) Az `f` ugyanazzal a típussal kell visszatérjen, mint a tömb elemeinek a típusa.
    1) Az újonnan előállt tömb hossza megegyezik a kiinduló tömbbel.
    1) A `.map()` mutálja a tömböt, amin meghívjuk.
1) Mely állítások igazak a `.filter(p)` függvényre?
    1) Szűri a tömb elemeit az `p` függvény alapján.
    1) Az `p` függvény egy predikátum.
    1) Az újonnan előállt tömb hossza megegyezik a kiinduló tömb hosszával.
    1) Az újonnan előállt tömb elemeinek a típusa megegyezik a kiinduló tömb elemeinek a típusával.
    1) A `.filter()` mutálja a tömböt, amin meghívjuk.
1) Mely állítások igazak a `.reduce(r[, i])` függvényre?
    1) Az `r` függvény egy reducer.
    1) Ha nem adunk meg `i` paramétert, akkor az első akkumulált állapot a tömb első eleme lesz.
    1) Az `r` függvény olyan típussal kell visszatérjen, mint ami az `i` típusa.
    1) Az `r` függvény olyan típussal kell visszatérjen, mint a tömb elemeinek a típusa.
    1) Az eredmény mindig egy tömb lesz.
1) Mit logol az alábbi snippet?
    ```js
    const f = (a = 10) => { console.log(a) }
    f()
    ```
    1) `undefined`
    1) `10`
1) Mit logol az alábbi snippet?
    ```js
    const f = (a = 10) => { console.log(a) }
    f(5)
    ```
    1) `5`
    1) `10`
1) Mit logol az alábbi snippet?
    ```js
    const f = (a = 10) => { console.log(a) }
    f(undefined)
    ```
    1) `undefined`
    1) `10`
1) Mit logol az alábbi snippet?
    ```js
    const f = (a = 10) => { console.log(a) }
    f(null)
    ```
    1) `undefined`
    1) `null`
    1) `10`
1) Mit logol az alábbi snippet?
    ```js
    const f = (...args) => { console.log(args) }
    f(10, 20, 30)
    ```
    1) `[ 10, 20, 30 ]`
    1) `10 20 30`
1) Mit logol az alábbi snippet?
    ```js
    const f = (...args) => { console.log(...args) }
    f(10, 20, 30)
    ```
    1) `[ 10, 20, 30 ]`
    1) `10 20 30`
1) Mit logol az alábbi snippet?
    ```js
    const f = (first, ...others) => { console.log([ first, ...others ]) }
    f(...[10, 20], 30)
    ```
    1) `[ 10, 20, 30 ]`
    1) `10 20 30`
1) Mit logol az alábbi snippet?
    ```js
    const f = (...args) => { console.log(args[0]) }
    f()
    ```
    1) `[]`
    1) `undefined`
1) Mit logol az alábbi snippet?
    ```js
    const foo = 'bar'
    console.log({ [foo]: 'foo' })
    ```
    1) `{ foo: 'foo' }`
    1) `{ bar: 'foo' }`
    1) `{ foo: 'bar' }`
1) Mit logol az alábbi snippet?
    ```js
    const name = 'pista'
    console.log({ name })
    ```
    1) `{ name: 'name' }`
    1) `{ name: 'pista' }`
    1) `{ pista: 'pista' }`
    1) Hibát dob
1) Melyik esetben lesz a `this` undefined?
    1) `{ f() { console.log(this) } }`
    1) `{ f: function() { console.log(this) } }`
    1) `{ ['f']: function() { console.log(this) } }`
    1) `{ f: () => { console.log(this) } }`
1) Mit logol az alábbi snippet?
    ```js
    const name = 'pista'
    const s = `My name is ${name}!`
    console.log(s)
    ```
    1) `My name is ${name}!`
    1) `My name is pista!`
1) Mit logol az alábbi snippet?
    ```js
    for (const a in [10, 20, 30])
        console.log(a)
    ```
    1)
        - `10`
        - `20`
        - `30`
    1)
        - `0`
        - `1`
        - `2`
1) Mit logol az alábbi snippet?
    ```js
    for (const a of [10, 20, 30])
        console.log(a)
    ```
    1)
        - `10`
        - `20`
        - `30`
    1)
        - `0`
        - `1`
        - `2`
1) Igaz-e a `[ 10, 20, 30 ].includes(20)`
    1) Igen
    1) Nem
1) Igaz-e a `[ 10, 20, 30 ].includes('20')`
    1) Igen
    1) Nem
1) Igaz-e a `[ [], {} ].includes({})`
    1) Igen
    1) Nem
1) Igaz-e a `[ [ 10, 20 ] ].includes(20)`
    1) Igen
    1) Nem
1) Igaz-e a `Symbol === Symbol` kifejezés
    1) Igen
    1) Nem
1) Igaz-e a `Symbol() === Symbol()` kifejezés
    1) Igen
    1) Nem
1) Igaz-e a `Symbol('alma') === Symbol('alma')` kifejezés
    1) Igen
    1) Nem
1) Igaz-e a `Symbol('alma') == Symbol('alma')` kifejezés
    1) Igen
    1) Nem
1) Mit logol az alábbi snippet?
    ```js
    const A = Symbol()
    const B = Symbol()
    console.log(A === B)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const A = Symbol()
    const B = A
    console.log(A === B)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    let A = Symbol()
    let B = A
    A = Symbol()
    console.log(A === B)
    ```
    1) `true`
    1) `false`
1) Igaz-e a `Number.isFinite(0)` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `Number.isFinite(1)` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `Number.isFinite(Infinity)` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `Number.isFinite(null)` kifejezés?
    1) Igen
    1) Nem
1) Igaz-e a `Number.isFinite(undefined)` kifejezés?
    1) Igen
    1) Nem
1) Mit logol az alábbi snippet?
    ```js
    const items = [
        { id: 0 },
        { id: 1 },
        { id: 2 },
        { id: undefined },
        { id: null },
        {}
    ]
    console.log(items.filter(item => item.id))
    ```
    1) `[ { id: 0 }, { id: 1 }, { id: 2 }, { id: undefined }, { id: null }, {} ]`
    1) `[ { id: 0 }, { id: 1 }, { id: 2 }, { id: undefined }, { id: null } ]`
    1) `[ { id: 0 }, { id: 1 }, { id: 2 } ]`
    1) `[ { id: 1 }, { id: 2 } ]`
1) Mit logol az alábbi snippet?
    ```js
    const items = [
        { id: 0 },
        { id: 1 },
        { id: 2 },
        { id: undefined },
        { id: null },
        {}
    ]
    console.log(items.filter(item => Number.isFinite(item.id)))
    ```
    1) `[ { id: 0 }, { id: 1 }, { id: 2 }, { id: undefined }, { id: null }, {} ]`
    1) `[ { id: 0 }, { id: 1 }, { id: 2 }, { id: undefined }, { id: null } ]`
    1) `[ { id: 0 }, { id: 1 }, { id: 2 } ]`
    1) `[ { id: 1 }, { id: 2 } ]`
1) Mit logol az alábbi snippet?
    ```js
    const [a, b, c] = [ 10, 20, 10 ]
    console.log(a === c)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const [a, ...b] = [ 10, 20, 10 ]
    console.log(a, b)
    ```
    1) `10 20 30`
    1) `10 [ 20, 30 ]`
1) Mit logol az alábbi snippet?
    ```js
    const [ , [a] ] = [ 10, [ 20, 30 ] ]
    console.log(a)
    ```
    1) `[ 20, 30 ]`
    1) `20`
1) Mit logol az alábbi snippet?
    ```js
    const [ , [...a] ] = [ 10, [ 20, 30 ] ]
    console.log(a)
    ```
    1) `[ 20, 30 ]`
    1) `20`
1) Mit logol az alábbi snippet?
    ```js
    const { a } = { a: 1, b: 2 }
    console.log(a)
    ```
    1) `{ a: 1 }`
    1) `1`
1) Mit logol az alábbi snippet?
    ```js
    const { ...a } = { a: 1, b: 2 }
    console.log(a)
    ```
    1) `{ a: 1 }`
    1) `{ a: 1, b: 2 }`
1) Mit logol az alábbi snippet?
    ```js
    const { b, ...a } = { a: 1, b: 2 }
    console.log(a)
    ```
    1) `{ a: 1 }`
    1) `{ a: 1, b: 2 }`
1) Mit logol az alábbi snippet?
    ```js
    const { a: b } = { a: 1, b: 2 }
    console.log(a)
    ```
    1) `1`
    1) `{ a: 1 }`
    1) `{ b: 2 }`
    1) `undefined`
1) Mit logol az alábbi snippet?
    ```js
    const { a: b } = { a: 1, b: 2 }
    console.log(b)
    ```
    1) `1`
    1) `2`
1) Mit logol az alábbi snippet?
    ```js
    const { b: { c } } = { a: 1, b: { c: 2 } }
    console.log(c)
    ```
    1) `1`
    1) `2`
    1) `{ c: 2 }`
1) Mit logol az alábbi snippet?
    ```js
    const { a, b: { c: d } } = { a: 1, b: { c: 2 } }
    console.log(a, d)
    ```
    1) `1 2`
    1) `2 2`
    1) `1 { c: 2 }`
1) Mit logol az alábbi snippet?
    ```js
    const s = new Set([ 10 ])
    s.add('alma')
    s.add('körte')
    s.add(10)
    s.add('alma')
    console.log(...s)
    ```
    1) `[ 10, 'alma', 'körte', 10 ]`
    1) `[ 10, 'alma', 'körte', 10, 'alma' ]`
    1) `[ 10, 'alma', 'körte', 'alma' ]`
    1) `[ 10, 'alma', 'körte' ]`
1) Mit logol az alábbi snippet?
    ```js
    const m = new Map()
    m.set('k', 'v')
    console.log(m.get('k'))
    ```
    1) `k`
    1) `v`
1) Mit logol az alábbi snippet?
    ```js
    const token = 'abc-xyz-123'
    const m = new Map()
    m.set(token, a => b => a + b)
    console.log(m.get(token)(10)(20) === 30)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const token = 'abc-xyz-123'
    const m = new Map()
    m.set(token, a => b => a + b)
    console.log(m.get(token)(10, 20) === 30)
    ```
    1) `true`
    1) `false`
1) Igaz-e a `Promise.resolve(10) === 10`
    1) Igen
    1) Nem
1) Igaz-e a `Promise.resolve(10) == 10`
    1) Igen
    1) Nem
1) Mit logol az alábbi snippet?
    ```js
    Promise.resolve(10)
        .then(n => n + 1)
        .then(n => console.log(n))
    ```
    1) `10`
    1) `11`
1) Mit logol az alábbi snippet?
    ```js
    Promise.resolve(10)
        .then(n => Promise.resolve(n + 1))
        .then(n => console.log(n))
    ```
    1) `10`
    1) `11`
    1) `NaN`
1) Mit logol az alábbi snippet?
    ```js
    Promise.reject(new Error('hiba'))
        .then(n => n + 1)
        .then(n => console.log(n))
    ```
    1) `10`
    1) `11`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    Promise.reject(new Error('hiba'))
        .then(n => n + 1)
        .then(n => console.log(n))
        .catch(e => console.log(e.message))
    ```
    1) `10`
    1) `11`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    Promise.reject(new Error('hiba'))
        .then(n => n + 1)
        .catch(e => {})
        .then(() => 10)
        .then(n => console.log(n))
    ```
    1) `10`
    1) `11`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    new Promise((resolve, reject) => reject(new Error('hiba')))
        .then(n => n + 1)
        .then(n => console.log(n))
        .catch(e => console.log(e.message))
    ```
    1) `10`
    1) `11`
    1) `10 hiba`
    1) `11 hiba`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    new Promise(resolve => resolve(new Error('hiba')))
        .then(_ => _)
        .then(e => console.log(e.message + '!'))
        .catch(e => console.log(e.message))
    ```
    1) `hiba`
    1) `hiba!`
1) Mit logol az alábbi snippet?
    ```js
    new Promise(resolve => resolve(10))
        .then(async n => n + 1)
        .then(n => Promise.resolve(n + 1))
        .then(n => console.log(n))
    ```
    1) `10`
    1) `11`
    1) `12`
1) Mit logol az alábbi snippet?
    ```js
    new Promise(resolve => resolve(10))
        .then(async n => { throw new Error('hiba') })
        .then(n => Promise.resolve(n + 1))
        .then(n => console.log(n))
    ```
    1) `10`
    1) `11`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    new Promise(resolve => resolve(10))
        .then(async n => { throw new Error('hiba') })
        .then(n => Promise.resolve(n + 1))
        .then(n => console.log(n))
        .catch(e => e)
        .catch(e => console.log(e.message))
    ```
    1) `10`
    1) `11`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    new Promise(resolve => resolve(10))
        .then(async n => { throw new Error('hiba') })
        .then(n => Promise.resolve(n + 1))
        .then(n => console.log(n))
        .catch(e => { throw e })
        .catch(e => console.log(e.message))
    ```
    1) `10`
    1) `11`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    const f = async n => n + 1
    console.log(f(10) === 11)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const f = async () => 10
    const g = async h => await h()
    g(f).then(n => console.log(n === 10))
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const f = async () => {
        throw new Error('hiba')
        return 10
    }

    f()
        .then(n => console.log(n))
        .catch(e => console.log(e.message))
    ```
    1) `10`
    1) `undefined`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    const f = async () => { throw new Error('hiba') }

    const g = async () => {
        try {
            f()
            console.log(10)
        } catch (e) {
            console.log(e.message)
        }
    }

    g()
    ```
    1) `10`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    const f = async () => { throw new Error('hiba') }

    const g = async () => {
        try {
            await f()
            console.log(10)
        } catch (e) {
            console.log(e.message)
        }
    }

    g()
    ```
    1) `10`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    const f = async () => { throw new Error('hiba') }

    const g = async () => {
        try {
            await Promise.reject(new Error('hiba'))
            console.log(10)
        } catch (e) {
            console.log(e.message)
        }
    }

    g()
    ```
    1) `10`
    1) `hiba`
    1) semmit
1) Mit logol az alábbi snippet?
    ```js
    const f = async () => { throw new Error('hiba') }

    const g = async () => {
        try {
            await new Promise((resolve, reject) => reject(new Error('hiba')))
            console.log(10)
        } catch (e) {
            console.log(e.message)
        }
    }

    g()
    ```
    1) `10`
    1) `hiba`
    1) semmit