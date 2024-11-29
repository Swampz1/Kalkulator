**README for Kalkulator**

Kalkulator er en enkel og brukervennlig kalkulatorapplikasjon skrevet i Python med hjelp av biblioteket tkinter. Applikasjonen er laget for å være enkel å bruke og tilby en rekke funksjoner for å utføre matematiske operasjoner.

**Installasjon**

For å kjøre denne applikasjonen, må du ha Python installert på din datamaskin. Du kan laste ned Python fra https://www.python.org/downloads/.

Når Python er installert, kan du installere tkinter-biblioteket ved å kjøre følgende kommando i terminalen (eller kommandolinjen):

```
pip install tk
```

**Kjøring av applikasjonen**

For å kjøre applikasjonen, åpne en terminal, naviger til mappen der du har lastet ned `main.py`, og kjør følgende kommando:

```
python main.py
```

**Bruk av kalkulator**

Når applikasjonen kjøres, vil du se et vindu med en kalkulator.

Du kan bruke tallknappene (0-9) og operasjonsknappene (+, -, *, /, %, C, ±, .) til å skrive inn uttrykk og utføre beregninger.

- Tallknappene (0-9) legger til tall i resultatfeltet.
- Operasjonsknappene (+, -, *, /, %, C, ±, .) utfører de tilhørende matematiske operasjonene.
- Knappen "C" tømmer resultatfeltet.
- Knappen "%" beregner prosenten av det forrige tallet.
- Knappen "±" bytter mellom positivt og negativt tall.
- Knappen "." legger til desimalpunkt i tallet.
- Knappen "=" utfører beregningen og viser resultatet i resultatfeltet.

**Import-funksjoner**

- `tkinter`: Dette er hovedbiblioteket for å lage GUI-applikasjoner i Python.
- `ttk`: Dette er en modifisert versjon av tkinter som tilbyr en mer moderne og enkel å bruke stil for GUI-komponenter.

**Ekstra informasjon**

- Denne applikasjonen støtter bare grunnleggende matematiske operasjoner (+, -, *, /) og ikke avanserte funksjoner som faktorisering, kvadratroting osv.
- Applikasjonen har ikke noe feilhåndtering for ulovlige uttrykk, slik som divisjon med null. Du bør være forsiktig med å skrive inn gyldige uttrykk.
