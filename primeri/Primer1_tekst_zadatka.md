# Da li znanje matematike ima veze sa znanjem programiranja

U fajlu "studenti.csv" je dataset sa podacima više studenata (svaki red je jedan student) i kolonama:
- Indeks (broj indeksa - anonimizirano)
- Ime, Prezime (anonimizirano)
- Pol
- Matematika 1 (broj poena na ispitu iz matematike)
- Principi programiranja (broj poena na ispitu iz programiranja)

Potrebno je utvrditi da li postoje neke grupe studenata kada se analiziraju ocene iz matematike i programiranja.
Subjektivne pretpostavke su da studenti koji znaju matematiku, znaju dobro i da programiraju. Ne uzimati u obzir
pol studenata pri klasterizaciji.

Probati sa **KMeans klasterizacijom**.

Kojem klasteru bi pripao student koji ima 50 poena iz matematike i 100 iz programiranja?

Napomene:
- Ovo je "idealan" primer, ali su podaci stvarni
- Nema nedostajućih podataka
- Nema outlier-a
- Radi se analiza samo prema dve promenljive (broj poena iz matematike i programiranja)
- Obe promenljive su u istom rasponu od 40 do 100