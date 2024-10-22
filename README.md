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

   - a++ => post-action
   - ++a => pré-action

Les autres opérateurs sont +/- similaires à ceux de Windev et facile à apprendre :

![image](https://github.com/user-attachments/assets/f31f187f-fb7f-4a90-a0be-99aaa87513d5)


## Les Objects 

Le type « Object » permet de stocker un ensemble de valeur sous forme de propriété.

![image](https://github.com/user-attachments/assets/2beec1a6-2b39-4610-8c45-23042969d1b9)

Exemple 

        



  

  
