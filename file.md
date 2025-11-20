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