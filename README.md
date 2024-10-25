# Javascript_1
Explications JS 


## Définition 

Le JavaScript est un langage de script orienté objet qui est interprété ou compilé à la volée et exécuté par le navigateur.

Il est régit par la norme ECMAScript qui est publiée annuellement.

## Utilisation console

- console.log()
- console.debug()
- console.warn()
- console.error()

## Interactions avec l'utilisateur

- alert()
- prompt() => renvoie un champ de saisie et les boutons "Ok" / "Annuler"
- confirm() => renvoie juste les boutons "Ok" / "Annuler" (correspond +/- au "OuiNon()" en Windev)

## Déclarations des variables

- var 
- let
- const

![image](https://github.com/user-attachments/assets/cb0dcb57-12db-4e36-8702-ea56cf54100b)


## Les types de valeurs

- Number (comprend les entiers et les nombres à virgules)
- BigInt
- String
- Boolean
- Undefined
- Null
- Object (les Date sont des Objects en JS, il n'y a pas de "type" Date)

  Afin d'obtenir le type d'une variable on utilise **typeof**

## Exemple pour obtenir le type d'une variable Object

   const now = new Date()

 - via la propriété constructor

  now.constructor.name => renvoie Date

 - via l'opérateur instanceof

  now.instanceofDate => renvoie True

  ## DOM : définition

  Document Object Model

  C'est la représentation sous forme d'objets des données qui composent la structure et le contenu d'une page web.

  Le DOM est une API.

  ![image](https://github.com/user-attachments/assets/e2dc544a-7361-4ac5-b204-615d14229646)


## Quelques fonctions utiles du DOM

  - getElementById : retourne l'élément ayant l'attribut id spécifié
    
  - querySelector : retourne le premier élément qui correspond au sélecteur CSS
    
  - querySelectorAll : retourne une « NodeList » avec tous les éléments qui correspondent au sélecteur CSS

## Propriétés des éléments du DOM

    - id : permet d'obtenir/modifier la valeur d'un attribut
    
    - innerHTML : permet d'obtenir/modifier le contenu de la balise
    
    - textContent : permet d'obtenir/modifier le contenu textuel
    
    - className : permet d'obtenir/modifier le contenu de l'attribut "class" d'une balise
    
    - classList : permet les interactions avec la valeur de l'attribut "class" d'une balise (grâce aux méthodes : add, remove, contains, replace, toggle*) *toggle permet l'ajout / la suppression de la classe spécifiée.
    
    - firstElementChild / lastElementChild : permet d'obtenir le premier / dernier élément de la balise
    
    - children : permet d'obtenir 1 collection avec tous les éléments enfants de la balise
    
    - value : permet d'obtenir/modifier la valeur d'une balise "input", "textarea", "select"
    
    - valueAsNumber : permet d'obtenir/modifier la valeur d'une balise "input" convertie en type Number (disponible que sur des balises Number et Date)
    
    - checked : permet d'obtenir/modifier l'état d'une balise "input" de type "checkbox"
    
    - addEventListener("click",...) : permet d'ajouter un code en sommeil sur l'évènement "clique" de l'élément ciblé
   
## Quelques fonctions JS

   - parseInt(a,b)
    
   - parseFloat(a,b)
   
   **==> sont les 2 fonctions qui permettent de convertir une variable de type String**
   
  - toFixed(nbChiffre) : renvoie le nombre formaté en chaîne de caractères avec une notation à point-fixe.
    
  - toLocaleString(locale,options) : renvoie le nombre formaté en chaîne de caractères en tenant compte de la locale ('fr-be' par exemple)
   


    en JS, pour les fonctions mathématiques, on utilise l'object **MATH** (exemple : Math.pi, Math.round, Math.floor, Math.ceil, Math.random,...) ou des **constantes** telles que MIN_VALUE, MAX_VALUE, MIN_SAFE_INTEGER, MAX_SAFE_INTEGER, EPSILON.

    Certaines **fonctions sur les nombres** existent également comme "isFinite()", "isNaN()" (utilisée pour savoir si c'est un nombre ou pas), "isInteger", "isSafeInteger", ...

    
   
  ### Autres fonctions sur les STRING
   
   - 3 façons d'effectuer la concaténation : 
   
     1) via l'opérateur "+" 
     2) via la méthode ".concat"
     3) via le template "String" (via les `` avec `${chaine1} ${chaine2}`)
     
  - indexOf()
    
  - includes()
    
  - startsWith / endsWith
    
  - localeCompare()
    
  - trim()
    
  - trimStart()
    
  - trimEnd()
    
  - toUpperCase()
    
  - toLowerCase()
    
  - toLocaleUpperCase()
    
  - toLocaleUpperCase()
    
  - padStart()
    
  - padEnd()
    
  - replace()
    
  - replaceAll()
    
  - substring()
    
  - slice()
    
  - split() 


         
## Opérateurs

   - Egalité Faible (==) , Inégalité Faible (!=)
   - Egalité Stricte (===), Inégalité Stricte (!==)
   - Attention, préconiser l'utilisation des opérateurs strictes.
   - a++ => post-action
   - ++a => pré-action
   - le "_ET_" de Windev devient &&
   - le "_OU_" de Windev devient ||

Les autres opérateurs sont +/- similaires à ceux de Windev et facile à apprendre :

![image](https://github.com/user-attachments/assets/f31f187f-fb7f-4a90-a0be-99aaa87513d5)

## Opérateur ternaire 
![image](https://github.com/user-attachments/assets/acaed438-a22a-483d-aef8-784bdbc74e9d)


## Opérateur "Nullish coalescing"

![image](https://github.com/user-attachments/assets/5f88f274-2fa9-48dc-9601-7fd02125389d)

![image](https://github.com/user-attachments/assets/1df609f4-390e-41a4-8d88-1e59763c2004)


## Les Objects 

Le type « Object » permet de stocker un ensemble de valeur sous forme de propriété.

![image](https://github.com/user-attachments/assets/2beec1a6-2b39-4610-8c45-23042969d1b9)


Exemple avec les accesseurs de propriétés : 

const tabObjets = {
clé1 : 'Valeur1',
clé2 : 'Valeur2'
};

tabObjets['clé1'] = 'ValeurA';
tabObjets.clé2 = 'ValeurB';

### Le "Optional chaining" opérateur (?.) 

Permet d'éviter d'accéder à une propriété d'un objet "null" ou "undefined" (sinon erreur levée par le JS).

Si on utilise ceci sur une propriété d'un objet "null" ou "undefined" ça renvoie uniquement "undefined" et non une erreur.

Exemple : 

![image](https://github.com/user-attachments/assets/8d79666b-839e-4d6c-b79a-c11c17d59e0f)


## Les Dates 

En JS, une date est stockée sous forme d'un entier qui correspond au nombre de millisecondes écoulées depuis le 1er janvier 1970 (UTC).

![image](https://github.com/user-attachments/assets/f0024b11-d401-45c7-b479-2d391a9edb89)

- getDate() / setDate(nbJour) : obtenir / modifier la valeur du JOUR du mois d'une date
- getMonth() / setMonth(indexMois) : obtenir / modifier la valeur de l'index (de 0 à 11) représentant le mois d'une date
- getFullYear() / setFullYear(nbAnnée) : obtenir / modifier la valeur de l'année d'une date
- getHours() / setHours(nbHeure) : obtenir / modifier la valeur de l'heure d'une date
- getMinutes() / setMinutes(nbMinute) : obtenir / modifier la valeur des minutes d'une date
- getSeconds() / setSeconds(nbSeconde) : obtenir / modifier la valeur des secondes d'une date
- getMilliseconds() / setMilliseconds(nbMilliseconde) : obtenir / modifier la valeur des millisecondes d'une date
- getDay() : obtenir / modifier la valeur du jour de la semaine d'une date (de 0 à 6)
- getTime() : obtenir en millisecondes le temps écoulés depuis le 1er janvier 1970

## Fonctions utiles Dates 

- toString()
- toISOString()
- toJSON()
- toLocaleString(locale,options)
- toLocaleDateString(locale,options)
- toLocaleTimeString(locale,options)

## Structures if/else et Switch

Exemple if/else : 

![image](https://github.com/user-attachments/assets/41fe44c5-afca-4938-9c21-0433ff80c401)

Exemple Switch : 

![image](https://github.com/user-attachments/assets/347f0c68-798b-4b91-b571-b7504a247522)

## Boucles 

- WHILE
  ![image](https://github.com/user-attachments/assets/39da958f-ca99-4271-8bdf-7fa1850ea7bb)

- DO ... WHILE
![image](https://github.com/user-attachments/assets/eb2fa641-89cc-4621-9360-4186fcdeac35)
  
- FOR
  ![image](https://github.com/user-attachments/assets/a232d22b-e84e-45e4-9ffa-9f929a6daeb8)

On utilise également les instructions CONTINUE et BREAK en JavaScript :)

- forEach(...) => parcourt la totalité des éléments d'une collection. Attention : Il est impossible d'arrêter le traitement de cette boucle sauf en déclenchant une exception (Code d'erreur).  
  
- for ... of  => permet de parcourir des objets itérables (Array, Map, String,...) 
  
- for ... in => permet de parcourir les propriétés énumérables d'un objet (Exemple : for (const key in tableauClesValeurs) {} )

## Collections indexées "ARRAY" 

Une collection indexée est une structure de données qui permet de stocker un ensemble de valeurs dans une variable et de les rendre accessibles à l’aide d’un index.

![image](https://github.com/user-attachments/assets/fd950c2d-f849-4c6b-bb6f-2a87efce49b0)

- Littéral : const arr = [1, 2, 3];
  
- Constructeur : const arr = new Array(1, 2, 3);
  
- Accéder à un élément : arr[index]
  
__Ajouter/Supprimer des éléments : __

- push(item) : Ajoute à la fin.
  
- pop() : Supprime le dernier élément.
  
- unshift(item) : Ajoute au début.
  
- shift() : Supprime le premier élément.
  
- splice(start, deleteCount, ...items) : Modifie à partir d'un index (ajout/suppression). (la fonction ".toSpliced()" est similaire à "splice()" sauf que celle-ci crée une copie de la collection qui est modifiée et renvoyée) 
  
- slice(start, end) : Extrait une portion sans modifier l'original. 
  
- join([séparateur]) : Renvoie une chaîne de caractères en concaténant tous les éléments d'u tableau séparés par le séparateur (par défaut: ","). (La fonction "toString()" est similaire à cette fonction join).

  __Itérations : __
  
- forEach(callback) : Exécute une fonction pour chaque élément.
  
- map(callback) : Crée un nouveau tableau en appliquant une fonction à chaque élément.
  
- filter(callback) : Crée un nouveau tableau avec les éléments qui passent un test.
  
- reduce(callback, initialValue) : Réduit le tableau à une seule valeur en appliquant une fonction.
  
- some(callback) : Retourne true si au moins un élément passe le test.
  
- every(callback) : Retourne true si tous les éléments passent le test.
  
- find(callback) : Retourne le premier élément qui passe le test.

- findLast(callback) : Retourne le dernier élément qui passe le test. 
  
- findIndex(callback) : Retourne l’index du premier élément qui passe le test.
  
__Recherches et transformations : __

- indexOf(item) : Retourne l'index d'un élément (ou -1).
  
- includes(item) : Vérifie si un élément est présent.
  
- join(separator) : Crée une chaîne de caractères à partir des éléments.
  
- concat(...arrays) : Combine plusieurs tableaux.
  
- flat(depth) : Aplati un tableau imbriqué.
  
- reverse() : Inverse l'ordre des éléments. (la fonction ".toReversed() est similaire à "reverse()" sauf que celle-ci crée une copie de la collection qui est modifiée et renvoyée) 

- sort(compareFunction) : Trie le tableau. (la fonction ".toSorted([methodeComparaison])" est identique à "sort()" sauf que celle-ci crée une copie de la collection qui est modifiée et renvoyée)
  
__Autres : __

- length : Propriété pour obtenir la taille du tableau.
  
- fill(value, start, end) : Remplit le tableau avec une valeur.
  
- copyWithin(target, start, end) : Copie une portion du tableau vers un autre endroit.

## Le Type "MAP"

** TO BE CONTINUED ** 

## TRY / CATCH / FINALLY


## 











        



  

  
