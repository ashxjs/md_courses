# Les tableaux

## Concept
Les tableaux permettent de stocker des données et peu importe leurs types. En Javascript, les tableaux sont des objets à part entière.
Nous pouvons les créer de manière simple comme :


## Structure
Les tableaux stockent les valeurs les une a la suite des autres. Chaque valeur est rangée dans une case à laquelle correspond un `index` donné.

🚨 Attention, les index en Javascript commencent à 0 🚨

Dans l'exemple suivant nous avons un tableau contenant 7 valeurs de l'index 0 à 6.
![js array structures](https://qph.cf2.quoracdn.net/main-qimg-8b306b4c6d47bbafe378924ab42d24ba-lq)

En Javascript, pour créer un array avec les mêmes valeurs nous pouvons le faire comme ceci:

<SyntaxHighlighter language="javascript" style="materialDark">
	const arr = [3, 8, 1, 0, 5, -2, 34];
</SyntaxHighlighter>

## Accéder à une valeur d'un tableau avec son index
Pour accéder aux éléments d'un tableau, on utilise l'opérateur `[]` suivi de l'index voulu.

Ici nous voulons récupérer la première valeurs du tableau.

Quel est son index ?

<SyntaxHighlighter language="javascript" style="materialDark">
const arr = [3, 8, 1, 0, 5, -2, 34];
console.log(arr[0]); // output: 3
</SyntaxHighlighter>

### Parcourir un tableau
Ici nous allons utiliser la bonne vieille méthode de la boucle `for` pour parcourir notre tableau. Comme nous utilisons une boucle dite déterministe, nous devons connaitre à l'avance le nombre de fois que nous allons parcourir notre tableau ! Pour cela, la class Array possède un attribut `length`. !

Nous allons écrire une fonction qui parcour notre tableau et qui nous donne l'index de l'emoji qui n'est pas un animal.

Quel sont les étapes à réaliser ?
- Parcourir les éléments du tableau un à un
- Comparer notre caractère à l'emplacement `i` à notre variable `intruder`.
- Afficher lorsqu'on a trouvé l'intrus: "l'index de l'intrus est:"

<SyntaxHighlighter language="javascript" style="materialDark">
const animals = ["dog", "cat", "duck", "ball"];
const intruder = "ball";
for(let i = 0; i < animals.length; i++) {
    if(animals[i] === intruder) {
        console.log("l'index de l'intrus est:", animals[i]);
    }
}
</SyntaxHighlighter>

## L'avantage des tableaux en Javascript
Comme on l'a vu précédemment le tableau en Javascript possède des attributs et des méthodes !
Ils nous permettent de réaliser des traitements sans avoir à écrire nous même le code !
Allons voir ca de plus prêt 🚀

### Attributs
Une instance d'Array ne possède qu'un attribut public (accéssible en dehors de la class) !
C'est `length` qui vous donne la taille de celui-ci.

<SyntaxHighlighter language="javascript" style="materialDark">
const cars = ["Saab", "Volvo", "BMW"];
console.log(cars.length); // output: 3
</SyntaxHighlighter>

### Méthodes
#### Filter
Renvoie un nouveau tableau contenant tous les éléments du tableau appelant pour lesquels la fonction de filtrage fournie renvoie un résultat positif.

La méthode filter prend en paramètre, une fonction de filtre, ce traitement sera appliqué à chaque élément du tableau. À la fin des traitements, la méthode retournera un tableau contenant les éléments recherchés.

<SyntaxHighlighter language="javascript" style="materialDark">
const cats = [{ name: "Marie", gender: "female" }, { name: "Berlioz", gender: "male" }, { name: "Toulouse" }];
const females = cats.filter((cat) => cat.gender === "female" );
console.log(females); // output: { name: "Marie", gender: "female" }
</SyntaxHighlighter>

Si aucun élément n'a été trouvé, un tableau vide sera retourné.

<SyntaxHighlighter language="javascript" style="materialDark">
const cats = [{ name: "Marie", gender: "female" }, { name: "Berlioz", gender: "male" }, { name: "Toulouse" }];
const females = cats.filter((cat) => cat.gender === "Marie");
console.log(females); // output: []
</SyntaxHighlighter>

#### Find
La méthode find() des instances de tableau renvoie le premier élément du tableau fourni qui satisfait à la fonction de test fournie. Si aucune valeur ne satisfait la fonction de test, la méthode renvoie undefined.

<SyntaxHighlighter language="javascript" style="materialDark">
const employees = [
    { name: "Skywalker", firstname: "Anakin", order: "jedi" },
    { name: "Skywalker", firstname: "Luc", order: "jedi" },
    { name: "Obiwan", firstname: "Kenobi", position: "jedi" },
    { name: "Windu", firstname: "Mace", position: "jedi" },
];
const females = cats.find((jedi) => jedi.name === "Skywalker" && jedi.firstname === "Anakin" );
console.log(females); // output: { name: "Skywalker", firstname: "Anakin", order: "jedi" }
</SyntaxHighlighter>

#### Map
La méthode map() des instances de tableau crée un nouveau tableau contenant les résultats de l'appel d'une fonction fournie sur chaque élément du tableau appelant.

<SyntaxHighlighter language="javascript" style="materialDark">
const array1 = [1, 4, 9, 16];
const map1 = array1.map((x) => x * 2); // on retourne le produit x fois 2.
console.log(map1); // output: [2, 8, 18, 32]
</SyntaxHighlighter>

Tu pourras retrouver la liste complete des méthodes existantes ➡️ [ici](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) ⬅️

## Exercice
Vous devrez créer une class MyArray. Elle doit avoir un attribut `length` qui renvoie la taille du tableau.
Elle doit prendre dans son constructeur un tableau d'éléments quelconque.
Aide toi de la doc que je t'ai donné juste au dessus.

<SyntaxHighlighter language="javascript" style="materialDark">
    const arr = new MyArray([1, 5, 7]);
    console.log(arr.length); // output: 3
    arr.push("pouette");
    console.log(arr.length); // output: 4
    console.log(arr.some((elt) => typeof elt === "string")); // output: true
    console.log(arr.find((elt) => elt === "pouette")); // output: "pouette"
    console.log(arr.find((elt) => elt === "Vador")); // output: undefined
</SyntaxHighlighter>

Ainsi que 5 méthodes:
- find: `find(callbackFn)` prennant en paramètre la fonction de recherche. Si aucun éléments n'est trouvé retourne `[]`.
- push: `push(value)` prennant en paramètre l'élément à àjouter au tableau.
- some: `some(callbackFn)` prennant en paramètre l'élément à àjouter au tableau. Retourne `false` si aucun élément n'est trouvé.

Good luck ! 🙏