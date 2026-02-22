# Analiza podataka ekspresije gena

## Opis projekta

Cilj projekta je analiza visokodimenzionalnog skupa podataka koji predstavlja matricu ekspresije gena.  
Podaci sadrže približno:

- ~20 000 gena (atributa)
- ~8 000 ćelija (uzoraka)

Zbog velikog broja dimenzija, poseban fokus je stavljen na optimizaciju memorije i efikasnu numeričku obradu.

---

## Učitavanje podataka

Podaci se inicijalno učitavaju pomoću biblioteke pandas, radi lakšeg rada sa imenima gena i ćelija.

Međutim, zbog velike dimenzionalnosti matrice, kompletna obrada se vrši korišćenjem NumPy biblioteke.  
Podaci se konvertuju u `numpy.ndarray` tipa `float32` kako bi se smanjila potrošnja memorije i izbeglo gašenje kernela.

Strategija rada:

1. Učitavanje pomoću pandas
2. Konverzija u NumPy
3. Dalja numerička obrada u NumPy okruženju
