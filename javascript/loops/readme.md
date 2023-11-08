# Les Boucles

---

# Les Boucles en JavaScript : Le Tour de Manège du Code 🎠

Si vous avez déjà souhaité dire à votre ordinateur de répéter une tâche encore et encore sans copier-coller le même code des centaines de fois, les boucles sont votre baguette magique. 🪄

**Qu'est-ce qu'une boucle? 🔄**

Imaginez que vous avez une liste de tâches à faire. Sans boucle, vous liriez et effectueriez chaque tâche une par une, manuellement. Avec une boucle, c'est comme si vous aviez un assistant personnel infatigable qui lit la première tâche, l'exécute, puis retourne au début de la liste pour passer à la suivante, et ainsi de suite jusqu'à ce que la liste soit terminée.

En programmation, une boucle fait exactement cela : elle répète une opération ou un bloc de code tant qu'une certaine condition est vraie. C'est un outil fondamental qui aide à :

- Exécuter le même code encore et encore, économisant ainsi de précieuses lignes et heures de codage.
- Parcourir des données complexes, comme les éléments d'un tableau ou les propriétés d'un objet, avec une efficacité chirurgicale.
- Effectuer des tâches répétitives jusqu'à ce qu'une certaine condition soit remplie (par exemple, chercher un nombre spécifique dans une liste).

e.g:
L'Entreprise X possède 157 salariés et a besoin de créer pour chacun de ses salariés, un dossier permettant de classé leurs bulletins de paies.

<SyntaxHighlighter language="javascript" style="materialDark">
/*
    Faire 157 fois l'operation suivante:
        créer un dossier contenant le ne nom du salarié
*/
</SyntaxHighlighter>

## While

### Concept

La boucle while est une boucle dite non déterministe, car nous répétons un ensemble d'actions pendant un temps indéfinit.
C'est à dire qu'on ne sait pas à l'avance quand on doit arréter la boucle.
e.g:
<SyntaxHighlighter language="javascript" style="materialDark">
/_
tant qu'il pleut
je reste à l'abris
_/
</SyntaxHighlighter>

### En Javascript

Pour écrire une boucle while, rien de plus simple.
La condition se trouve entre les parenthèse.
Cette condition doit forcement devenir fausse, sinon on aurait une boucle infinit (pas de panique il faut juste fermer le programme).

🚨 Attention à bien déclarer des variables de types `let` car ici on veut bien modifier sa valeur.
<SyntaxHighlighter language="javascript" style="materialDark">
let loading = true;
let progress = 0;

while(loading) {
if(progress < 100) {
progress++; // on incrémente progress de 1 (revient à écrire: progress = progress + 1)
} else {
loading = false;
}
}
</SyntaxHighlighter>

## For

### Concept

La boucle `for` est une boucle déterministe, car on sait à l'avance combien de fois on va l'éxécuter.
Par convention, la variable d'incrément s'appelle `i` ou `j`.

e.g: Dans cet example nous avons 10 employés, on connait donc le nombre d'itération à l'avance.
<SyntaxHighlighter language="javascript" style="materialDark">
/_
pour i allant de 1 à 10 faire
créer un dossier avec le nom de l'employée x
_/
</SyntaxHighlighter>

### En Javascript

Sa notation est plus complexe car elle comprend 3 partie:

- 1️⃣ déclaration de la variable
- 2️⃣ condition de fin
- 3️⃣ incrémentation.

🚨 Attention à ne pas oublier les `;`, ils permettent de séparer les déclarations 🚨

<SyntaxHighlighter language="javascript" style="materialDark">
    for(let i = 0; i < 10; i++) {
        console.log("C'est le message: ", i);
    }
</SyntaxHighlighter>

## TL;DR

- On utilise une **boucle** afin d'exécuter plusieurs fois un bloc d'instructions. Chaque exécution est appelée un tour de boucle ou encore une **itération**. Le bloc d'instructions associé à une boucle est appelé le corps de la boucle.
- La boucle `while` permet de répéter des instructions tant qu'une condition est vérifiée. La boucle `for` ajoute la possibilité d'effectuer un traitement à l'entrée dans la boucle (initialisation) et après chaque tour de boucle (étape).
- La variable utilisée dans l'initialisation, la condition et l'étape d'une boucle `for` est appelée le compteur de la boucle.
- Il faut toujours que la condition d'une boucle `while` puisse devenir fausse afin d'éviter le risque d'une boucle infinie.
- On s'interdit de manipuler le compteur d'une boucle `for` à l'intérieur du corps de la boucle. Toutes les boucles peuvent s'écrire avec un `while`. La boucle `for` est à privilégier lorsque le nombre d'itérations est connu à l'avance.

## Exercice:

Écrivez le code d'une fonction en JavaScript appelée sommeDesCarres qui prend un nombre entier positif en paramètre et renvoie la somme des carrés de tous les nombres de 1 jusqu'à ce nombre, en utilisant une boucle while ou for.

Renvoyez `-1` lorsque la valeur n'est pas un entier positif compris entre 1 et 9.

### Exemples

Si l'on appelle la fonction avec l'argument 3, la fonction doit renvoyer 1^2 + 2^2 + 3^2, soit 14.
Soit 1 à la puissance 2
Les valeurs suivantes seronts testé:

| ordre | valeur |
| ----- | ------ |
| 1     | 8      |
| 2     | -1     |
| 3     | 5      |
| 4     | a      |
| 4     | 7      |
| 4     | test   |
