# Mila · A-frame Zlatibor

Statični sajt za glamping A-frame kućicu Mila na Zlatiboru (srpski i engleski).

## Fajlovi

- `index.html` – početna stranica
- `utisci.html` – stranica sa svim utiscima gostiju
- `utisci.json` – utisci gostiju (podaci)
- `.nojekyll` – GitHub Pages da ne obrađuje fajlove kroz Jekyll

## Objavljivanje na GitHub Pages

1. Napravi novi repozitorijum na GitHub-u (npr. `mila-zlatibor`).
2. Otpremi sve fajlove iz ovog foldera u koren repozitorijuma (Add file → Upload files). Uključi i `.nojekyll`.
3. Settings → Pages → Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)** → Save.
4. Za minut-dva sajt je na `https://<korisničko-ime>.github.io/mila-zlatibor/`.

## Podešavanja (u `index.html`, deo `CONFIG` na dnu)

```js
phone: "+381 6x xxx xxxx",   // broj za prikaz
whatsapp: "",                // isti broj samo cifre, npr. 381641234567
email: "info@mila-zlatibor.rs",
priceWeek: 8000,             // RSD po noći, ned–čet
priceWeekend: 10000,         // RSD po noći, pet i sub
minNights: 2
```

## Dodavanje utisaka (`utisci.json`)

```json
[
  {
    "ime": "Ime gosta",
    "mesto": "Grad",
    "datum": "2026-09",
    "ocena": 5,
    "tekst": "Utisak na srpskom.",
    "tekst_en": "Optional English translation."
  }
]
```

Početna prikazuje 4 najnovija utiska (po polju `datum`), a `utisci.html` sve.

## Lokalno testiranje

Utisci se učitavaju iz `utisci.json`, što pregledač ne dozvoljava kad se fajl otvori direktno sa diska.
Pokreni mali server u ovom folderu i otvori http://localhost:8000:

```
python3 -m http.server 8000
```
