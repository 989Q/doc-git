## Next.js + GraphQL Blueprint

This blueprint likely provides a professional-grade setup for integrating Next.js with GraphQL. 

YouTube Tutorial: NextJS + GraphQL Blueprint: [Professional Grade Setup](https://www.youtube.com/watch?v=XzE-PzALyDc&t=817s)

GitHub Repository: [Next-GQL-Dogs](https://github.com/jherr/next-gql-dogs)



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



## Tanstack query

In the provided code snippet, the `prefetchTodos` function is defined in the `client/pages/index.js` file. This function uses the `queryClient.prefetchQuery` method to prefetch the results of the `fetchTodos` query.

```tsx
// Import necessary dependencies, including queryClient and fetchTodos function

const prefetchTodos = async () => {
  // Use queryClient.prefetchQuery to prefetch the results of the fetchTodos query
  await queryClient.prefetchQuery({
    queryKey: ['todos'],  // Unique key to identify the query in the cache
    queryFn: fetchTodos,   // The function that fetches the todos data
  })
}
```

Explanation:

- `queryKey:` It is a unique identifier for the query. In this case, the query key is set to `['todos']`. This key is used to identify the query in the cache.

- `queryFn:` This is the function that fetches the data. In the example, it's `fetchTodos`. This function is responsible for making the actual network request to get the todos data.

- `await queryClient.prefetchQuery:` This line initiates the prefetching process. It asynchronously prefetches the data and stores it in the cache with the specified query key.

Make sure to check the documentation provided at [tanstack-query Prefetching Guide](https://tanstack.com/query/v4/docs/react/guides/prefetching) for more details and advanced usage.



## Install with bash

### GraphQL and Apollo Server (Server-side)

```bash
# Install GraphQL and Apollo Server (for server-side)
npm i graphql apollo-server-micro
```

- `graphql:` The core GraphQL library.
- `apollo-server-micro:` Apollo Server implementation for microservices.

### GraphQL Code Generation

```bash
# Install GraphQL code generation tools
pnpm add -D @graphql-codegen/cli @graphql-codegen/typescript
pnpm add -D @graphql-codegen/typescript-operations
pnm add -D @graphql-codegen/typescript-graphql-request
pnpm add -D @graphql-codegen/typescript-react-query
```

- `@graphql-codegen/cli`: GraphQL Code Generator command-line interface.
- `@graphql-codegen/typescript`: GraphQL Code Generator plugin for TypeScript.
- `@graphql-codegen/typescript-operations`: GraphQL Code Generator plugin for TypeScript operations.
- `@graphql-codegen/typescript-graphql-request`: GraphQL Code Generator plugin for generating TypeScript types for GraphQL requests.
- `@graphql-codegen/typescript-react-query`: GraphQL Code Generator plugin for generating React Query hooks.

### Tanstack's React Query

```bash
# Install tanstack's React Query
pnpm add @tanstack/react-query
```

- `@tanstack/react-query`: React Query library from tanstack.


### Additional Resource
You've also provided a link to a blog post on how to use GraphQL Code Generator with React Query from nhost.io.

[How to Use GraphQL Code Generator with React Query](https://nhost.io/blog/how-to-use-graphql-code-generator-with-react-query)
