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
