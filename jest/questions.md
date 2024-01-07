# Jest

## Issue: Cannot find name 'describe'.

[Cannot find name 'describe'. Do you need to install type definitions for a test runner?](https://stackoverflow.com/questions/54139158/cannot-find-name-describe-do-you-need-to-install-type-definitions-for-a-test)

If you encounter the error "Cannot find name 'describe'. Do you need to install type definitions for a test runner?", follow these steps:

1. Install Jest type definitions:
```bash
npm install --save-dev @types/jest
```

2. Add the following import statement at the beginning of your test file:
```ts
import '@types/jest';
```
This ensures that TypeScript recognizes the Jest types.



# tsconfig

## Issue: 'supertest_1.default is not a function'

[Error message 'supertest_1.default is not a function' when starting e2e test #99](https://github.com/nestjs/schematics/issues/99)

The following error message is output when calling 'npm run test:e2e' in a newly generated nest.js app:

```ts
    TypeError: supertest_1.default is not a function

      17 |
      18 |   it('/ (GET)', () => {
    > 19 |     return request(app.getHttpServer())
         |            ^
      20 |       .get('/')
      21 |       .expect(200)
      22 |       .expect('Hello World!');

      at Object.it (app.e2e-spec.ts:19:12)
```

The problem is fixed when replacing the supertest import in the e2e spec file to this:

```ts
import * as request from 'supertest';
```

### Solution

The docs show `import * as request from 'supertest'` for a reason. Supertest does not use a default export. Unless you add `esModuleInterop: true` to your `tsconfig` you'll need to use the commonjs import syntax for Typescript. If you need further support, please visit our [Discord](https://discord.com/invite/nestjs)


## Issue: "express.default is not a function" in a Container

[Getting "express.default is not a function" error when i run node server in a container](https://stackoverflow.com/questions/63744824/getting-express-default-is-not-a-function-error-when-i-run-node-server-in-a-co)

I'm getting an express.default is not a function error when i run my node server inside a remote container.

main.ts file:
```ts
import * as express from 'express';
...
const server = (express as any).default();
...
```

logs:
```bash
/main.js:112
2020-09-04 10:58:29const server = express.default();
const server = express.default();
2020-09-04 10:58:29^
^
2020-09-04 10:58:29TypeError: express.default is not a function
TypeError: express.default is not a function
2020-09-04 10:58:29at Object.<anonymous> (/main.js:112:35)
...
```

### Solution

Turn on "esModuleInterop": true, from your tsconfig.json file
```json
{
  "compilerOptions": {
    "esModuleInterop": true
  }
}
```
