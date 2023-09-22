## Variables

### Qu'est-ce qu'une variable ?

Une variable est comme une boîte où vous pouvez stocker des valeurs pour les utiliser ou les manipuler plus tard.

<SyntaxHighlighter language="javascript" style="materialDark">
let age = 25;
</SyntaxHighlighter>

### Déclaration de variable (var, let, const)

- `var`: Ancienne manière de déclarer des variables. Portée fonctionnelle.
- `let`: Nouvelle manière de déclarer des variables. Portée de bloc.
- `const`: Comme `let`, mais la valeur ne peut pas être modifiée.

<SyntaxHighlighter language="javascript" style="materialDark">
var name = "John";
let age = 30;
const pi = 3.14159;
</SyntaxHighlighter>

### Types natifs en JavaScript

JavaScript possède quelques types de données fondamentaux, souvent appelés types primitifs, qui sont les suivants :

- Types Basiques:
  - **number**: Représente les nombres entiers et flottants.
  - **string**: Représente les chaînes de caractères.
  - **boolean**: Représente une valeur vraie ou fausse (`true` ou `false`).
- Types Complexes:
  - **object**: Utilisé stocker un ensemble de propriété par clés.
  - **undefined**: Utilisé pour les variables qui ont été déclarées mais n'ont pas encore été attribuées.
  - **null**: Représente une absence délibérée de valeur.
  - **NaN**: Utilisé pour indiquer qu'une opération mathématique est invalide.

<SyntaxHighlighter language="javascript" style="materialDark">
let aNumber = 42; // Number
let aString = "Hello"; // String
let aBoolean = true; // Boolean
let anObject = {}; // Object
let notDefined; // undefined
let isEmpty = null; // null
let emptyArray = []; // Array
let stringArray = ["string1", "string2"]; // Array
</SyntaxHighlighter>

## Exercices

### Objectif

L'objectif de cet exercice est de tester votre compréhension des variables.

### Instructions

1. Déclarez une variable `firstName` et assignez-lui votre prénom comme valeur.
2. Déclarez une variable `lastName` et assignez-lui votre nom de famille comme valeur.
3. Déclarez une variable `age` et assignez-lui votre âge comme valeur.
4. Déclarez une variable `isAdult` qui sera `true`.
5. Déclarez une variable `skills` et assignez-lui un tableau contenant les noms de quelques compétences que vous possédez (par exemple, "JavaScript", "HTML", "CSS").
6. Déclarez une variable `person` et assignez-lui un objet contenant les clés `firstName`, `lastName`, `age`, `isAdult`, et `skills`, en utilisant les variables que vous avez déjà déclarées.
