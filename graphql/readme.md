### 🐣 Next.JS & GraphQL
NextJS + GraphQL Blueprint: Professional Grade Setup
- youtube : https://www.youtube.com/watch?v=XzE-PzALyDc&t=817s
- github : https://github.com/jherr/next-gql-dogs



</br>

### 🐣 codegen
- web : https://typegraphql.com/docs/installation.html

Packages installation
First, we have to install the main package, as well as graphql-js and class-validator which are peer dependencies of TypeGraphQL:
``` 
npm i graphql class-validator type-graphql 
```
Also, the reflect-metadata shim is required to make the type reflection work:
``` 
npm i reflect-metadata 
```
We must ensure that it is imported at the top of our entry file (before we use/import type-graphql or our resolvers):
``` 
import "reflect-metadata"; 
```



</br>

### 🐣 tanstack-query
Prefetching 
- web : https://tanstack.com/query/v4/docs/react/guides/prefetching

client / pages / index.js
```tsx
const prefetchTodos = async () => {
  // The results of this query will be cached like a normal query
  await queryClient.prefetchQuery({
    queryKey: ['todos'],
    queryFn: fetchTodos,
  })
}
```



</br>

### 🐣 bash
```bash
# GraphQL
npm i graphql apollo-server-micro
npm i graphql class-validator type-graphql

# codegen
pnpm add -D @graphql-codegen/cli @graphql-codegen/typescript
pnpm add -D @graphql-codegen/typescript-operations
pnpm add -D @graphql-codegen/typescript-graphql-request
pnpm add -D @graphql-codegen/typescript-react-query

# tanstack
pnpm add @tanstack/react-query
# - https://nhost.io/blog/how-to-use-graphql-code-generator-with-react-query
```
