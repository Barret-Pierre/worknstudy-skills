# GraphQL

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la différence entre REST et GraphQL ✔️
- les besoins auxquels répond GraphQL ✔️
- la définition d'un schéma
- Query ✔️
- Mutation ✔️
- Subscription ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

Présentation de la partie Back du site WildBook

```typescript
async function bootstrap(): Promise<void> {
  // ... Building schema here
  const schema = await buildSchema({
    resolvers: [WildersResolver],
  });

  // Create the GraphQL server
  const server = new ApolloServer({
    schema,
  });
}
```

```typescript
// Stock the datasource entity
const repository = dataSource.getRepository(Wilder);

// Create a wilder resolver
@Resolver()
export class WildersResolver {
  // This is a mutation, whit it you can insert, update or delete data. Here we want to create a wilder profile.
  @Authorized()
  @Mutation(() => Wilder)
  async createWilder(
    @Arg("data") data: WilderInput,
    @Ctx() context: IContext
  ): Promise<Wilder> {
    data.user = context.me;
    return await repository.save(data);
  }

  // This is a query, whit it you can read data, here we want to fetch all the wilders with their upvotes and the skill wich is linked.
  @Query(() => [Wilder])
  async readWilders(): Promise<Wilder[]> {
    return await repository.find({
      relations: ["upvotes", "upvotes.skill"],
      order: {
        id: "ASC",
        upvotes: {
          skill: {
            name: "ASC",
          },
        },
      },
    });
  }
}
```

### Utilisation dans un projet ✔️

[lien github](https://github.com/Barret-Pierre/wild_book_docker_front)

Description : Partie front du site WildBook. Site permettant de travailler en équipe en fonction des compétences de chacun.

### Utilisation en production si applicable ❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### AppoloServer

- https://www.apollographql.com/docs/apollo-server/v3/getting-started
- Documentation technique permettant d'utiliser la librairie ApolloClient, facilitant la création et la documentation de l'API GraphQL.

### AppoloClient

- https://www.apollographql.com/docs/react/data/queries
- Documentation technique permettant d'utiliser la librairie ApolloClient, facilitant la consomation de l'API GraphQL coté front.

### GraphQL

- https://graphql.org/learn/
- Documentation technique permettant d'utiliser et de renforcer les conncaissances théorique de GraphQL.

### TypeGraphQL

- https://typegraphql.com/docs/installation.html
- Documentation technique permettant d'utiliser TypeGraphQL, une librairie facilitant l'utilisation de GraphQL avec TypeScript.

### Kinsta

- https://kinsta.com/fr/blog/graphql-vs-rest/
- Contenue théorique permettant de comprendre la différence entre les API GraphQL et Restfull.

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
