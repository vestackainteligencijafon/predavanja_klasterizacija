# Postupak klasterizacije

1. Učitati podatke iz csv fajla (i eventualno uraditi početnu selekciju)
2. Pregledati okvirno koji su podaci (promenljive) i izvršiti izbor promenljivih
    - Izbaciti promenljive koje nisu bitne (identifikatori, tekstualne promenljive tj. sve koje nisu numeričke ili nemaju smisla za taj zadatak, i kategorijske promenljive koje nema smisla kodirati u numeričke)
    - Pogledati raspodele preko scatter plot-a (ako su ostale samo dve promenljive) ili box-plota (ako ih ima više)
3. Priprema podataka
    - 3.1. Proveriti nedostajuće vrednosti
        - Izbaciti cele redove (ako neki red ima puno nedostajućih vrednosti)
        - Ili izbaciti cele promenljive (ako neka ima puno NAs) ili
        - Ili zameniti NaN sa npr. medijanom ili prosekom za tu promenljivu (median tj. mean)
    - 3.2. Proveriti korelacije. Ako ima velikih korelacija izbaciti odgovarajuću promenljivu (ili više njih)
    - 3.3. Proveriti outlier-e
        - Ako ih ima, uraditi winsorization za tu promenljivu. Izabrati donji i gornji percentil (obično 5 i 95) u zavisnosti na koju stranu se outlier-i pojavljuju.
        - Ako neka promenljiva ima puno outlier-a (npr. preko 10%), izbaciti tu promenljivu.
    - 3.4. Proveriti raspon vrednosti promenljivih. Pošto skoro izvesno nisu u istom rasponu uraditi skaliranje (normalizaciju)
4. Izabrati metodu klasterizacije (KMeans ili hijerarhijska) i parametre klasterizacije
    - KMeans - kmeans++, uraditi elbow metodu zbog broja klastera
    - Hijerarhijska - izbor linkage metode i merenja udaljenosti (obično euklidska), iscrtati dendrogram (ili više njih)
5. Izvršiti klasterizaciju (ako nije jasan optimalan broj klastera, uraditi sve varijante koje se čine ok)
6. Proceniti tj. protumačiti rezultate klasterizacije
    - Nacrtati uporedni boxplot a, ako su samo dve promenljive, može i scatterplot sa označenim instancama i klasterima
    - Pogledati veličine klastera (objektivna procena), centre klastera i disperziju od centara
    - Subjektivno proceniti klastere i opisati ih
7. Ako se rezultati ne čine ok, vratiti se na korak 5 samo sa drugim parametrima klasterizacije (drugi broj klastera, druga metoda za računanje udaljenosti ili linkage)