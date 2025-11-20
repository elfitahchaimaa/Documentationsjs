categorie1:
//difference entre let var et const
JavaScript permet d’utiliser des variables avant qu’elles ne soient déclarées en plaçant les déclarations var en haut de leur portée contenante. Mais jusqu’au moment de la déclaration, sa valeur initiale sera indéfinie.

console.log(myVar); indéfini

var myVar = 5 ;

console.log(myVar); // 5

Bien que var ait rempli son rôle aux premiers jours de JavaScript, ses bizarreries conduisent souvent à des comportements inattendus et à des bogues.

L’essor de let et const
Pour surmonter les limites de « var », ECMAScript 6 (ES6) introduit 'let' et 'const'. En limitant l’existence de la variable à l’ensemble d’accolades le plus proche, tel qu’une fonction, une boucle ou un bloc conditionnel, ces deux mots-clés améliorent la déclaration de la variable avec l’étendue des blocs.

vol
La déclaration d’une variable qui peut être réaffectée ultérieurement est rendue possible par la commande « let ». Ceci est utile pour des variables telles que les compteurs de boucle ou les valeurs d’entrée dont les valeurs fluctuent au fil du temps.

let compteur = 0 ;

si (vrai) {

let compteur = 1 ; Ce compteur est différent de celui extérieur
console.log(compteur); // 1

}

console.log(compteur); // 0

Const
Lors de la création d’une variable dont la valeur ne doit pas être modifiée, le mot-clé « const » est utilisé. Si la variable est un objet ou un tableau, vous pouvez toujours modifier son contenu, elle n’est donc pas nécessairement immuable.

const utilisateur = { nom : « Alice » };

user.name = « Bob » ; Ce n’est pas grave

console.log()user.name ; Sorties « Bob »

utilisateur = { nom : « Charlie » }; Cela générera une erreur

Lequel utiliser ? 
L’utilisation de let et const au lieu de var est conseillée dans le développement JavaScript contemporain. Lorsque vous définissez des constantes, utilisez const autant que possible. Cela permet d’éviter les réaffectations involontaires et de clarifier votre intention. Utilisez let si vous savez qu’une variable doit être réaffectée. L’adoption de let et const réduit la probabilité d’erreurs liées à la portée et produit un code plus prévisible et plus facile à maintenir.

//fonction

Les déclarations de fonctions
Une définition de fonction (aussi appelée déclaration de fonction ou instruction de fonction) est construite avec le mot-clé function, suivi par :

Le nom de la fonction.
Une liste d'arguments à passer à la fonction, entre parenthèses et séparés par des virgules.
Les instructions JavaScript définissant la fonction, entre accolades, { }.
Le code suivant, par exemple, définit une fonction intitulée carré :

js

Copy
function carré(nombre) {
  return nombre * nombre;
}
La fonction carré prend un seul argument, appelé nombre. La fonction est composée d'une seule instruction qui renvoie l'argument de la fonction (nombre) multiplié par lui-même. L'instruction return spécifie la valeur qui est renvoyée par la fonction.

js

Copy
return nombre * nombre;
Les paramètres primitifs (comme les nombres) sont passés à la fonction par valeur. La valeur est passée à la fonction mais si cette dernière change la valeur du paramètre, cela n'aura pas d'impact au niveau global ou au niveau de ce qui a appelé la fonction.

Si l'argument passé à la fonction est un objet (une valeur non-primitive, comme un objet Array ou un objet défini par l'utilisateur), et que la fonction change les propriétés de cet objet, ces changements

//la difference entre primitifs et objets

 Variables de type primitif
 Les types primitifs sont : boolean, char, byte, short, int, long, float, double.
 Pour repr´esenter les valeurs de ces types, il faut un nombre fixe de bits : par exemple 8 bits pour les
 byteet 32 pour les int.
 Lorsqu'on d´eclare une variable, on donne son type : Une variable d´eclar´ee de type primitif contient
 une valeur de type primitif. Ainsi, lors des d´eclarations suivantes :
 Listing 11.1– (pas de lien)
 1 int n;
 2 char c = 'a';
 3 n=5;
 4 double d = 2.0;

 //objet
 
  Que se passe t il lorsque nous cr´eons une variable dont le type est une classe ?
 Date d = new Date();
 (On suppose que Date est la classe d´efinie dans le cours sur les classes et les objets). Une nouvelle
 variable, d est cr´ee. Par ailleurs, new Date() cr´ee une instance de la classe Date, un objet. Le
 point cl´e est le suivant : contrairement aux variables primitives du paragraphe pr´ec´edent, d ne contient
 pas un objet , mais une r´ef´erence `a un objet. Si une variable primitive contient des bits qui repr´esentent
 la valeur qu'elle contient, une variable de type complexe contient des bits qui repr´esentent une fac¸on
 d'acc´eder `a l'objet. Elle ne contient pas l'objet lui mˆeme, mais quelque chose qui permet de retrouver
 l'adresse o`u se situe l'objet en m´emoire. C'est pourquoi nous disons que ces variables contiennent
 l'adresse de l'objet ou encore un pointeur sur l'objet. Nous appellerons ces variables des variables
 r´ef´erences.
 Nous n'avons pas besoin de savoir comment la JVM impl´emente les r´ef´erences aux objets. C'est
 sans importance parce que nous ne pouvons les utiliser que pour acc´eder `a l'objet. Nous savons en
 revanche que pour un