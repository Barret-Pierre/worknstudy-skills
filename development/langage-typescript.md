# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️
- les types de bases ✔️
- comment et pourquoi étendre une interface ❌
- les classes et les decorators ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️

// Déclaration de l'interface User permettant de créer un type personaliser qui décrient la structure d'un objet.
// L'objet User à un nom, un âge et une data d'anniverssaire qui est une propriété optionnelle
interface IUser {
  name: string;
  age: number;
  birthday?: string;
}

// Fonction pertmattant d'afficher un message cette fonction prend en paramêtre un Tableau de User et ne renvois rien
const prettyPrintWilder = (users: IUser[]): void => {
  users.map((user) => {
    console.log(`${user.name} is ${user.age} years old`);
  });
};

// Déclaration d'une constante wilder qui est un tableau de User
const wilders: IUser[] = [];
// Déclaration de plusieur User
const user1: IUser = { name: "Pierre", age: 23 };
const user2: IUser = { name: "Paul", age: 32, birthday: "10/02/1990" };
const user3: IUser = { name: "Jacques", age: 25 };

// Ajout des User dans le tableau Wilder
wilders.push(user1);
wilders.push(user2);
wilders.push(user3);

// Execution de la fonction prettyPrintWilder
prettyPrintWilder(wilders);


### Utilisation dans un projet ❌ / ✔️

[lien github](...)

Description :

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

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
