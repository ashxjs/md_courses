# Les strings

## Concept
Une string est la représentation d'un mot ou d'un caractère.
Elle peut être créée de plusieurs façons:
 
<SyntaxHighlighter language="javascript" style="materialDark">
	const str1 = "Je suis une string"; // Double quote
	const str2 = 'Je suis une string'; // Simple quote
</SyntaxHighlighter>

Il n'y a aucune différence entre ces 3 façons de créer les strings. On doit simplement être sur de ne pas la fermer avec un caractère différent.

## Templated string
Une template string se délimite par ` (backtick) elles autorisent les string multi-lignes, les interpolations (quand on insère une valeur).

<SyntaxHighlighter language="javascript" style="materialDark">
const value = 99;
const multiligne = \`je suis
    une variable multi-lignes
\`;
const interpolatedVar = \`Nous avons ${value} employés.\`; // output: Nous avons 99 employés.
</SyntaxHighlighter>

## Objet

En JS, les string sont des objets ! Lorsque vous allez créer une string, elle va être stockée en mémoire sous la forme d'un tableau. Qui pour chacune des "cases" va contenir un caractère.

<img width="75%" src="https://usemynotes.com/wp-content/uploads/2021/06/How-to-access-the-characters-of-a-String.jpg" alt="javascript memory sample" />

<SyntaxHighlighter language="javascript" style="materialDark">
const str = "hello world!";
console.log(str[6]); // output: 'w'
</SyntaxHighlighter>

Mais vu que notre string `str` est un objet, elle possède aussi des attributs et des méthodes.
Comme c'est un tableau de caratères elle possède aussi l'attribut `length`.

### Méthodes
Elle possède de nombreuses méthodes nous allons en voir quelques une ensemble:

### includes
La méthode includes() de String values effectue une recherche sensible à la casse pour déterminer si une chaîne donnée peut être trouvée dans cette chaîne, en renvoyant true ou false selon le cas.

<SyntaxHighlighter language="javascript" style="materialDark">
    const email = "john.doe.hotmail.com";
    const isValid = email.includes("@"); // false
</SyntaxHighlighter>

### charAt
La méthode charAt() des valeurs String renvoie une nouvelle chaîne composée de l'unité de code UTF-16 à l'index donné.

<SyntaxHighlighter language="javascript" style="materialDark">
const sentence = 'The quick brown fox jumps over the lazy dog.';
const index = 4;
console.log(\`The character at index ${index} is ${sentence.charAt(index)}\`);
// Expected output: "The character at index 4 is q"
</SyntaxHighlighter>

### toLowerCase
La méthode `toLowerCase()` des valeurs String renvoie cette chaîne convertie en minuscules.

<SyntaxHighlighter language="javascript" style="materialDark">
    const userName = "jOhN";
    console.log(userName.toLowerCase()); // output: john
</SyntaxHighlighter>

### toUpperCase
La méthode toUpperCase() des valeurs String renvoie cette chaîne convertie en majuscules.

<SyntaxHighlighter language="javascript" style="materialDark">
    const userName = "john";
    console.log(userName[0].toUpperCase()); // output: J
</SyntaxHighlighter>

Tu pourras retrouver la liste complete des méthodes existantes ➡️ [ici](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#instance_properties) ⬅️

# Exercices
Tu devras coder ces différentes fonctions afin de valider ce chapitre !
- `reverseStr` qui prend en paramètre une string `str` et qui retourne cette string inversé (ex: "Hello World !" -> "! dlroW olleH")
- `isPapalindrome` recoit un parametre `str` et retourne `true` lorsque le mot est un palindrome definition ➡️ [ici](https://www.larousse.fr/dictionnaires/francais/palindrome/57418) ⬅️, `false` dans le cas contraire. (ex: kayak -> true, essayer -> false, essayasse -> true)
- `capitalize` qui recoit une string et met la première lettre en capital. (ex: bonjour -> Bonjour, john -> John, miaou -> Miaou)