## Introduction aux opérateurs en JavaScript

Les opérateurs sont des symboles qui permettent d'effectuer des opérations sur une ou plusieurs valeurs. Imaginons que ces opérateurs soient comme des outils dans une boîte à outils, chaque outil ayant un rôle spécifique.

### Opérateurs d'égalité

Ces opérateurs sont utilisés pour comparer la valeur ou le type de deux variables.

- `==` : Compare les valeurs et renvoie `true` si elles sont égales. Par exemple, `5 == "5"` renverra `true` car la valeur est la même, même si le type est différent.
- `===` : Compare à la fois la valeur et le type, et renvoie `true` si les deux sont égaux. Ainsi, `5 === "5"` renverra `false` car le type est différent.
- `!=` : Renvoie `true` si les valeurs ne sont pas égales.
- `!==` : Renvoie `true` si la valeur ou le type ne sont pas égaux.

#### Exercices pratiques

1. Quelle sera la sortie de ce code:

<SyntaxHighlighter language="javascript" style="materialDark">
   console.log(10 == "10");
</SyntaxHighlighter>

2. Que renvoie le code suivant:

<SyntaxHighlighter language="javascript" style="materialDark">
   console.log(7 !== "7");
</SyntaxHighlighter>
3. Évaluez le résultat de:

<SyntaxHighlighter language="javascript" style="materialDark">
   console.log(4 === 4 && 5 != "5");
</SyntaxHighlighter>

### Opérateurs de comparaison

Ces opérateurs sont utilisés pour comparer deux valeurs.

- `>` : Vérifie si la valeur à gauche est plus grande que celle de droite.
- `<` : Vérifie si la valeur à gauche est plus petite que celle de droite.
- `<=` : Vérifie si la valeur à gauche est plus petite ou égale à celle de droite.
- `>=` : Vérifie si la valeur à gauche est plus grande ou égale à celle de droite.

#### Exercices pratiques

#### Exercices pratiques sur les opérateurs d'égalité

#### Consigne: Pour chacun des exercices ci-dessous trouve l'opérateur qui renvoie `true`.

Pour valider l'exercice tu devras afficher le message avec la fonction `console.log(MESSAGE A AFFICHER)`

1. Message: "égalité entre une string et un number"

<SyntaxHighlighter language="javascript" style="materialDark">
   const a = "5";
   const b = 5;
</SyntaxHighlighter>

2. Message: "égalité entre une string et un string"

<SyntaxHighlighter language="javascript" style="materialDark">
   const x = "Hello World !";
   const y = "Hello World";
</SyntaxHighlighter>

3. Message: "égalité entre deux tableaux"

<SyntaxHighlighter language="javascript" style="materialDark">
   const array1 = [1, 2, 3];
   const array2 = [1, 2, 3];
</SyntaxHighlighter>

#### Exercices pratiques sur les opérateurs de comparaison

1. Message: "La personne est bien majeur"

<SyntaxHighlighter language="javascript" style="materialDark">
   const age = 20;
   const isAdult = age >= 18;
</SyntaxHighlighter>

2. Message: "Winter is comming"

<SyntaxHighlighter language="javascript" style="materialDark">
   const temperature = -5;
   const isFreezing = temperature <= 0;
</SyntaxHighlighter>

3. Message: "La vitesse est bien comprise entre 30 et 50 km/h"

<SyntaxHighlighter language="javascript" style="materialDark">
   const speed = 45;
   const isSpeeding = speed > 30 && speed < 50;
</SyntaxHighlighter>

---

Nous espérons que cette introduction aux opérateurs en JavaScript vous a été utile et vous a donné envie de poursuivre cette formation !
