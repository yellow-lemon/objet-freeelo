# Classes

Les "blueprints" des classes sont stockées dans la RAM statique. Les objets eux, sont stockés dans la RAM dynamique

```cs
public class Personne
{
  // Données membres
  string m_person;
  string m_nom;
  int m_age;

  // Constructeurs

  // Priopriétés (get, set, indexeurs) majuscule

  // Méthodes

  // Opérateurs
  
  // Destructeurs


}
```

## Données membres (ou attribut)
Les données membres sont les variables de la classe. \
Pour plus de claireté, il est possible de les déclarer ainsi :
```cs
string m_person;
string m_nom;
int m_age;

// au lieu de 

string person;
string nom;
int age;
```
Utilisé les variables plutot que les propriétés si possible

### Tableau
```cs
int [10] m_tab;

public TypeRetour this [int i]
{
  get {return m_tab[i]}
}

// dans le main

Toto untoto = new Toto();

untoto[3];
```


## Déclaration d'un objet
### Déclaration
```cs
Personne unePersonne;
```
### Instanciation
```cs
unePersonne = new Personne();
```

## Garbage collector
Le garbage collector s'occupe de libérer la mémoire pour nous. \
Il ne détruit que les espaces mémoires qui ne sont plus utilisés par personne.

## Signature
Il est possible d'avoir plusieurs classes avec le même nom.
```cs
public int calculerPaye(int salaire, int jours)
{
  // ...
}

public int calculerPaye(float salaire, int jours)
{
  // ...
}

public int calculerPaye(int salaire, int jours, int bonus)
{
  return this.calculerPaye(salaire, jours) + bonus;
}
```

## Constructeurs
```cs
// Constructeur par défaut
public Personne()
{
  m_prenom = "";
  m_nom = "";
  m_age = 0;
}
```

### Surcharge
Plusieurs constructeurs
```cs
```cs
// Constructeur par défaut
public Personne()
{
  m_prenom = "";
  m_nom = "";
  m_age = 0;
}

public Personne(string pprenom, string pnom)
{
  m_nom = pnom;
  m_prenom = pprenom;
  m_age = 0;
}

public Personne(int page)
{
  m_age = page;
}

public Personne(pprenom, pnom, page)
{
  this.Personne(page);
  this.Personne(pprenom, pnom)
}
```

### Surchage de compareTo
```cpp
public class Planete : | Comparable
{

}
```

## Override

```cs
public override bool equal (Personne pPersonne)
{
  //...
}

public override string toString()
{
  //...
}
```

## Surchage d'opérateur

```cs
public static Planete operator + (Planete partieGauche, Planete partieDroite)
{
  //code
}
```


## Destructeurs
```cs
public class Toto
{
  //...

  ~Toto()
  {

  }
}
```

## Statique
```cs
// dans la classe
public static int m_age;

public static int calculerBMI()
{
  //... Les variables/méthodes statiques se partagent entre tous les objets,
}
```
Il est impossible d'accéder au dynamique à partir du statique

