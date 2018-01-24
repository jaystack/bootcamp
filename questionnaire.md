1) Melyik állítás igaz?
    1) A Javascript-et jellemzően gépi kódra fordítjuk és binárisokat állítunk elő belőle.
    1) A Javascript egy interpreter által futtatott nyelv, amelynek az értelmezése runtime történik.
1) Az alábbi típusok közül melyek primitívek (melyek adódnak át érték szerint)?
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
    try {
        let a = JSON.parse(JSON.stringify({ b: 1 }))
    } catch (error) {
        let a = null
    }
    console.log(a)
    ```
    1) `1`
    1) `{ b: 1 }`
    1) `null`
    1) semmit, hibát dob
1) Mit logol az alábbi snippet?
    ```js
    let a
    try {
        a = JSON.parse(JSON.stringify({ b: 1 }))
    } catch (error) {
        a = null
    }
    console.log(a)
    ```
    1) `1`
    1) `{ b: 1 }`
    1) `null`
    1) semmit, hibát dob
1) Mit logol az alábbi snippet?
    ```js
    try {
        var a = JSON.parse(JSON.stringify({ b: 1 }))
    } catch (error) {
        var a = null
    }
    console.log(a)
    ```
    1) `1`
    1) `{ b: 1 }`
    1) `null`
    1) semmit, hibát dob
1) Mit logol az alábbi snippet?
    ```js
    try {
        const a = JSON.parse(JSON.stringify({ b: 1 }))
    } catch (error) {
        const a = null
    }
    console.log(a)
    ```
    1) `1`
    1) `{ b: 1 }`
    1) `null`
    1) semmit, hibát dob
1) Mit logol az alábbi snippet?
    ```js
    const a = null
    try {
        a = JSON.parse(JSON.stringify({ b: 1 }))
    } catch (error) { }
    console.log(a)
    ```
    1) `1`
    1) `{ b: 1 }`
    1) `null`
    1) semmit, hibát dob
1) Mit logol az alábbi snippet?
    ```js
    const a = null
    a = JSON.parse(JSON.stringify({ b: 1 }))
    console.log(a)
    ```
    1) `1`
    1) `{ b: 1 }`
    1) `null`
    1) semmit, hibát dob
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
    1) `new Date()`
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
1) Igaz-e a `x => x + 1 === x => x + 1` kifejezés?
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
    const o = {
        a: 10,
        f() { return this.a; }
    }
    const f = o.f
    console.log(f() === 10)
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
        f() { return this.a; }
    }
    const f = o.f.bind(o)
    console.log(f() === 10)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const o = {
        a: 10,
        f() { return this.a; }
    }
    const f = o.f
    console.log(f.call(o) === 10)
    ```
    1) `true`
    1) `false`
1) Mit logol az alábbi snippet?
    ```js
    const o = {
        a: 10,
        f: () => { return this.a }
    }
    console.log(o.f() === 10)
    ```
    1) `true`
    1) `false`
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
    1) Az `r` függvény olyan típussal kell (célszerű) visszatérjen, mint ami az `i` típusa.
    1) Az `r` függvény olyan típussal kell (célszerű) visszatérjen, mint a tömb elemeinek a típusa.
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
1) Melyik függvény logol `false`-t?
    1) `const o = { f() { console.log(o === this) } }`
    1) `const o = { f: function() { console.log(o === this) } }`
    1) `const o = { ['f']: function() { console.log(o === this) } }`
    1) `const o = { f: () => { console.log(o === this) } }`
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
1) Mivel tér vissza egy `async` függvény?
    1) Önmagával
    1) Promise-szal
    1) A visszatérési értékével
1) Mit old fel az `await`?
    1) Promise-t
    1) Mindent triviálisan felold, de ha Promise-t kap, akkor megvárja annak a resolve-ját
    1) HTTP request-eket
1) Mivel tér vissza egy generátor?
    1) Iterátorral
    1) Az első kilépési pontjának értékével
    1) A visszatérési értékével
1) Mit logol az alábbi snippet?
    ```js
    const g = function*() {
        yield 10
        return 20
    }
    console.log(g())
    ```
    1) `10`
    1) `20`
    1) `{ value: 10, done: false }`
    1) `{ value: 20, done: true }`
    1) Egy generátort
1) Mit logol az alábbi snippet?
    ```js
    const g = function*() {
        yield 10
        return 20
    }
    const i = g()
    i.next()
    console.log(i.next())
    ```
    1) `10`
    1) `20`
    1) `{ value: 10, done: false }`
    1) `{ value: 20, done: true }`
1) Mit logol az alábbi snippet?
    ```js
    const g = function*(p) {
        const a = yield p
        return a + 20
    }
    const i = g(10)
    i.next()
    console.log(i.next(20))
    ```
    1) `{ value: 10, done: false }`
    1) `{ value: 20, done: true }`
    1) `{ value: 30, done: true }`
    1) `{ value: 40, done: true }`
1) Mit logol az alábbi snippet?
    ```js
    const g = function*(p) {
        const a = yield p
        return a + 20
    }
    const i = g(10)
    console.log(i.next(i.next().value))
    ```
    1) `{ value: 10, done: false }`
    1) `{ value: 20, done: true }`
    1) `{ value: 30, done: true }`
    1) `{ value: 40, done: true }`
1) Mit logol az alábbi snippet?
    ```js
    const g = function*(p) {
        try {
            const a = yield p
            console.log(a)
        } catch (e) {
            console.log(e.message)
        }
    }
	const i = g(10)
    i.next()
	i.throw(new Error('hello'))
    ```
    1) `10`
    1) `{ value: 10, done: false }`
    1) `{ value: 10, done: true }`
    1) `hello`
1) Mit nevezünk egy függvény a kontextusának (context)?
    1) A blokk, ami a függvényt tartalmazza
    1) Az objektum, ami függvényt tartalmazza
    1) A függvény argumentumainak összessége
1) Mi a scope?
    1) Egy olyan láthatósági tartomány, amiben a változók elérhetőségét értelmezzük
    1) Egy objektum, amire a `this` mutat
    1) Egy osztály, amire a `this` mutat
1) Mire mutat a `this`?
    1) A függvény kontextusára
    1) A függvény scopejára
    1) Egy metódus osztályára
1) Mit osztályoz az OOP osztály?
    1) Az objektumokat
    1) A metódusokat
    1) A névtereket
1) Milyen osztálynak nevezzük azt, amit kizárólag csak egyszer példányosítunk?
    1) abstract
    1) static
    1) singleton
    1) private
1) Milyen osztálynak nevezzük azt, amit nem lehet példányosítani?
    1) abstract
    1) static
    1) singleton
    1) private
1) Hogy nevezzük azt az osztályt, amiből egy osztály származik?
    1) Gyermek
    1) Ős
    1) Példány
1) Hogy nevezzük azt az osztály, ami egy osztályból származik?
    1) Gyermek
    1) Ős
    1) Példány
1) Mi a prototípus?
    1) Egy olyan osztály, amiből származtatunk
    1) Egy olyan objektum, amit példányosításkor reassignolunk
1) Mi a konstruktor?
    1) Egy függvény, ami példányosításkor fut le
    1) Egy függvény, ami örökléskor fut le
1) Mit nevezünk static függénynek/metódusnak?
    1) Az osztálynak egy olyan függvénye, amit csak az osztály láthat
    1) Az osztálynak egy olyan függvénye, ami nem példányhoz kötött
    1) Az osztálynak egy olyan függvénye, ami még nincs implementálva
1) Mit nevezünk abstract függvénynek/metódusnak?
    1) Az osztálynak egy olyan függvénye, amit csak az osztály láthat
    1) Az osztálynak egy olyan függvénye, ami nem példányhoz kötött
    1) Az osztálynak egy olyan függvénye, ami még nincs implementálva
1) Mit nevezünk metódus override-nak?
    1) Az őshöz képest egy osztály metódusainak felüldefiniálását.
    1) Az gyermek osztály metódusainak első definiálását.
1) Mit logol az alábbi snippet?
    ```js
    class A {
        static a = 10
        a = 20

        static f() {
            console.log(this.a)
        }

        f() {
            console.log(this.a)
        }
    }

    A.f()
    ```
1) Mit logol az alábbi snippet?
    ```js
    class A {
        static a = 10
        a = 20

        static f() {
            console.log(this.a)
        }

        f() {
            console.log(this.a)
        }
    }

    new A().f()
    ```
1) Mit logol az alábbi snippet?
    ```js
    class A {
        constructor() {
            console.log('hello')
            this.f()
        }

        f() {
            console.log('hali')
        }
    }

    new A().f()
    ```
    1) `hello`
    1) `hali`
    1) `hello` és `hali`
    1) `hello` és `hali` és `hali`
1) Mit logol az alábbi snippet?
    ```js
    class A {
        static a = 10
        static f() {
            console.log(this.a)
        }

        a = 20

        constructor() {
            this.constructor.f()
        }

        f() {
            console.log(this.a)
        }
    }

    new A()
    ```
    1) `10`
    1) `20`
1) Mit logol az alábbi snippet?
    ```js
    class A {
        static a = 10
        static f() {
            console.log(this.a)
        }

        a = 20

        constructor() {
            this.f()
        }

        f() {
            console.log(this.a)
        }
    }

    new A()
    ```
    1) `10`
    1) `20`
1) Mit logol az alábbi snippet?
    ```js
    class A {
        f() {
            console.log('hello')
        }
    }

    class B extends A {
        f() {
            console.log('hali')
        }
    }

    new B().f()
    ```
    1) `hello`
    1) `hali`
    1) `hello` és `hali`
1) Mit logol az alábbi snippet?
    ```js
    class A {
        f() {
            console.log('hello')
        }
    }

    class B extends A {
        f() {
            super.f()
            console.log('hali')
        }
    }

    new B().f()
    ```
    1) `hello`
    1) `hali`
    1) `hello` és `hali`
1) Mit logol az alábbi snippet?
    ```js
    class A {
        a = 10

        f(p) {
            this.a = this.a + p
        }
    }

    class B extends A {
        f(p) {
            super.f(p)
            this.a = this.a + p
            console.log(this.a)
        }
    }

    new B().f(20)
    ```
    1) `30`
    1) `40`
    1) `50`
1) Mit logol az alábbi snippet?
    ```js
    class A {
        constructor(p) {
            this.a = p
        }
    }

    class B extends A {
        constructor(p) {
            super(p + 10)
            console.log(this.a)
        }
    }

    new B(30)
    ```
    1) `10`
    1) `30`
    1) `40`
1) Mit logol az alábbi snippet?
    ```js
    class A {
        static f() {
            return 10
        }

        constructor(p) {
            this.a = p
        }

        f() {
            return 20
        }
    }

    class B extends A {
        static f() {
            return super.f() + 1
        }

        constructor(p1, p2) {
            super(4)
            console.log(
                p1 +
                p2 +
                super.constructor.f() +
                this.constructor.f() +
                super.f() +
                this.f() +
                this.a
            )
        }

        f() {
            return super.f() + 2
        }
    }

    new B(A.f(), B.f())
    ```
    1) `10`
    1) `20`
    1) `22`
    1) `44`
    1) `84`
    1) `88`
1) Mikor érdemes OOP osztályt definiálni?
    1) Logikai egységbe tudunk vele rendezni függvényeket.
    1) Állapottal rendelkező objektumot/objektumokat tudunk velük konstruálni, mely állapoton/állapotokon műveleteket tudunk végezni.
    1) Típusokat definiálhatunk, amelyek között származási kapcsolatokat tudunk definiálni.
1) Mi a különbség az *interface* és az *osztály* között?
    1) Az interface egy típus, az osztály pedig egy típushoz kötött műveleteket definiál.
    1) Az osztály egy típus, az interface pedig egy típushoz kötött műveleteket definiál.
1) Mi a különbség az *expression* (kifejezés) és a *statement* között?
    1) Az expression kiértékelhető, a statement elvégezhető.
    1) Az expression elvégezhető, a statement kiértékelhető.
1) Mi az a *pure function*?
    1) Olyan függvény, amelyben csak szabad paraméterek vannak.
    1) Olyan függvény, amelyben nincsenek szabad paraméterek.
    1) Olyan determinisztikus függvény, amely ugyanazon inputra mindig ugyanazt az outputot produkálja.
1) Mit nevezünk szabad paraméternek?
    1) A függvény scope-jában definiált változó.
    1) A függvény egy argumentuma, aminek nincs default értéke.
    1) A függvényen belül egy olyan változó, ami a függvény scope-jában és argumentumai közt sincs definiálva.
1) Mi a capturing?
    1) Szabad paraméter felüldefiniálása.
    1) Szabad paraméter megkötése.
    1) Szabad paraméter elhagyása.
1) Mit logol az alábbi snippet?
    ```js
    const f = a => b => a + b
    console.log(f(10, 20))
    ```
    1) `10`
    1) `20`
    1) `30`
    1) Egy függvényt
1) Mit logol az alábbi snippet?
    ```js
    const f = (a, b) => a + b
    console.log(f.bind(null, 10))
    ```
    1) `10`
    1) `20`
    1) `30`
    1) Egy függvényt
1) Mit jelent a magasabb rendű függvény?
    1) Egy osztálynak olyan tagfüggvénye, amely az osztály tulajdonságait képes megváltoztatni.
    1) Olyan függvény, amely más függvények meghívásával határozza meg saját visszatérési értékét.
    1) Olyan függvény, amely paraméterül kap egy másik függvényt és/vagy egy másik függvénnyel tér vissza.
1) Mit logol az alábbi snippet?
    ```js
    const f = h => p => h(p)
    const g = p => p + 1
    console.log(f(g)(10))
    ```
    1) `10`
    1) `11`
    1) Egy függvényt
1) Mi a closure?
    1) Olyan kifejezés, amelyben a szabad paraméterek rejtettek a külvilág számára.
    1) Egy osztálynak olyan metódusa, amely private tag-ok értékét adja vissza.
    1) Olyan változó, amelynek értékéhez nem lehet hozzáférni.
1) Mit logol az alábbi snippet?
    ```js
    const createIdGenerator = () => {
        let id = 0
        return () => ++i
    }
    const getId = createIdGenerator()
    getId()
    console.log(getId())
    ```
    1) `0`
    1) `1`
    1) `2`
1) Mi a currying lényege?
    1) A többváltozós függvények leírhatóak egyváltozós függvények closure-jeként.
    1) Függvények közvetlen meghívása helyett azokat átadjuk egy másik függvénynek, hogy az hívja meg őket.
1) Mit jelent az immutábilitás?
    1) `var` és `let` helyett mindig `const`-ot használunk.
    1) Nem írunk felül és nem törlünk semmit a memoriában. A nem használt allokációkat a Garbage Collector-ra bízzuk.
    1) Csak a heap-en módosítunk adatot, a stack-en soha.
1) Melyik nem igaz a NEM tisztán funkcionális kódra?
    1) Immutable
    1) Lazy
    1) Determinisztikus
    1) Könnyen párhuzamosítható
    1) Könnyen tesztelhető
1) Melyik állítás igaz a mellékhatásokra?
    1) Indeterminisztikus
    1) Determinisztikus
    1) Csak aszinkron lehet
1) Az alábbiak közül melyek mellékhatások?
    1) Fájlművelet
    1) Hálózati kommunikáció
    1) Promise
    1) Idő
    1) Exception
    1) Standard output
    1) Véletlen
    1) Hardware megszakítás
    1) Closure
    1) Környezeti változó
1) Az alábbi kifejezések közül melyek mellékhatások?
    1) `new Promise((resolve, reject) => resolve(10))`
    1) `Promise.reject()`
    1) `Promise.resolve()`
    1) `fetch('/users')`
    1) `db.find({ a: 1 })`
    1) `fs.writeFile('hello.txt', 'hello')`
    1) `fs.writeFileSync('hello.txt', 'hello')`
    1) `new Error('hiba')`
    1) `setTimeout(() => 1, 1000)`
    1) `setInterval(() => 1)`
    1) `Date.now()`
    1) `new Date()`
    1) `new Date('2018-01-01')`
    1) `Math.random()`
    1) `console.log('hello')`
    1) `window.clientWidth`
    1) `window.location`
    1) `window.navigator`
    1) `new window.Worker()`
    1) `process.env`
    1) `process.stdout`