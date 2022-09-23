# Langage Javascript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les `structures` de base du langage ✔️
- les normes `ecmascript` ✔️
- l'utilisation de l'`asynchrone` ✔️
- les spécifités du mot-clef `this` ✔️

## 💻 Je code en Javascript

### Un exemple de code commenté ✔️

let string = "Hello world !";

// Converti la chaine de caractère en Ascii
function convertInAscii(string) {
  let stringInAscii = [];
  for (letter of string) {
    stringInAscii.push(letter.charCodeAt(0));
  }
  return stringInAscii;
}

// Ajoute des zeros à la chaine de caractère tant que sa longueur ne respecte pas celle d'un octet
function addZero(string) {
  return string.padStart(8, '0');
}

// Converti un nombre de base 10 en base 2
function convertNumInOctet(int) {
  let intToReturn = "";
  while (int !== 0) {
    // permet d'inversé la chaine de charactère
    intToReturn = (int % 2) + intToReturn;
    int = parseInt(int / 2);
  }
  return addZero(intToReturn);
}

// Converti un tableau Ascii (tableau de nombre) en chaine de caractère binaire
function convertAsciiInBin(array) {
  const arrayConverted = array.map((letter) => {
    return convertNumInOctet(letter);
  });
  return arrayConverted.join(" ");
}

// Fait l'assemble de la conversion en ascii vers le décimal et le décimale vers la base 2
function convertStringInBin(string) {
  return convertAsciiInBin(convertInAscii(string))
}

console.log(convertStringInBin(string));

### Utilisation dans un projet ✔️

[ien du projet] https://github.com/Barret-Pierre/Mastermind

Description : Création d'un mastermind 

### J'ai utilisé ce langage en production ✔️

[lien du projet] https://barret-pierre.github.io/Mastermind_App/

Description : Déploiement de la page Mastermind sur github

### J'ai utilisé ce langage en environement professionnel ✔️

Description : J'ai utilisé JS dans le but de créer l'interface d'un site de mise en realtions B2B, durant un stage de fin de formation. J'ai utilisé le Framework VueJs afin de rendre le front maintenanble par léquipe de production. 

## 🌐 J'utilise des ressources

### MDN

- https://developer.mozilla.org/fr/docs/Web/JavaScript
- Documentation Web participative regroupant tout les langages de base au web développement

### Stackoverflow

- https://stackoverflow.com/
- Blog participatif d'entraide concernant différent langages de programmation

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️

