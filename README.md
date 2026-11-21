# Weekend Journal — calendar anual RO / EN

Aplicație web statică, pornind de la aplicația „Notițele noastre” și inspirată de calendarele pe hârtie din fotografiile atașate.

## Utilizare

Deschide `index.html` dintr-un server web HTTPS (de exemplu GitHub Pages, Netlify sau alt hosting static). Publică **toate** fișierele în același director. Pentru test local se poate rula `python3 -m http.server 8000` în director și apoi accesa `http://localhost:8000`.

- 12 luni pe an, navigare în orice an (1900–2200), vedere detaliată și listă cronologică
- Zilele de weekend evidențiate; clic pe orice zi pentru adăugare
- Eveniment, loc, tip, planificat/realizat, notițe, editare și ștergere
- Filtrare, statistici, export CSV, traducere RO/EN, mod luminos/întunecat, interfață mobilă
- Date locale salvate în browser; sincronizare cu EtherCalc la pornire, după modificări și periodic

## EtherCalc

Foaie configurată: https://calc.domainepublic.net/glo9m1jolj7l

Antetul CSV utilizat este:

`record_type,id,date,title,place,type,status,notes,updated_at,deleted`

La prima folosire, aplicația poate popula o **foaie goală**. Dacă foaia există și are alt format, aplicația **nu o suprascrie**. Pentru siguranță, exportă periodic un CSV. Importul este realizat prin `PUT /_/glo9m1jolj7l`, iar verificarea prin `GET /_/glo9m1jolj7l/csv`. Suportul CORS și permisiunile de scriere ale serverului pot bloca sincronizarea directă. În această situație, datele rămân în stocarea locală și pot fi exportate CSV.

**Important:** EtherCalc nu oferă tranzacții atomice pentru rescrierea întregului CSV. Evită editările simultane pe mai multe dispozitive; acestea pot produce conflicte. Ștergerea folosește marcaje `deleted` pentru a evita reaparția după sincronizare. Nu șterge datele browserului înainte să confirmi sincronizarea sau să exporți CSV.

Nu s-a efectuat scriere live în foaia indicată, pentru a nu modifica datele utilizatorului. Starea sincronizării este afișată în partea de sus a aplicației.


## Tema Aurora (v3)

Design modern cu fundal gradient, accente violet-turcoaz, carduri translucide si mod noapte bleumarin. Functionalitatea si formatul datelor EtherCalc raman neschimbate.
