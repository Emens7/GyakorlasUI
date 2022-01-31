# DOM gyakorló feladatok:

Feladatok webes felhasználói felület programozásának a gyakorlásához.

## Alapok:

Elemek, vezérlők kiválasztása:

```js
//A submit-button azonosítójú elem kiválasztása
const btn = document.querySelector('#submit-button');

//Több elem kiválasztása osztálynév alapján
const items = document.querySelectorAll('li.todo-item');
```

A document.querySelector() függvény CSS szelektorokat használ.

Eseménykezelő függvények regisztrálása:

```js
    const btn = document.querySelector('#submit-button');
    //Regisztrálunk egy eseménykezelőt, amely a btn-re való kattintást "figyeli", ha a felhasználó megnyomja a gombot a böngésző meghívja a megadott függvényt.
    btn.addEventListener('click', () => {
        console.log('Hi!');
    });
```

## Feladatok:

1. Kérjük be egy felhasználó nevét egy beviteli mezőbe és üdvözöljük például egy alert-el.

2. Számoljuk ki egy felhasználó által megadott (helyezzünk el hozzá két számbeviteli mezőt és egy gombot az oldalon) téglalap kerületét és területét, majd jelenítsük meg az oldalon!

3. Adott a következő konténer:

    ```html
    <div id="color" style="width: 500px; height: 500px;"></div>
    ```
    Helyezzünk el az oldalon egy színválasztó mezőt (`<input type="color">`) és ha megváltozik a kiválasztott szín (`input` esemény), akkor színezzük a div-et(háttérszín) a kiválasztott színűre.

4. Kérjünk be a felhasználótól számokat egy szövegbeviteli mezőbe vesszővel elválasztva, majd egy gomb lenyomására számoljuk ki a megadott számok átlagát és jelenítsük meg az átlagot két tizedesjegyre kerekítve a gomb alatt. Ha ezzel készen vagyunk, próbáljuk meg ellenőrizni, hogy a felhasználó valóban számokat adott-e meg, és ha nem akkor jelenítsünk meg hibaüzenetet (pl.: alert-el)

5. Helyezzünk el egy jelszóbeviteli mezőt az oldalon és folyamatosan ellenőrizzük a tartalmát miközben a felhasználó gépel (a jelszó legalább 6, de legfeljebb 12 karakter hosszú lehet, és tartalmaznia kell legalább egy számot). Ha a jelszó nem megfelelő azt azonnal jelezzük piros szöveggel a beviteli mező alatt. Ha a jelszó helyes zöld szöveggel jelezzük a felhasználónak szintén a mező alatt. A visszajelzés automatikusan frissüljön miközben a felhasználó gépel, de amíg a felhasználó nem nyúlt a mezőhöz ne jelenjen meg visszajelzés.

6. Készítsünk egy felületet, ahol egy tetszőleges fotóra lehet alkalmazni csúszkával állítható szűrőket (sepia, kontraszt, szaturáció, stb.), egyszerre akár többet is. Ez egy összetetteb feladat lehet elsőre, az is elég, ha egy szűrőt megcsinálunk és később visszatérünk a feladatra. A feladathoz használjunk [CSS filtereket](https://developer.mozilla.org/en-US/docs/Web/CSS/filter).

    [Minta](https://1drv.ms/v/s!AhgIdtoaigtclR6FX5IfvTaBYlCu?e=aIP945)

7. Adott egy termékeket tartalmazó lista. Jelenítsük meg egy listában (ul) az oldalon a termékeket az árukkal együtt, majd a lista alatt írjuk ki a teljes összeget (összegezzük az árakat).

    ```js
        const products = [
            {
                name: 'Képkeret',
                price: 1800
            },
            {
                name: 'Asztali lámpa',
                price: 12549
            },
            {
                name: 'Fotel',
                price: 35500
            },
            {
                name: 'Puff (80x40)',
                price: 16900
            },
            {
                name: 'TV-asztal',
                price: 10500
            }
        ];
    ```
    Ha ezzel megvagyunk akkor tegyük lehetővé, hogy új termékeket lehessen hozzáadni a listához az árukkal együtt, ha hozzáadtunk egy terméket kerüljön a lista aljára és a teljes összeg is frissüljön, a beviteli mezőket pedig állítsuk üresre. Ellenőrizzük a bevitt adatokat, az ár kötelező és nem lehet negatív, a termék neve pedig legalább két karakter kell, hogy legyen.

8. Kérjünk be szöveget a felhasználótól egy beviteli mezőbe, majd egy gomb lenyomására jelenítsük meg a szöveget megfordítva a mező alatt (például `abc -> cba`).

9. Készítsünk egy egyszerű "szerencsekerék" alkalmazást, amelyben különböző elemeket (nevek, lehetőségek, stb.) vehetünk fel egy listába egy szövegmező és egy gomb segítségével, majd egy másik gombra kattintva véletlenszerűen kiválasztunk egy elemet a listából és megjelenítjük az oldalon.

10. Jelenítsünk meg a [kettő n-edik hatványait](https://en.wikipedia.org/wiki/Power_of_two) n = 0-tól n = 15-ig, az első oszlopban a kitevők legyenek, a másodikban pedig a hatványok.

    Minta:
    | n  | 2^n |
    | -- | --  |
    | 0  | 1   |
    | 1  | 2   |
    | 2  | 4   |
    | 3  | 8   |
    | .. | ..  |

11. Adott egy mátrix, jelenítsük meg táblázatos formában:

    ```js
        const matrix = [
            [1, 4, 3, 7],
            [0, 12, 22, 24],
            [32, 24, 52, 67],
            [72, 45, 32, 77]
        ];
    ```
    Ha ez kész, akkor tegyük lehetővé egy gombbal a mátrix transzponálását (a sorok és oszlopok felcserélése), nem kell feltétlenül elvégezni a memóriában tárolt mátrixon a műveletet, elég ha transzponálva jelenítjük meg a mátrixot a táblázatban.

12. Készítsünk egy oldalt, ahol lekérdezhetjük, hogy egy adott irányítószámhoz, milyen település tartozik. Az adatokat lekérdezhetjük ajax kérésekkel a [zippopotam.us](https://zippopotam.us/) API használatával. Példa: `https://api.zippopotam.us/hu/8634`. Helyezzünk el az oldalon egy szövegmezőt, amibe be lehet írni az irányítószámot és egy gombot, amire kattintva megtörténik a lekérdezés és megjelenik a település neve és a megye neve. Ha az irányítószám nem létezik az adatbázisban azt jelezzük a felhasználónak.

    Az API-tól kapott válaszból kiolvashatjuk a település koordinátáit is, ezek segítségével jelenítsünk meg egy Bing térképet iframe-ben.
    Példa:
    ```html
    <iframe
        id="map"
        src="https://www.bing.com/maps/embed?h=400&w=500&cp=50~20&lvl=13"
        width="500"
        height="400"
    ></iframe>
    ```