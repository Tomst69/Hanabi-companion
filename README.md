# Hanabi Notebook

Jednoduchá appka do prohlížeče na sledování možností karet ve hře Hanabi.
Žádný build, žádné závislosti ke stažení — je to jeden soubor `index.html`,
který si prohlížeč umí sám celý stáhnout a spustit (React, Babel a Tailwind
se načtou z CDN, jakmile appku otevřeš).

## Jak to spustit lokálně hned teď

Stačí dvakrát kliknout na `index.html` — otevře se v prohlížeči a appka
funguje (je potřeba internet, protože se z CDN stahuje React/Babel/Tailwind).

## Jak to dostat na GitHub (přes web, bez příkazové řádky)

1. Jdi na [github.com](https://github.com) a přihlas se (nebo si založ účet).
2. Vpravo nahoře klikni na **+** → **New repository**.
3. Zadej název, např. `hanabi-notebook`, nastav ho jako **Public**, nic dalšího
   nezaškrtávej, a klikni **Create repository**.
4. Na stránce nového repozitáře klikni na **uploading an existing file**
   (nebo **Add file → Upload files**).
5. Přetáhni tam soubor `index.html` z této složky.
6. Dole klikni **Commit changes**.

## Jak to zpřístupnit jako veřejnou appku (GitHub Pages)

1. V repozitáři jdi do **Settings** (nahoře v menu repozitáře).
2. Vlevo klikni na **Pages**.
3. U **Branch** vyber `main` a složku `/ (root)`, klikni **Save**.
4. Počkej cca minutu, obnov stránku — nahoře se objeví odkaz typu
   `https://tvoje-jmeno.github.io/hanabi-notebook/`.
5. Tenhle odkaz si ulož/přidej na plochu telefonu (Sdílet → Přidat na plochu) —
   appka pak funguje jako normální ikonka.

## Jak to dostat na GitHub přes příkazovou řádku (pokud preferuješ git)

```bash
cd hanabi-notebook-repo
git init
git add index.html README.md
git commit -m "Hanabi notebook"
git branch -M main
git remote add origin https://github.com/TVOJE-JMENO/hanabi-notebook.git
git push -u origin main
```

Pak už jen zapni GitHub Pages podle kroků výše.

## Poznámky k appce

- Data (rozsvícené/vyloučené barvy a čísla) se ukládají do `localStorage`
  prohlížeče na daném zařízení — nejsou nikde sdílená ani synchronizovaná.
- Klepnutí na barvu/číslo = "může to být tohle".
  Dvojklik do 0,5 s = "tohle to nemůže být".
- Appka nepotřebuje žádný backend ani databázi.
