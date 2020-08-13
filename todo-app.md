# Fullstack TODO app

Készíts egy egyszerű fullstack TODO appot, ami egy
- **node api**-ból
- és egy **react alkalmazás**ból áll.

## Node API

Egyszerű express rest service, ami az alábbi végpontokkal rendelkezik:
- `GET /todos` - visszaadja az összes TODOt
- `GET /todos/:id` - visszaadja az id-val megjelölt TODOt
- `POST /todos` - készít egy új TODOt, a payload HTTP body-ban érkezik és visszaadja az új TODOt
- `PUT /todos/:id` - módosít egy TODOt, a payload HTTP body-ban érkezik, és visszaadja az új TODOt
- `DELETE /todos/:id` - töröl egy TODOt

---

- Lehetőleg ne bajlódjunk adatbázisokkal. Egyszerű inmemory tárolás elegendő.

## React app

Egyszerű react app (`create-react-app`-pal készítve):
- Lista az aktuális TODOkról. A listában lehetőség van módosításra és törlésre.
- Felette egy gomb, amivel készíthetünk újat.
- Új todo hozzáadásakor vagy meglévő módosításakor legyen valamilyen Save gomb, ami elindítja a requestet.
- A többi a fantáziádra van bízva... :)

---

- Állapotkezelés történjen Redux-szal!
- Nem kell designolással bajlódni. Ha nagyon igyényes vagy, szépítheted, de +pont nem jár érte :)
- Ha jártas vagy a react hook-ok használatában, akkor kérlek használj hookokat!

## Extraságok

- Ha van kedved és időd, készíthetsz egy keresőt is backend támogatással. A kereséshez ne kelljen Entert ütni vagy gombot nyomni. Ha a felhasználó abbahagyja a gépelést, akkor mehet automatikusan a keresés az api felé. Erre a célra használd a `GET /todos` végpontot egy opcionális `q` query paraméterrel.

## Instrukciók

- Ha ismered a TypeScript-et, nyugodtan használd!
- Ha jártas vagy a funkcionális patternek használatában, akkor itt kiélheted magad :) Lényeg, hogy ne mutálj!
- Ne bonyolítsd túl az alkalmazás funkcióit! Inkább a patternekre koncentrálunk :)
