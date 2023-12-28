## Fonctions

### Qu'est-ce qu'une fonction ?

## Concept

Une fonction est un ensemble d'instructions qui effectue une tâche ou calcule une valeur. Prenons un exemple simple comme faire la vaisselle; ça fait partie des tâches qui sont presque systématiquement identiques :
<SyntaxHighlighter language="javascript" style="materialDark">
/*
    fonction faireLaVaisselle:
		prendre l'eponge
		mettre du liquide vaisselle
		frotter
		rincer
		ranger
*/
</SyntaxHighlighter>

Une fonction peut retourner une valeur ou non. Dans le cas où une fonction ne retourne pas de valeur, on dit que c'est une procédure. Notre fonction `faireLaVaisselle` est bien une procédure car elle ne retourne aucune valeur.

À l'inverse, une fonction se doit de retourner une valeur, peu importe sa nature (type).

<SyntaxHighlighter language="javascript" style="materialDark">
	function addition a, b
		retourne a + b
</SyntaxHighlighter>

La fonction addition retourne bien une valeur numérique. C'est bien une fonction. Les termes `procédure` et `fonction` sont des termes souvent utilisés en algorithmie mais qu'on ne retrouve pas dans tous les langages de programmation.

## En Javascript

En `javascript` une fonction se déclare comme ceci:

<SyntaxHighlighter language="javascript" style="materialDark">
function hello() {
  console.log("hello");
}
</SyntaxHighlighter>

Une fonction commence par le mot `function` qui est suivi par son nom. Dans les parenthèses, nous allons déclarer les paramètres qu'elle peut recevoir ou non (regarde notre fonction coucou ne prend pas de paramètre !)

Les paramètres sont des valeurs qui sont attribuées à l'exécution de notre fonction.

<SyntaxHighlighter language="javascript" style="materialDark">
// déclaration de notre fonction
function addition(a, b) {
  return a + b;
}

const resultat = addition(5, 1); // appel de notre fonction ou a = 5 et b = 1
console.log(resultat); // affichera 6 !
// 🚨 l'ordre a un sens important 🚨
</SyntaxHighlighter>

🚨 Les fonctions possèdent leurs propres `scope`; une fois sorties des accolades `{}`, les variables ainsi que leurs valeurs n'existent plus !! 🚨

<SyntaxHighlighter language="javascript" style="materialDark">
	const date = "2023"; // global scope
	function getCurrentYear() {
  		const date = "2021"; // function scope
  		return date;
	}
	const currentYear = getCurrentYear();
</SyntaxHighlighter>

### Les fonction anonymes

Une fonction anonyme est une fonction qui n'a pas de nom. Ce qui veut dire qu'elle n'est pas accessible dans la mémoire avec son nom. Généralement, on les utilise dans l'appel d'une autre fonction pour avoir des comportements personnalisés.

Une fonction souvent utilisée est `setTimeout`: [👉 documentation 👈](https://developer.mozilla.org/fr/docs/Web/API/setTimeout) Celle-ci prend 2 paramètres : une fonction à exécuter et un délai en milliseconde.

La fonction ici permet de définir le code qui sera rappelé.

<SyntaxHighlighter language="javascript" style="materialDark">
	setTimeout(function () {
		console.log("Bonjour");
	}, 1000);
</SyntaxHighlighter>

#### Depuis ES6, La notation Fat arrow
Depuis ECMAScript 6, une nouvelle notation est possible. Elle permet de gagner un temps conciderable !
##### Sans retour de valeur
<SyntaxHighlighter language="javascript" style="materialDark">
	setTimeout(() => {
		console.log("Bonjour");
	}, 1000);
</SyntaxHighlighter>

##### Avec retour de valeur
Sans cet exemple, nous voulons savoir si la valeur est paire ou non.
Une fat arrow, sans accolade (`{}`) retourne son expression ! Dans cet exemple nous avons donc:

| tour | valeur | resultat |
| ----- | ------ | ------ |
| 1     | 1  | faux | 
| 2     | 2  | true |
| 3     | 4  | true |
| 4     | 99 | false |

<SyntaxHighlighter language="javascript" style="materialDark">
	[1, 2, 4, 99].filter((elt) => elt % 2 === 0); 
</SyntaxHighlighter>

## Exercice:
Créer 4 fonction qui pour chacune d'elle te renverras si son paramètre est bien du type attendu !

- isNumber: Vérifie que mon chiffre est bien un nombre (positif | négatif | entier | flottant)
- isString: Vérifie que c'est bien une string ("a" "Hello World !")
- isBoolean: Vérifie que c'est bien un booléen (true | false)
- isNil: Vérifie que la valeur est `null`
- isUndefined: Vérifie que la valeur est `undefined`

Ci tu ne sais pas comment faire, c'est normal ! Mais internet est ton ami 😁