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

## Brend

- Bordo (akcija, akcenat): `#6b0f1a`, hover `#500b14`
- Tamnoplava (tekst, tamne površine, podnožje): `#1b2e3c`
- Plava (sekcije Odabrani projekti i Kontakt): `#2b4162`
- Sive: `#556171` (sporedni tekst), `#c5ceda` (tekst na tamnom), `#d8dde2` (linije), `#f3f4f5` (svetle sekcije)
- Bela: `#fefefe`
- Font: Montserrat (Google Fonts), težine 400/500/600/800
- Zaobljenje uglova: 4px
- Logo: tamnoplavi oblik + bordo „W“ na belom, ceo beo na tamnom. Naziv uvek „TRGOIMPEX W“ sa `translate="no"`.

## Pravila

- Bordo reč u naslovu sekcije samo na svetlim pozadinama.
- Naslovi sekcija normalnim slovima; velikim slovima samo glavni naslov u hero sekciji i nazivi na karticama projekata.
- Svaka animacija mora imati `prefers-reduced-motion` varijantu.
- Linkovi i dugmad min. 44px za dodir; vidljiv `:focus-visible`.
- Ne izmišljati podatke o firmi (brojke, reference, recenzije) – pitati Dragana.

## Otvoreno pre objave

- Forme rade preko `mailto:`; treba ih povezati sa Formspree ili Cloudflare Workerom.
- Instagram, Facebook i „Politika privatnosti“ vode na `#` – potrebni pravi linkovi.
- Fotografije su delom privremene (ista hala se koristi više puta, iskop i inženjering nemaju svoje slike).
- Proveriti tekstove opisa delatnosti i brojke (20+, 180+, 15+) sa klijentom.
- Sekcija „Naše delatnosti“ na računaru pomera kartice vodoravno dok se skroluje (CSS scroll-driven animations, Chrome/Edge); u ostalim pregledačima i na telefonu je vodoravna traka koja se prevlači.
