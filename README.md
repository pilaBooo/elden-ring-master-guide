# Elden Ring Master Guide — V6.480 (GitHub CLEAN)

Hrvatski Elden Ring Master Guide za GitHub Pages. Ova distribucija sadrzi samo datoteke potrebne za javnu stranicu, plus ovaj README.

## Struktura

- `index.html` — glavni vodic i NPC Tracker
- `assets/` — 29 slika karata; **mapa vec postoji u ZIP-u**
- `.nojekyll` — omogucava jednostavno objavljivanje putem GitHub Pages
- `README.md` — ove upute; ne prikazuje se u vodicu

## Postavljanje na GitHub Pages

1. Raspakiraj ZIP. Nemoj posebno stvarati `assets`: mapa nastaje raspakiravanjem.
2. U repozitoriju `pilabooo.github.io` zamijeni postojeci `index.html`.
3. Prenesi mapu `assets` **sa svim slikama** tako da putanje ostanu `assets/map-01.png` itd. Ako vec postoji mapa `assets`, zamijeni njezine datoteke odgovarajucima iz ZIP-a.
4. Dodaj `README.md`. Dodaj `.nojekyll` ako vec nije u repozitoriju.
5. GitHub Pages mora objavljivati iz korijena odgovarajuce grane (`/root`). Pricekaj objavu i osvjezi Safari stranicu.

**Napomena za iPhone:** GitHubovo web sucelje na mobitelu moze ogranicavati prijenos cijelih mapa. Nemoj uploadati ZIP kao jednu datoteku i ocekivati da ce se raspakirati. Ako se `assets` ne moze prenijeti kao mapa, upotrijebi racunalo s GitHub web prijenosom (drag-and-drop raspakirane mape) ili Git aplikaciju koja podrzava commit direktorija. Ako su sve karte vec u postojecoj `assets` mapi, nije ih potrebno ponovno prenositi ako su iste.

## Testiranje

**Prvo izvezi JSON sigurnosnu kopiju napretka.** Testiraj na drugom profilu.

1. Otvori stranicu; provjeri navigaciju i ucitavanje svih karata.
2. Oznaci i odznaci NPC korak; provjeri osvjezavanje NPC Trackera.
3. Sellen GOLD/RED: suprotna grana treba biti vizualno prigusena; istovremene odluke trebaju upozorenje.
4. Millicent GOLD: RED alternativa treba biti prigusena; NG+ napomena vidljiva.
5. Seluvis: provjeri STOP za Magic Scorpion Charm.
6. Dung Eater: pocetni koraci ne smiju lazno potvrditi zavrsnu nagradu.
7. Promijeni profil; provjeri odvojenost napretka.
8. Izvezi JSON, promijeni testnu kvacicu, uvezi JSON i provjeri vracanje stanja i Trackera.

## Vazno

Ova CLEAN verzija ne mijenja NPC logiku u odnosu na V6.480. Uklonjene su razvojne AUDIT/CSV datoteke iz distribucije, ne izvorne kontrole iz internog radnog arhiva. Uvodni testovi nisu zamjena za funkcionalno testiranje u pregledniku.


## V6.482 — Blaidd tracker
Jedinstvena READ-ONLY Blaidd kartica, 14 referentnih redaka, s postojećim Walkthrough kvačicama gdje postoje. Koraci bez vlastite kvačice označeni su kao nepraćeni; nisu automatski potvrđeni.


V6.484: Blaidd - tracked walkthrough checkpoints; existing IDs preserved.
