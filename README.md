# Projets C++ — BTS CIEL

Exercices et travaux pratiques de C++ réalisés en première année de BTS CIEL à Campus Ozanam (Lille), avec CodeLite.
Deux modules couverts : les bases du langage (Module 2) et la programmation avancée — tableaux, fonctions, pointeurs, classes (Module 5).

---

## Structure

```
cpp-bts/
├── module2/          # Bases : variables, conditions, boucles
└── module5/          # Avancé : tableaux, fonctions, pointeurs, classes, héritage
```

---

## Module 2 — Bases du C++

Premiers programmes en C++ : entrées/sorties, variables, structures conditionnelles, boucles. IDE : CodeLite avec compilateur GCC.

### TP1 — Variables & opérations

| Exercice | Description |
|---|---|
| Hello World | Saisie du prénom, affichage "Bonjour \<prénom\>" |
| Disque | Calcul de la circonférence et de la surface à partir d'un rayon |
| Pas à pas | Analyse de code et utilisation du débogueur CodeLite |
| Dépassement de capacité | Mise en évidence d'un overflow avec le debugger |
| Aire | Calcul de l'aire d'un triangle (formule de Héron, `sqrt()`) |
| Moyenne | Calcul de la moyenne de 2 puis 3 valeurs avec une seule variable de saisie |
| Code ASCII *(bonus)* | Saisie d'un entier 0–255, affichage du caractère ASCII correspondant |
| Papier peint *(bonus)* | Calcul du nombre de rouleaux nécessaires pour tapisser une pièce (`ceil`, `floor`) |
| Opérations *(bonus)* | Mise en évidence des limites de précision du type `float` |
| TVA *(bonus)* | Calcul d'un prix TTC avec le taux de TVA défini comme constante |

### TP2 — Structures alternatives (`if/else`, `switch/case`)

| Exercice | Description |
|---|---|
| Parité | Teste si un entier est pair ou impair |
| Signe | Affiche `+`, `-` ou `0` selon le signe d'un entier |
| Équation du second degré | Calcul du discriminant, affichage du nombre de solutions réelles |
| Calculs (switch) | Menu opérations : carré, racine carrée, cosinus, sinus |
| Quadrant | Détermine le quadrant d'un point (x, y) avec `if` imbriqués |
| Égal | Comparaison de deux réels avec gestion de la précision flottante |
| Calcul de π — partie 1 *(bonus)* | Tirage d'un point aléatoire dans un carré, test d'appartenance au cercle inscrit |
| Cryptage *(bonus)* | Chiffrement d'un entier 4 chiffres : `(chiffre + 7) % 10` puis permutation |
| Décryptage *(bonus)* | Programme inverse du cryptage |

### TP3 — Structures itératives (`while`, `do/while`, `for`)

| Exercice | Description |
|---|---|
| Étoile | Affichage d'une colonne de N étoiles |
| Saisie montant | Saisie répétée jusqu'à obtenir un multiple de 20 €, limité à 120 € |
| Notes | Saisie de notes (valeur négative = fin), calcul de la somme, moyenne, max, min |
| Condensateur | Simulation de la décharge RC — calcul du temps à une tension donnée |
| Calcul de π — partie 2 *(bonus)* | Méthode Monte Carlo complète avec N tirages, estimation de π |
| Losange ASCII *(bonus)* | Saisie d'un nombre impair, affichage d'un losange avec boucles imbriquées |

```
    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *
```

---

## Module 5 — C++ Avancé

Programmation avancée et introduction à la POO : tableaux, fonctions, pointeurs, classes.

### TP1 — Tableaux

Tableaux statiques et dynamiques : déclaration, remplissage, parcours, recherche d'extremums, statistiques.

| Exercice | Description |
|---|---|
| Remplit tableau | Remplissage aléatoire d'un tableau de 100 éléments |
| Mois / Jours | Tableau des jours par mois ; saisie d'un numéro de mois, affichage du nombre de jours |
| Affiche tableau | Parcours et affichage d'un tableau, une valeur par ligne |
| Min / Max | Recherche du minimum et du maximum dans un tableau |
| Statistiques | Simulation de 1000 jets de dés, comptage des occurrences de chaque face |
| Mise en forme | Formatage avec `iomanip` : `setw`, `setfill`, `setprecision` |
| Table | Affichage des entiers de 0 à 10 avec leur carré et leur cube |
| Dés | Tableau de N entiers entre 1 et 6, statistiques en pourcentage |
| Tasser | Suppression des zéros dans un tableau, tassage des éléments restants |
| Cryptage/Décryptage | Reprise du cryptage TP2 avec tableau et boucle, support jusqu'à 10 chiffres |

### TP2 — Fonctions

Écriture et appel de fonctions : prototypes, procédures, récursivité, différents modes de passage de paramètres.

| Exercice | Description |
|---|---|
| Valeur absolue | Fonction retournant la valeur absolue d'un entier |
| Max | Fonction retournant le plus grand de deux entiers |
| Losange | Refactorisation du losange TP3 avec `void TraceLigne(int ligne, int hauteur)` et `void losange(int diagonale)` |
| Cryptage/Décryptage | Fonctions `bool Dissociation(const long int&, int[])`, `bool Cryptage(long int&)`, `bool Decryptage(long int&)` avec menu |
| Condensateur *(bonus)* | Extraction de la logique dans une fonction `TrouveT1(E1, E0, Tau, precision)` |

Modes de passage vus : par valeur, par référence (`&`), par référence constante (`const &`), passage de tableau.

### TP3 — Pointeurs

Arithmétique des pointeurs, passage par adresse, tableaux dynamiques.

| Exercice | Description |
|---|---|
| Cryptage/Décryptage | Réécriture des fonctions du TP2 avec passage par pointeur (`*`) |
| Tableaux et moyenne | Tableau dynamique (`new`/`delete`), fonctions `Moyenne()` et `EnlevePremier()` |
| Stockage de mots | Tableau de `char*` dynamiques : taille de chaque chaîne adaptée au mot saisi |

Concepts : `new`, `delete`, `delete[]`, arithmétique de pointeur (`*(tableau+i)`), parcours par pointeur.

### TP4 — Classes

Introduction à la POO : encapsulation, attributs privés, méthodes publiques, constructeur, destructeur, architecture `.h`/`.cpp`.

---

**Classe `Losange` (`TP4-1`)**

Refactorisation du losange en classe avec fichiers `.h`/`.cpp` séparés. Première utilisation d'une architecture multi-fichiers.
Méthodes : `TraceTriangleSuperieur`, `TraceTriangleInferieur`, `TraceLigne`. Le constructeur prend la diagonale en paramètre.

---

**Classe `CryptageDecryptage` (`TP4-2`)**

Chiffrement et déchiffrement d'un entier par permutation de ses chiffres. Le constructeur reçoit la taille maximale du nombre traitable.

```cpp
class CryptageDecryptage {
private:
    int m_tailleMax;
    int m_tableau[TAILLE_MAX];
    void Permutation();           // méthode privée
public:
    CryptageDecryptage(int taille);
    bool Dissociation(const long int& nombre);
    bool Cryptage(long int& nombre);
    bool Decryptage(long int& nombre);
};
```

Concepts : encapsulation, méthode privée, passage par référence constante, menu interactif en boucle.

---

**Classe `Temps` (`TP4-3`)**

Représentation d'une durée en heures/minutes/secondes avec affichage militaire (`23:50:10`) et standard (`11:50:10 PM`).

```cpp
class Temps {
private:
    unsigned int heure, minute, seconde;
public:
    Temps();   // initialise à 0:0:0
    void AjusterTemps(unsigned int h, unsigned int m, unsigned int s);
    void AfficherMilitaire();
    void AfficherStandard();
};
```

`AjusterTemps()` vérifie la validité des valeurs et remet à zéro les valeurs hors plage.

---

---

## Compiler et exécuter

```bash
# Projet simple (un seul fichier)
g++ -o programme main.cpp

# Projet multi-fichiers (ex: CryptageDecryptage)
g++ -o programme main.cpp CryptageDecryptage.cpp

# Projet multi-fichiers avec plusieurs classes (ex: Temps)
g++ -o programme main.cpp Temps.cpp
```

---

## Ce que j'ai appris

- La progression des concepts C++ : du `cout` basique jusqu'aux classes
- Pourquoi séparer `.h` et `.cpp` — déclaration vs implémentation
- La gestion manuelle de la mémoire avec `new` / `delete` et l'importance du destructeur
- La différence concrète entre passage par valeur, par référence et par pointeur
- Les bases de la POO : encapsulation, instanciation, méthodes publiques/privées, constructeur/destructeur
