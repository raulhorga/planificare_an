# Notițele noastre · v2

Aplicație mobile-first cu aspect de carnet de notițe. **Lista comună** se deschide implicit; butonul și ecranul Acasă au fost eliminate. Pe desktop există navigare în lateral, iar pe mobil o bară de navigare fixă jos.

Editorul de notițe permite text liber și autosalvare în foaia de cumpărături / ToDo. Checklist-urile, categoriile, listele Raul și Andreea, camerele casei, istoricul DONE cu dată și oră, traducerea RO/EN și exportul CSV rămân disponibile.

## Foi EtherCalc

- Cumpărături, activități și notițe: https://calc.domainepublic.net/0yku9i1un5nf
- De avut în casă: https://calc.domainepublic.net/ewi97w9qa7ks

## Publicare

Publică `index.html`, `styles.css`, `app.js`, `manifest.webmanifest` și `icon.svg` în același director al unui hosting HTTPS, cum ar fi GitHub Pages. După actualizare, reîncarcă pagina dacă browserul a păstrat fișiere vechi în cache.

**Limitare:** sincronizarea directă depinde de permisiunile CORS ale serverului EtherCalc și de formatul datelor. Codul refuză să suprascrie foi care au o structură necunoscută. Nu a fost efectuat un test live de scriere în foile utilizatorului.



## Categorii direct în editorul de notițe
În **Lista comună**, pune cursorul pe un rând sau selectează textul dorit și apasă **Categorie** pentru a-l transforma într-un titlu **bold și subliniat**. Apasă **Text normal** ca să revii la un paragraf obișnuit. Formatarea și textul sunt salvate automat în același rând EtherCalc ca înainte (coloana `notes`, cu prefixul `HTML_NOTE_V1:`). Notițele vechi sunt compatibile. Dacă editezi manual rândul notiței direct în EtherCalc, păstrează acest prefix și structura HTML pentru a conserva formatarea.
