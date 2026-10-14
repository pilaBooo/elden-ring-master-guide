V6.363: NPC Tracker now shows per-character progress meters derived from the existing shared Walkthrough checkboxes; no new storage keys, routes or map changes. Browser functional verification pending.

V6.362: NPC Tracker sada uključuje i NPC kvačice unutar upozoravajućih callout okvira (Patches, Gatekeeper Gostoc, Roderika u CH1). Status se dijeli s Walkthroughom; postojeći identifikatori nisu mijenjani. Funkcionalni test u pregledniku nije proveden.

# V6.350 – NPC identitet i kronološko grupiranje

- Ispravljeno grupiranje ponovljenih NPC susreta: Yura (3 koraka), Boc (2), Varré (2), Roderika/Hewg (2), Nepheli/Gideon (2), Rogier/Fia (2), Renna/Ranni (2).
- Postojeće kvačice i identifikatori ostaju nepromijenjeni.
- Prikaz i dalje obuhvaća samo 22 NPC callouta s kvačicama; potpuna dopuna CH1–CH26 nije završena.
- Razvojna verzija; za igranje koristiti potvrđenu V6.345.

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


V6.346: NPC Tracker first-stage cleanup: existing NPC task list and branch rewards prioritized, old audit panels moved to collapsed archive at runtime. No checkbox identifiers or storage format changed. NPC task consistency across all chapters remains pending.


V6.347: First chronological NPC tracker: existing walkthrough NPC callouts are mirrored read-only in order; two missing NPC callout checkboxes added. The full CH1-CH26 NPC checkpoint conversion remains pending.


## V6.348 — NPC tracker checkbox mirror
NPC Tracker sada prikazuje kvačicu na svakom postojećem povezanom NPC koraku. Klik na kvačicu prosljeđuje promjenu originalnoj kvačici u Walkthroughu, bez drugog ključa spremanja. Ovaj prolaz još ne pokriva NPC napomene koje nemaju originalni zadatak niti kompletno grupiranje po liku. Funkcionalni test na iPhoneu još nije proveden.


V6.349: NPC tracker now groups existing shared-checkbox NPC callouts by character in first Walkthrough encounter order. Does not yet cover all NPC milestones in CH1-26.


## V6.351 — NPC checkbox expansion
Added shared Walkthrough/Tracker NPC checkboxes for: Irina, D, Hunter of the Dead, Kenneth Haight, Blaidd / Mistwood, Thops: dovrši odmah. These are standalone NPC actions, not caution notes. Existing data-id based persistence retained. Not yet a complete CH1–CH26 audit.


V6.352: Added 27 NPC quest checkpoint checkboxes to existing chronological walkthrough NPC asides; shared with NPC tracker via data-id, without changing PSN numbers. Development version; functional browser test pending.


V6.353: NPC tracker now includes standalone NPC aside steps with data-npc-task checkboxes, not just .callout.npc; original walkthrough inputs remain source of truth. Functional browser test pending.


V6.354: NPC tracker adds chronological per-character task sequence, completed styling, and filter for unfinished tasks. Uses the same walkthrough checkboxes and profile state; no new progress keys.


## V6.355 — NPC identiteti i pretraga
- Razdvojeni su zasebni NPC likovi Sellen/Jerren, Millicent/Gowry, Corhyn/Goldmask, Roderika/Hewg, Nepheli/Gideon, Rogier/Fia i Edgar/Irina gdje naslov koraka dopušta razlučivanje.
- Pretraga otvara karticu s pronađenim zadatkom.
- Nisu dodane nove kvačice; preostali NPC događaji i višeznačni naslovi zahtijevaju daljnju reviziju.


## V6.357 – NPC razgovori (razvojna verzija)
Dodano 6 NPC kvačica za postojeće dijaloge u Liurniji/Jarburgu: npc-v357-boc-lake-facing, npc-v357-thops-irith, npc-v357-patches-liurnia, npc-v357-hyetta-purified, npc-v357-jarbairn-jarburg, npc-v357-boc-east-gate. Ne mijenjati PSN numeraciju. Provjeriti na uređaju prije korištenja za igranje.


V6.358: NPC Tracker sada obuhvaća postojeće NPC kvačice u div i aside okvirima, uključujući starije formate; uklonjeno filtriranje koje je preskakalo div NPC korake bez bold oznake NPC. Prošireno prepoznavanje identiteta za Melina, Miriel, Iji, Tanith, Albus i Three Fingers. Razvojna verzija, funkcionalni test potreban.


## V6.361 — šest postojećih NPC kontrolnih točaka
Dodane su zajedničke Walkthrough/Tracker kvačice za D (Roundtable), Thops (Church of Irith), Jar-Bairn (Jarburg), Fia (Roundtable), Alexander (Radahn Festival) i Fia (nakon Champions). Bez promjene PSN numeracije. Nove kvačice treba funkcionalno testirati prije uporabe kao glavne verzije.
