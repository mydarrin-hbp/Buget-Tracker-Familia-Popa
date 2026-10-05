# Buget Tracker – Familia Popa

Aplicație single-page (HTML/JS) pentru buget familial. Datele se păstrează în `localStorage`, în browserul fiecărui dispozitiv.

## Report de sold între luni
- Soldul rămas la finalul unei luni **închise** (pozitiv sau negativ) se adaugă la veniturile lunii următoare.
- Luna se închide din tab-ul „Pe luni” (sau din bannerul care apare după încheierea ei) și se poate redeschide.
- Lunile încă deschise raportează un sold **estimat** din buget; lunile închise raportează soldul **real** (sume introduse).
- Report-ul este doar calculat: sumele bugetate și cele introduse nu se modifică niciodată.
- „Sold inițial” (tab „Pe luni”) = soldul de dinaintea primei luni din buget.

## Parolă
Parola nu mai este în cod. La prima deschidere pe un dispozitiv se setează o parolă (se păstrează doar ca hash PBKDF2 în acel browser). Butonul 🔑 o schimbă.
Atenție: este o blocare de ecran, nu criptare. Fișierele din depozit (`data.js`, JSON, XLSX) rămân vizibile oricui are acces la depozit, deci depozitul trebuie să fie **privat**.

## Fișiere
- `index.html` – aplicația · `data.js` – bugetul implicit · `pdf-font.js` – font DejaVu (diacritice în PDF)
- `buget-popa-import.json` – același buget, pentru butonul „Import” · `Buget_Popa_Dashboard_Import.xlsx` – variantă Excel
