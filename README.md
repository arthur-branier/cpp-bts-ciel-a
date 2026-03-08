[README-cpp.md](https://github.com/user-attachments/files/25825380/README-cpp.md)
# Projets C++ — BTS CIEL

Exercices et travaux pratiques de C++ réalisés en première année de BTS CIEL à Campus Ozanam (Lille), avec CodeLite.
Deux modules couverts : les bases du langage (Module 2) et la programmation avancée — tableaux, fonctions, pointeurs, classes (Module 5).

---

## Structure

```
cpp-bts/
├── module2/          # Bases : variables, conditions, boucles
└── module5/          # Avancé : tableaux, fonctions, pointeurs, classes
```

---

## Module 2 — Bases du C++

Premiers programmes en C++ : entrées/sorties, variables, structures conditionnelles, boucles. IDE : CodeLite avec compilateur GCC.

| TP | Concepts couverts |
|---|---|
| TP1 | Variables, entrées/sorties, débogueur CodeLite |
| TP2 | Structures conditionnelles (`if/else`, `switch/case`) |
| TP3 | Boucles (`while`, `do/while`, `for`), premiers algos numériques (Monte Carlo) |

---

## Module 5 — C++ Avancé

Programmation avancée et introduction à la POO : tableaux, fonctions, pointeurs, classes.

| TP | Concepts couverts |
|---|---|
| TP1 | Tableaux statiques et dynamiques, statistiques |
| TP2 | Fonctions, prototypes, passage par valeur / référence / référence constante |
| TP3 | Pointeurs, arithmétique de pointeurs, tableaux dynamiques (`new`/`delete`) |
| TP4 | Classes, encapsulation, constructeur/destructeur, architecture `.h`/`.cpp` |

---

## Zoom — Classes POO (TP4)

Le point le plus avancé du module. Trois classes développées avec fichiers `.h`/`.cpp` séparés.

**Classe `CryptageDecryptage`**

Chiffrement et déchiffrement d'un entier par permutation de ses chiffres.

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

**Classe `Temps`**

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

---

## Compiler et exécuter

```bash
# Projet simple (un seul fichier)
g++ -o programme main.cpp

# Projet multi-fichiers (ex: CryptageDecryptage)
g++ -o programme main.cpp CryptageDecryptage.cpp
```

---

## Ce que j'ai appris

- La progression des concepts C++ : du `cout` basique jusqu'aux classes
- Pourquoi séparer `.h` et `.cpp` — déclaration vs implémentation
- La gestion manuelle de la mémoire avec `new` / `delete` et l'importance du destructeur
- La différence concrète entre passage par valeur, par référence et par pointeur
- Les bases de la POO : encapsulation, instanciation, méthodes publiques/privées, constructeur/destructeur
