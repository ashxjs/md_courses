# Introduction à la POO 🚀

## Concept
La POO (Programmation Orienté Objet) ou OOP (Object-Oriented Programming en 🇬🇧) est un `paradigme` de programmation qui consiste à `encapsuler` les données et leurs traitements dans des objects.
En POO nous parlons de `class`, elle représente un modèle qui possède des `attributs` et des `methodes`.

Une class se déclare en écrivant le mot clés `class` suivi du nom choisie.
Exemple:
<SyntaxHighlighter language="javascript" style="materialDark">
class Chat {}
</SyntaxHighlighter>

## Le Constructeur
Le `constructor` est la méthode qui va permettre de construire notre objet. C'est donc la première méthode à être appelé. On la définit avec le mot clés `constructor`. Dans le corp de celle-ci, nous avons accés au `this`. Il représente l'objet crée en mémoire. Nous verrons avec des exemple plus concret un peu plus bas. Dans notre constructeur nous allons donner la première valeur à nos différents attributs.

<SyntaxHighlighter language="javascript" style="materialDark">
class Soldier {
    constructor() {
        this.x = "meow";
    }
}
</SyntaxHighlighter>

## Attributs
Les attributs permettent de stocker des valeurs appartiennant à un objet.
Les méthodes quant à elle permettent de définir les actions de notre objet.

Prenons l'exemple d'une classe représentant un soldat, ce soldat possède:
- un nom
- un prénom
- un grade
- une vie
- un nombre de dégat qu'il peut infliger

<SyntaxHighlighter language="javascript" style="materialDark">
class Soldier {
    constructor() {
        this.nom // son nom
        this.prenom // son prenom
        this.grade // son grade
        this.vie // sa vie en chiffre
        this.degat // les dégats qu'il inflige
    }
}
</SyntaxHighlighter>

Ici nous avons bien des attributs, ce sont bien des valeurs qui permettent bien de définir mon objets.
Maintenant, il faut que mon soldat puisse faire des actions.

C'est la que nous allons lui définir des méthodes:

- On veut qu'il attaque ses ennemis
- Qu'il subisse des dégats

Exemple:
<SyntaxHighlighter language="javascript" style="materialDark">
class Soldier {
    constructor() {
        this.nom // son nom
        this.prenom // son prenom
        this.grade // son grade
        this.vie // sa vie en chiffre
        this.degat // les dégats qu'il inflige
    }
}
</SyntaxHighlighter>

Nous avons définis notre class ou modèle ! Notre application sait désormais qu'il y a des soldats, qu'ils possèdent des `attributs` (nom, prenom, grade, vie, degat) et des méthodes (attaquer, recevoirDegats).
Mais comment je crée un soldat qui s'appelle Jean Dupont qui est Général des armées ?

Pour ce faire on créé une `instance` de notre class.
Cette instance va être chargé directement dans notre mémoires (RAM) ! Pour ce faire on utilise le mot clés `new` suivi du nom de la class ne surtout pas oublier les `()` qui permettent d'appeler le constructeur de notre class.

Le constructeur, c'est la méthode qui est appelé dès que tu crées un objet.
Pour créer notre Soldat Jean Dupont, il nous faut modifier notre class, pour que notre constructeur accepte nos différents paramètres (nom, prenom, grade, vie, degat).

<SyntaxHighlighter language="javascript" style="materialDark">
class Soldier {
    constructor(nom, prenom, grade, vie, degat) {
        this.nom = nom;
        this.prenom = prenom
        this.grade = grade;
        this.vie = vie;
        this.degat = degat;
    }
}
</SyntaxHighlighter>

### Les méthodes

Comme nous l'avons vu plus haut, les méthodes servent à définir les différentes actions que notre class peut effectuer. Ici nous avons besoin d'ajouter des actions à notre class. Nous voulons que notre soldat puisse:

- On veut qu'il attaque ses ennemis
- Qu'il subisse des dégats

#### Méthodes Attaque d'ennemis
Chaque soldat possède sa propre vie et ses propres dégats.

<SyntaxHighlighter language="javascript" style="materialDark">
    const john = new Soldier("Doe", "John", "Major", 100, 25);
    const spidey = new Soldier("Parker", "Peter", "bleu", 200, 50);
</SyntaxHighlighter>

En toute logique lorsque j'attaque un autre soldat, il faut que je lui fasse subir autant de dégat que mon soldat le peu. Le nombre de dégat se réccupère avec l'attributs `degats`. Il nous faut aussi un objet de la class `Soldier` qui est l'objet qui va recevoir nos dégats. Les dégats seront reçue vient une autre méthode appelé `recoitDegats`.

<SyntaxHighlighter language="javascript" style="materialDark">
class Soldier {
    constructor(nom, prenom, grade, vie, degat) {
        this.nom = nom;
        this.prenom = prenom
        this.grade = grade;
        this.vie = vie;
        this.degat = degat;
    }
    attaque(ennemie) {
        ennemie.recoitDegats(this.degat); // on appelle la méthode recoitDegats avec notre capacité de dégat
    }
}
</SyntaxHighlighter>

#### Méthodes reçevoir des dégats
Nous allons nous attaqué à la dernière méthode de notre class. Ici on veut que notre soldat subisse des dégats c'est à dire qu'il perde de la vie. Pour ce faire nous avons à soustraire de la vie selon les dégats qu'on nous a infligé.

<SyntaxHighlighter language="javascript" style="materialDark">
class Soldier {
    constructor(nom, prenom, grade, vie, degat) {
        this.nom = nom;
        this.prenom = prenom
        this.grade = grade;
        this.vie = vie;
        this.degat = degat;
    }
    attaque(ennemie) {
        ennemie.recoitDegats(this.degat); // on appelle la méthode recoitDegats avec notre capacité de dégat
    }
    recoitDegats(degats) {
        this.vie -= degats; // on soustrait le nombre de dégat de notre vie
        console.log(this.prenom, "a perdu", degats, "points de vie.");
        if(this.vie <= 0) {
            console.log(this.prenom, "est mort 💀");
        } else {
            console.log("vie restante:", this.vie);
        }
    }
}
</SyntaxHighlighter>

### Notre première instance
Maintenant que nous avons créer notre class, il faut maintenant créer des objets qui la représente.

Lorsque notre application est chargé dans la mémoire, elle sait à présent qu'il existe une class `Soldier` mais qu'il n'existe pas d'instance (un objet `Soldier` en mémoire).

Pour créer une instance, on utilise le mot clés `new`.
Qui va charger dans la mémoire la class qui le précède.

<SyntaxHighlighter language="javascript" style="materialDark">
    new Soldier();
</SyntaxHighlighter>

Dans les parenthèses, nous allons renseigner ses paramètres.

🚨 Attention de bien respecter l'ordre 🚨

<SyntaxHighlighter language="javascript" style="materialDark">
    new Soldier("Doe", "John", "Major", 100, 25);
</SyntaxHighlighter>

Ici si nous voulons manipuler l'objet que nous avons créé, n'oublier de le stocker dans une variable.

<SyntaxHighlighter language="javascript" style="materialDark">
    const doe = new Soldier("Doe", "John", "Major", 100, 25);
</SyntaxHighlighter>

### Plus concrètement

Disons que notre ami `Spidey` attaque `John`, nous obtiendrons le code suivant:

<SyntaxHighlighter language="javascript" style="materialDark">
    const john = new Soldier("Doe", "John", "Major", 100, 25);
    const spidey = new Soldier("Parker", "Peter", "bleu", 200, 50);

    spidey.attaque(john); // on attaque john avec 50 points de dégats
    // affichera: John a perdu 50 points de vie.
</SyntaxHighlighter>

## TL;DR
Ce chapitre est l'un des plus complexe ! Car la Programmation Orientée Objet est un concepte avancé mais essentiel à aborder pour continuer sereinement le cours.

- On a vu que les `class` sont un modèle que l'on définit. Elles permettent d'encapsuler les données et leurs traitements.
- Elles possèdent des `attributs` qui sont les valeurs qui la définissent.
- Et des méthodes qui sont des actions qu'elles vont pourvoir faire pour intéragir avec ces `attributs`.
- Le `constructeur` est la fonction qui est appelé lorsque l'on instancie un objet. Il peut reçevoir un nombre indéfini de paramètre.

## Exercice
Créez une class `Animal`, qui possède:
- 3 attributs (name, race, age).
- 3 méthodes (getName, getRace, getAge).
    - getName: doit uniquement retourner le nom de l'animal
    - getRace: doit uniquement retourner la race de l'animal
    - getAge: doit uniquement retourner l'âge de l'animal
- Le constructeur de la class doit prendre les paramètres dans l'ordre suivant: name, race, age.