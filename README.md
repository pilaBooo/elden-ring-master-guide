# Elden Ring Master Guide V6.231 — GitHub Pages

Upload **index.html**, **.nojekyll** and the entire **assets/** folder to the repository root.
Enable GitHub Pages (Deploy from a branch, main / root).

The `index.html` uses relative image paths `assets/map-XX.png`; do not rename or omit them.
The separate V6.229 HTML remains the self-contained offline version; `index.html` in this package is NOT self-contained.

**Progress:** browser localStorage is per origin. Export JSON backup from your current guide, then import it on the deployed site. Keep a second copy of your JSON backup.

This build has passed structural checks and JS syntax checks; it has not been tested in iPhone Safari or on a live GitHub Pages deployment.


V6.233: plutajući gumb karte prati aktivnu oznaku Tu sam; ispravljen odabir karte za CH3–CH26.


## V6.340 — plan funkcionalne regresijske provjere (dva profila)

Ova verzija ne mijenja spremanje napretka ni identifikatore kvačica. Dodan je precizan
postupak provjere prije proglašavanja dvaju profila potpuno funkcionalnima.

1. Na Profilu A označi jednu obaveznu kvačicu nezavršene PSN rute. Provjeri status rute.
2. Prebaci na Profil B: ista kvačica mora ostati neoznačena, a ruta nezavršena.
3. Označi drugi zadatak na Profilu B, vrati se na A: obje vrijednosti moraju ostati odvojene.
4. Na Profilu A označi Legendary predmet; Itemi mora pokazati promjenu samo na A.
5. Provjeri boss trofej u Trofeji, a zatim NPC izbor i suprotnu NG+ nagradu.
6. Osvježi stranicu i ponovi prebacivanje A/B; oba profila moraju zadržati svoje stanje.
7. Provjeri da opcionalni zadatak ne blokira završavanje PSN rute.
8. Izvezi zasebnu JSON sigurnosnu kopiju prije stvarnog igranja ili objave.

**Kriterij prolaza:** nema prelijevanja kvačica ili odluka između profila;
Tracker statusi odgovaraju kvačicama aktivnog profila i ostaju točni nakon reload-a.

**Status:** strukturna provjera ZIP-a i sintaksna provjera JavaScripta provedene.
Funkcionalni test u Chromiumu/iPhone Safariju još nije potvrđen; ne označavati ga kao PASS.


V6.343: Zaštita dijagnostike starih CH9–11 profilnih ključeva od iznimke pri blokiranom localStorage; prikazuje upozorenje umjesto prekida. Nije mijenjano spremanje ni profilni podaci. Browser test je blokiran pravilima okruženja.


## V6.345 – Prvi korisnički test (smoke test)

Testiraj na stvarnoj GitHub Pages adresi (ne kao lokalni file://), u istom pregledniku i bez privatnog načina rada. Prije testiranja napravi sigurnosnu kopiju napretka ako vodič nudi izvoz.

1. Otvori profil A i označi jednu prethodno neoznačenu kvačicu; zapamti CH i korak.
2. Prebaci se na profil B: ta kvačica mora ostati neoznačena.
3. Vrati se na profil A: kvačica mora biti označena.
4. Ponovno učitaj stranicu i potvrdi da je kvačica profila A ostala označena.
5. U profilu B označi drugu kvačicu, prebaci se na A pa opet na B; oba napretka moraju biti odvojena.
6. Provjeri prikazuju li NPC, Itemi i Trofeji stanje aktivnog profila.
7. Nemoj resetirati poglavlja ili brisati podatke tijekom ovog testa.

Ako nešto ne radi, zabilježi profil, CH, PSN korak, očekivani i stvarni rezultat te screenshot.

Programska izmjena V6.345: zaštita upisa markera automatskog napredovanja u CH2 kada preglednik onemogući localStorage. Nije izvršen funkcionalni test preglednika.
