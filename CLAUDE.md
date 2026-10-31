# Trgoimpex W – sajt

Redizajn sajta za Trgoimpex W, porodičnu građevinsku firmu iz Novog Sada (ograđivanje placeva, asfaltiranje, iskopi, niskogradnja, visokogradnja, inženjering). Vlasnik projekta: Dragan Zec. Komunikacija na srpskom (latinica).

## Struktura

Statičan sajt, bez build koraka i bez biblioteka. Svaka stranica je jedan HTML fajl sa CSS-om u `<style>` i inline stilovima.

- `index.html` – početna (hero, Naše delatnosti, Odabrani projekti, O firmi, Kontakt sa formom)
- `projekti.html` – lista projekata
- `o-nama.html` – priča, delatnosti, brojke
- `kontakt.html` – kontakt podaci i forma
- `images/` – fotografije (webp)

Pokretanje: otvori `index.html` u pregledaču, ili `npx serve .` za lokalni server. Hosting je planiran na Cloudflare Pages.

Repozitorijum: https://github.com/cze45/trgoimpex-w-sajt (privatan). Dizajn kanvas sa istim stranicama: https://claude.ai/artifact/WhoPn9e5KpXhWtbLVcbUPa; izmene napravljene na kanvasu treba ručno preneti u HTML fajlove.

## Grid

- Kontejner `max-width: 1240px` sa `padding: 0 24px` (sadržaj širok 1240px). Zaglavlje i hero imaju `box-sizing: border-box`, pa tamo stoji `1288px`.
- 12 kolona, razmak 24px (klase `.g12`, `.g3`, `.g4` u `<style>`); elementi se postavljaju sa `grid-column`.
- Razdelne linije između kolona idu u sredinu razmaka (`.vr`, pseudo-element na `left: -12px`), da tekst ostane na liniji kolone.
- Ispod 900px grid prelazi u jednu kolonu, a fotografije idu iznad teksta (`.ph`).

## Brend

- Bordo (akcija, akcenat): `#6b0f1a`, hover `#500b14`
- Tamnoplava (tekst, tamne površine, podnožje): `#1b2e3c`
- Plava: `#2b4162` (sekcija Kontakt na kontakt.html, podnožje na početnoj), tamnija `#20324d` (sekcije Odabrani projekti i Kontakt na početnoj)
- Sive: `#556171` (sporedni tekst), `#c5ceda` (tekst na tamnom), `#d8dde2` (linije), `#f3f4f5` (svetle sekcije)
- Bela: `#fefefe`
- Font: Montserrat (Google Fonts), težine 400/500/600/800; Oswald 500 samo za nazive u sekciji „Naše delatnosti“
- Zaobljenje uglova: 4px
- Logo: tamnoplavi oblik + bordo „W“ na belom, ceo beo na tamnom. Naziv uvek „TRGOIMPEX W“ sa `translate="no"`.

## Pravila

- Bordo reč u naslovu sekcije samo na svetlim pozadinama.
- Naslovi sekcija normalnim slovima; velikim slovima samo glavni naslov u hero sekciji, nazivi na karticama projekata i nazivi delatnosti.
- Svaka animacija mora imati `prefers-reduced-motion` varijantu.
- Linkovi i dugmad min. 44px za dodir; vidljiv `:focus-visible`.
- Ne izmišljati podatke o firmi (brojke, reference, recenzije) – pitati Dragana.

## Otvoreno pre objave

- Forme rade preko `mailto:`; treba ih povezati sa Formspree ili Cloudflare Workerom.
- Instagram, Facebook i „Politika privatnosti“ vode na `#` – potrebni pravi linkovi.
- Fotografije su delom privremene (ista hala se koristi više puta, iskop i inženjering nemaju svoje slike).
- Proveriti tekstove opisa delatnosti i brojke (20+, 180+, 15+) sa klijentom.
- Sekcija „Naše delatnosti“ je mreža 3 × 2 (2 kolone na tabletu, 1 na telefonu) sa ikonicom, nazivom i kratkim opisom, bez animacije. Ikonice su ručno crtane SVG linije, 40px.
- Dizajn sistem „Trgoimpex W“ (https://claude.ai/artifact/V5NfqLMSvpkTRBDpWXR7jZ) je povezan sa kanvasom, ali se ne primenjuje na stranice; Dragan je odbio stranice prepravljene po njemu.
