# Prvi koraci s Pandocom

Učimo kako koristiti pandocom.
Trajanje = 25 minuta

Provjereno s Pandocom 3.14 na VS Codiumu sa Git Bashom.

## Prije početka

- Requirements:
    VS Code/VS Codium
    Git Bash terminal
    datoteka - README.md

## 1. Instalirajte Pandoc

### Windows

    Otvorite službenu stranicu za preuzimanje: https://pandoc.org/installing.html
    Preuzmite instalacijski paket za Windows (.msi) ili ZIP arhivu ako na računalu nemate administratorske ovlasti.
    Ako koristite instalacijski paket, pokrenite ga i slijedite upute instalacijskog čarobnjaka.
    Ako radite na računalu u učionici i koristite ZIP arhivu:
    Preuzmite Windows ZIP arhivu s izvršnom datotekom Pandoca.
    Raspakirajte je u mapu kojoj imate pristup, primjerice C:\Tools\Pandoc.
    Provjerite da se u raspakiranoj mapi nalazi datoteka pandoc.exe.
    Dodajte mapu koja sadrži pandoc.exe u korisničku varijablu okruženja Path. U Windowsima otvorite Edit environment variables for your account, odaberite varijablu Path, kliknite Edit → New i unesite putanju do mape.
    Spremite promjene i zatvorite postavke.
    Zatvorite i ponovno otvorite Git Bash kako bi prepoznao novu vrijednost varijable Path.

### macOS

    Otvorite službenu stranicu za preuzimanje: https://pandoc.org/installing.html
    Preuzmite instalacijski paket za macOS (.pkg) koji odgovara vašem računalu.
    Otvorite preuzetu datoteku i slijedite upute instalacijskog čarobnjaka.
    Otvorite Terminal ili terminal u VS Codiumu. Ako je potrebno, zatvorite ga i ponovno otvorite nakon instalacije.

## 2. Provjerite instalaciju

```bash
pandoc --version
```

**Očekivani rezultat:**

pandoc 3.13
Features: +server +lua
Scripting engine: Lua 5.4
User data directory: C:\Users\Pc\AppData\Roaming\pandoc
Copyright (C) 2006-2025 John MacFarlane. Web:  https://pandoc.org
This is free software; see the source for copying conditions. There is no
warranty, not even for merchantability or fitness for a particular purpose.

## 3. Pretvorite Markdown u Word

    pandoc README.md -o README.docx

    Očekivani rezultat: u mapi projekta pojavljuje se nova datoteka README.docx. Otvorite je u Microsoft Wordu ili kompatibilnom programu i provjerite jesu li naslov, podnaslovi, odlomci, popisi i blokovi koda pretvoreni u odgovarajuće elemente dokumenta.

    Datoteka README.md ostaje nepromijenjena.

## 4. Pretvorite Markdown u web-stranicu

    pandoc README.md -s -o README.html
    Očekivani rezultat: u istoj mapi pojavljuje se datoteka README.html. Otvorite je u web-pregledniku i provjerite prikazuju li se naslovi, odlomci i popisi kao na jednostavnoj web-stranici.

## Ako ne radi

| Poruka | Što znači | Što učiniti |

|command not found|Git Bash ne može pronaći izvršnu datoteku Pandoca.|Provjerite je li Pandoc instaliran i nalazi li se njegova mapa u varijabli PATH. Ponovno otvorite terminal i pokušajte opet.|

|pandoc is not recognized as an internal or external command|Windows terminal ne prepoznaje naredbu Pandoc.|Provjerite instalaciju i varijablu Path. Ako ste koristili ZIP arhivu, dodajte odgovarajuću mapu u Path.|

|pandoc: README.md: openBinaryFile: does not exist ili slična poruka|Datoteka README.md nije pronađena na trenutačnoj lokaciji.|Naredbom pwd provjerite trenutačnu mapu, a naredbom ls pregledajte njezin sadržaj. Otvorite ispravnu mapu ili navedite punu putanju do datoteke.|

|Datoteka .docx ili .html nije vidljiva|Izlazna datoteka možda je spremljena u drugu mapu ili pretvorba nije uspjela.|Provjerite poruke u terminalu i potražite datoteku u trenutačnoj radnoj mapi.|

|Word dokument ne izgleda kao Markdown|Markdown se pretvara u Wordove stilove, a ne zadržava nužno identičan izgled uređivača.|Provjerite strukturu izvornog dokumenta. Za prilagodbu izgleda možete naknadno koristiti Wordove stilove ili Pandoc predložak.|

## Što ste napravili

Naučili ste provjeriti instalaciju Pandoca i pretvoriti Markdown datoteku u Word dokument i HTML web-stranicu. Upoznali ste osnovnu strukturu naredbe pandoc, opciju -o za određivanje izlazne datoteke i opciju -s za izradu cjelovitog HTML dokumenta. Sada možete koristiti istu izvornu Markdown datoteku za izradu različitih formata dokumenata.git
