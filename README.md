# IMDb Movie Performance Analysis: Clustering & Classification

## Descrierea Proiectului
Acest proiect explorează setul de date **IMDb Top 1000 Movies** pentru a identifica factorii care contribuie la succesul critic și comercial al unui film. Scopul principal este de a îmbina tehnicile de Machine Learning (Supervised și Unsupervised) cu o perspectivă de business, oferind insight-uri bazate pe date despre ce transformă o producție cinematografică într-un succes.

## Obiective
* **Segmentarea pieței:** Identificarea unor grupuri ascunse (clustere) de filme cu caracteristici similare pentru a înțelege mai bine portofoliul cinematografic.
* **Analiză predictivă și cauzală:** Construirea unui model capabil să prezică dacă un film va depăși un prag calitativ (Rating IMDb $\ge$ 8.0) și interpretarea factorilor care influențează această performanță.

## Metodologie și Algoritmi
Proiectul este împărțit în trei mari etape:

1. **Data Preprocessing & Feature Engineering**
   * Curățarea datelor, tratarea valorilor lipsă și formatarea corectă a variabilelor (ex: transformarea veniturilor, extragerea duratei).
   * Pregătirea datelor pentru algoritmii de Machine Learning (StandardScaler).

2. **Unsupervised Learning: K-Means Clustering**
   * Am aplicat algoritmul K-Means pentru a găsi structuri și similarități în date. 
   * Această metodă ajută la segmentarea filmelor în categorii specifice, dincolo de genurile clasice, bazându-se pe atribute precum durata, anul lansării și numărul de voturi.

3. **Supervised Learning: Logistic Regression**
   * Am antrenat un model de Regresie Logistică pentru a prezice dacă un film va avea o notă $\ge$ 8.0.
   * **Business Value:** Modelul a oferit o explicație cauzal-statistică clară. Analizând coeficienții modelului, am putut cuantifica influența exactă a caracteristicilor specifice (numărul de voturi, durata filmului, anul lansării) asupra ratingului final.

## Tehnologii Utilizate
* **Limbaj:** Python 3
* **Manipularea datelor:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn
* **Data Visualization:** Matplotlib, Seaborn


* **Hyperparameter Tuning:** Optimizarea modelului folosind `GridSearchCV` și explorarea unor modele non-liniare (ex. Random Forest).
* **Integrare de date externe:** Corelarea setului de date actual cu informații despre premii (ex. Nominalizări sau premii Oscar câștigate) pentru a măsura impactul acestora asupra ratingului.
