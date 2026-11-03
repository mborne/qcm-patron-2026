# QCM patrons de conception 2026

> Une seule bonne réponse par question.

## Question 1

Avec le code suivant, quelle affirmation est vraie ?

```ts
const a = new Point([2.0, 3.0]);
const b = a;
b.translate(1.0, 1.0);
```

* [ ] A : *a* et *b* référencent le même objet
* [ ] B : Les coordonnées de *a* valent toujours `[2.0, 3.0]`
* [ ] C : Le code ne compilera pas
* [ ] D : *b* est une copie de l'objet *a*

## Question 2

Un ramasse-miettes (*garbage collector*) permet :

* [ ] A : La libération automatique de la mémoire
* [ ] B : L'implémentation du patron de conception `Prototype`
* [ ] C : L'implémentation de fabriques statiques
* [ ] D : La détection des erreurs de type à la compilation

## Question 3

Une application a été livrée avec une API publique mal conçue. Les clients l'utilisent désormais et il devient impossible de la modifier sans les casser. Il s'agit de l'anti-patron :

* [ ] A : Abstraction inverse
* [ ] B : Coulée de lave
* [ ] C : Optimisation prématurée
* [ ] D : Programmation spaghetti

## Question 4

Développer son propre système de log plutôt qu'utiliser une bibliothèque existante relève de l'anti-patron :

* [ ] A : Coup de marteau doré
* [ ] B : Réinventer la roue (carrée)
* [ ] C : Optimisation prématurée
* [ ] D : Coulée de lave

## Question 5

L'écriture de tests unitaires et fonctionnels est utile pour :

* [ ] A : Utiliser des patrons de conception
* [ ] B : Améliorer les performances de l'application
* [ ] C : Limiter le risque d'introduction d'un changement de comportement
* [ ] D : Programmer en orienté objet

## Question 6

Quel est le **plus gros problème** dans l'implémentation suivante ?

```ts
class Coordinate extends Logger {
    //...
    distance(other: Coordinate): number {
        const dx = this.x - other.x;
        const dy = this.y - other.y;
        this.debug("dx = " + dx + ", dy = " + dy);
        return Math.sqrt(Math.pow(dx, 2.0) + Math.pow(dy, 2.0));
    }
}
```

* [ ] A : `Math.pow(dx, 2.0)` est moins performant que `dx * dx`
* [ ] B : La console va être polluée par des logs inutiles
* [ ] C : `Coordinate` hérite de `Logger`
* [ ] D : `distance` devrait être une méthode statique

## Question 7

Quel patron de conception correspond à l'appel suivant ?

```ts
const c = Coordinate.fromString("2.0 3.0");
```

* [ ] A : Itérateur
* [ ] B : Composite
* [ ] C : Décorateur
* [ ] D : La fabrique statique

## Question 8

Quel patron de conception correspond aux appels suivants ?

```ts
const triangulation = new DelaunayTriangulation();
triangulation.addPoint(new Point([0.0, 0.0]));
triangulation.addPoint(new Point([1.0, 1.0]));
triangulation.addPoint(new Point([2.0, 0.0]));
triangulation.addPoint(new Point([1.0, -1.0]));
const triangles: Polygon[] = triangulation.getTriangles();
```

* [ ] A : La fabrique statique
* [ ] B : Monteur (*Builder*)
* [ ] C : Itérateur
* [ ] D : Décorateur

## Question 9

Dans le TP, la notion de "visite" dans `GeometryVisitor` s'applique :

* [ ] A : Aux différentes classes concrètes de la hiérarchie `Geometry` (`Point`, `LineString`...)
* [ ] B : Aux attributs privés des géométries
* [ ] C : Aux `EventListener` écoutant les modifications
* [ ] D : Aux copies de `Geometry`

## Question 10

Quels patrons de conception fournissent un cadre pour la construction d'un système complet ?

* [ ] A : Les patrons comportementaux
* [ ] B : Les patrons architecturaux
* [ ] C : Les patrons de création
* [ ] D : Les patrons structuraux
