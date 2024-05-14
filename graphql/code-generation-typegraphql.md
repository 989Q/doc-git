## Code Generation with TypeGraphQL

Web Example: [typegraphql](https://typegraphql.com/docs/installation.html)

**Packages installation**

First, we have to install the main package, as well as graphql-js and class-validator which are peer dependencies of TypeGraphQL:

```bash
npm i graphql class-validator type-graphql 
```

Also, the reflect-metadata shim is required to make the type reflection work:

``` bash
npm i reflect-metadata 
```

We must ensure that it is imported at the top of our entry file (before we use/import type-graphql or our resolvers):

```js
import "reflect-metadata"; 
```
