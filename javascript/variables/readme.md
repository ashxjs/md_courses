# Les Variables

## Comprendre les variables en JavaScript : Nom, Valeur, Types 🧩

Vous savez, une variable en JavaScript, c'est comme une boîte dans votre grenier 📦. Elle a un nom, elle contient des trucs, et ces trucs ont un type. Allez, décortiquons tout ça pour voir ce qu'il en est!

**1. Le Nom : L'étiquette sur la boîte 🏷️**: Le nom de la variable, c'est comme l'étiquette que vous collez sur une boîte pour savoir ce qu'elle contient sans devoir l'ouvrir. En JavaScript, les noms de variables sont des identificateurs uniques qui suivent quelques règles simples :

- pas de chiffres au début
- pas de caractères bizarres (à part `$` et `_`)
- pas de mots réservés. <a href="https://www.w3schools.com/js/js_reserved.asp" target="_blank">La liste des mots réservés ici</a>

Rappelez-vous, JavaScript est sensible à la casse `maVariable` et `mavariable`, sont deux variables différentes !

**2. La Valeur : Ce que la boîte contient 🧸**: La valeur, c'est ce que vous mettez dans la boîte. En JavaScript, une variable peut contenir plein de choses : des nombres, des chaînes de caractères, des booléens, et même des tableaux, objets ou des fonctions (nous aborderons ces concepts un peu plus tard)

**3. Les Types : Quelle sorte de trucs ? 🌈**: En JavaScript, on n'a pas besoin de dire quel type de trucs on met dans la boîte. Le langage est dynamiquement typé, ce qui signifie qu'il comprend tout seul si c'est un nombre, une chaîne de caractère, etc.
Il y a 7 types primitifs en Javascript:

### number

(Nombre) 🔢: Que ce soit un entier, un décimal, un positif ou un négatif, tout ça, c'est des nombres.
<SyntaxHighlighter language="javascript" style="materialDark">
let age = 42;
</SyntaxHighlighter>

### string

(Chaîne de caractères) 📝: Comme un collier de perles de caractères. Parfait pour des textes, des noms, bref, tout ce qui est mots et phrases.
<SyntaxHighlighter language="javascript" style="materialDark">
let nomDeVille = "Paris"; // "Paris" est une chaîne de caractères
let firstLetterOfFirstname = "J";
let firstname = "John";
let lastname = "Doe";
</SyntaxHighlighter>

### boolean

(Booléen) ✅ ou ❌: La simplicité à son paroxysme. Vrai ou faux. Oui ou non. 1 ou 0.
<SyntaxHighlighter language="javascript" style="materialDark">
let isAdult = true;
let isMinor = false;
</SyntaxHighlighter>

### null

(Aucune valeur) 🚫: Comme une boîte vide. Explicitement rien.
<SyntaxHighlighter language="javascript" style="materialDark">
let placeDisponible = null; // null signifie "rien" ou "aucune valeur"
</SyntaxHighlighter>

### undefined

(Indéfini) 🤷‍♂️: Quand une variable n'a pas encore reçu de valeur. Un peu comme une boîte qu'on a oublié de remplir.
<SyntaxHighlighter language="javascript" style="materialDark">
let resultat; // undefined, car resultat n'a pas été défini
</SyntaxHighlighter>

### object

(Objet) 🧳: Un conteneur pour toutes sortes de valeurs, avec des clefs pour y accéder.
<SyntaxHighlighter language="javascript" style="materialDark">
let voiture = { marque: "Toyota", modele: "Corolla", annee: 2021 }; // voiture est un objet
</SyntaxHighlighter>

### symbol

(Symbole) 🔣: Unique et immuable, parfait pour des identifiants qui ne se mélangent pas avec les autres.
<SyntaxHighlighter language="javascript" style="materialDark">
let id = Symbol("id"); // id est un symbole
</SyntaxHighlighter>

Alors, pourquoi c'est important? Parce que les variables sont les fondations de tout votre code. Les noms que vous choisissez, les valeurs que vous y stockez, et les types de ces valeurs, tout cela influence la clarté et la puissance de votre code. Maîtriser les variables, c'est comme maîtriser l'art de bien ranger son grenier pour retrouver facilement ses affaires plus tard! 🛠️💡

### Déclaration de variable

Avant de pouvoir stocker des informations dans une variable, il faut la créer. Cette opération s'appelle la **déclaration** de la variable. Au niveau de l'ordinateur, déclarer une variable déclenche la réservation d'une zone de la mémoire attribuée à cette variable. Le programme peut ensuite lire ou écrire des données dans cette zone mémoire en manipulant la variable.

Voici un exemple de code qui déclare une variable puis affiche sa valeur.
<SyntaxHighlighter language="javascript" style="materialDark">
let a;
console.log(a);
</SyntaxHighlighter>
On constate que le résultat affiché est`undefined`. Il s'agit d'un type JavaScript qui indique l'absence de valeur. Immédiatement après sa déclaration, une variable JavaScript n'a pas de valeur, ce qui est logique.

### Affecter une valeur à une variable

Au cours du déroulement du programme, la valeur stockée dans une variable peut changer. Pour donner une nouvelle valeur à une variable, on utilise l'opérateur=, appelé opérateur d'affectation.
<SyntaxHighlighter language="javascript" style="materialDark">
let a;
a = 3.14;
console.log(a); // affichera 3.14
</SyntaxHighlighter>
La valeur de la variable a été modifiée par l'opération d'affectation. La ligne a = 3.14 se lit "a reçoit la valeur 3,14".

On peut également combiner déclaration et affectation d'une valeur en une seule ligne. Il est cependant important de bien distinguer leurs rôles respectifs. Le programme ci-dessous est équivalent au précédent.

### Déclarer une variable constante

Si la valeur initiale d'une variable ne changera jamais au cours de l'exécution du programme, cette variable est ce qu'on appelle une constante. Il vaut alors mieux la déclarer avec le mot-clé `const` plutôt qu'avec `let`. Cela rend le programme plus facile à comprendre, et cela permet aussi de détecter des erreurs.

<SyntaxHighlighter language="javascript" style="materialDark">
const a = 3.14; // Création d'une variable constante
a = 6.28;       // Impossible : a ne peut pas changer de valeur !
</SyntaxHighlighter>

### Incrémenter une variable de type nombre

Il est également possible d'augmenter ou de diminuer la valeur d'un nombre avec les opérateurs+= et++. Ce dernier est appelé opérateur d'incrémentation, car il permet d'incrémenter (augmenter de 1) la valeur d'une variable.
<SyntaxHighlighter language="javascript" style="materialDark">
let b = 0; // b contient 0
b += 1; // b contient 1
b++; // b contient 2
console.log(b); // 2
</SyntaxHighlighter>

## Exercices

### Objectif

L'objectif de cet exercice est de tester votre compréhension des variables.

### Instructions

1. Déclarez une variable `firstName` et assignez-lui votre prénom comme valeur.
2. Déclarez une variable `lastName` et assignez-lui votre nom de famille comme valeur.
3. Déclarez une variable `age` et assignez-lui votre âge comme valeur.
4. Déclarez une variable `isAdult` qui vaudra `true`.
5. Déclarez une `const` catAlwaysSays et affecté lui la valeur `meow`.
