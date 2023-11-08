# Les Structures conditionnelles

## Maîtriser les Conditions

Imaginez que vous êtes devant un distributeur de boissons : si vous appuyez sur le bouton de l'eau, vous obtenez de l'eau. Si vous appuyez sur celui du soda, vous obtenez du soda. Et si vous voulez un jus ? Il y a un bouton pour ça aussi ! En algo, on utilise des "si" et des "sinon" pour faire des choix similaires. C'est ce qu'on appelle les structures conditionnelles. 🚦

<div class="algo-code-bloc">
evenement = "eau"

Si evenement est equal a "eau" Alors
Donne de l'eau

Si evenement est equal a "soda" Alors
Donne du soda

Sinon garde la pièce du client (parceque je suis sure que ca t'es aussi arrivé)
</div>

Pour commencer, la déclaration `if` est votre premier bouton. Elle dit à votre programme : "Hey, si cette chose spécifique est vraie, alors fais quelque chose !" 👉👈 C'est la base de la prise de décision dans votre code.

Mais que se passe-t-il si la condition `if` n'est pas vraie ? Là, `else` entre en jeu, comme un plan B. Il dit : "Ok, si la première condition n'est pas vraie, alors faisons autre chose à la place." 🔄

Parfois, les choses ne sont pas si noires ou blanches, et vous pourriez avoir besoin de plus d'options. C'est là que `else if` arrive à la rescousse. Vous pouvez l'utiliser pour tester plusieurs conditions différentes l'une après l'autre, comme choisir entre eau, soda, ou jus. 🥤

En Javascript, on traduirait l'exemple ci-dessus comme ceci:
<SyntaxHighlighter language="javascript" style="materialDark">
function getMyDrink(askedDrink) {
    if ( askedDrink === "water" ) {
        return "water";
    } else if ( askedDrink === "coca" ) {
        return "coca";
    } else if ( askedDrink === "orangina" ) {
        return "orangina";
    } else {
        return "asked drink doesn't exist";
    }
}
</SyntaxHighlighter>

## Simplifier les Choix Multiples

Alors, accrochez-vous, car on va explorer la magie des conditions `switch` ! 🧙✨ Vous savez, parfois dans la vie, on doit choisir parmi plein d'options, un peu comme quand on est au buffet et qu'on doit décider entre pizza, pâtes, sushi ou salade. On ne peut pas juste dire "si pizza, alors je suis content", parce qu'il y a beaucoup trop d'options appétissantes. C'est pareil en code ! 😄🍕

Le `switch` en JavaScript, c'est comme votre propre chef cuisinier personnel qui peut préparer une variété de plats basés sur votre commande. Vous lui dites ce que vous voulez, et hop, il vous le prépare ! En termes de code, vous avez une expression et une série de cas (`case`) et le `switch` exécute le code correspondant à la valeur de l'expression. 🔄

Voici le truc cool : vous donnez à `switch` une valeur, et il la compare avec les valeurs spécifiées dans chaque `case`. Si ça correspond, il exécute le code associé à ce `case`. Sinon, il passe au suivant, jusqu'à ce qu'il trouve une correspondance ou atteigne l'instruction `default`, qui est un peu comme dire "et sinon, fais-moi juste un sandwich". 🥪

Utiliser `switch` rend votre code plus propre et plus lisible, surtout quand vous avez une longue liste de conditions. C'est comme avoir une télécommande pour sélectionner la chaîne que vous voulez regarder au lieu de zapper frénétiquement. 📺

Voici le meme code avec l'utilisation d'un switch !
<SyntaxHighlighter language="javascript" style="materialDark">
function getMyDrink(askedDrink) {
    switch (askedDrink) {
        case "water":
            return "water";
        case "coca":
            return "coca";
        case "orangina":
            return "orangina";
        default:
            return "asked drink doesn't exist";
    }
}
</SyntaxHighlighter>

Dans ce code, la fonction `getMyDrink` vérifie maintenant la valeur de askedDrink en utilisant une instruction `switch`. Chaque `case` correspond à une option de boisson possible. Si la valeur de `askedDrink` correspond à l'un des `case`, la fonction retournera cette boisson.

Si aucune correspondance n'est trouvée, le `default` sera exécuté, indiquant que la boisson demandée n'existe pas. Cela rend le code plus succinct et généralement plus facile à lire, surtout quand il y a un grand nombre de conditions à vérifier.

## Exercices

### Objectif

L'objectif de cet exercice est de tester votre compréhension des structures conditionnelles.

### Instructions

Pour valider cette exercice, vous devrez coder votre première calculatrice ! <br>
La valeur du paramètre `operator` ne pourra seulement être: `add`, `minus`, `times` ou `divide`.
Les paramètre `a` et `b` seront toujours des entiers positifs.

On utilisera le mot `return` suivie de l'operator voulu.
Exemple: `return 1 + 3;`

Voici les opération qui seront testé une part une.

| order |operator|a|b|
| -------- | -------- | ------- | -------- |
| 1 |add|10|20|
| 2 |minus|100|199|
| 3 |times|5|123|
| 4 |divide|100|4|

<SyntaxHighlighter language="javascript" style="materialDark">
function calcul(operator, a, b) {
    // la fonction devra retourné l'opération demandé
}
</SyntaxHighlighter>