For [Issue #69](https://github.com/jest-community/jest-runner-eslint/issues/69) on `jest-runner-estlint`.

Reproduction steps:

First run

```
eslint src
```

Output:

    /Users/samselikoff/Projects/oss/jest-runner-eslint-issue-69/src/response.js
       1:14  error  'console' is not defined                                                   no-undef
      40:21  error  Do not access Object.prototype method 'hasOwnProperty' from target object  no-prototype-builtins
      48:39  error  Do not access Object.prototype method 'hasOwnProperty' from target object  no-prototype-builtins

Then run

```
jest
```

Output:

    FAIL   lint  src/response.js
     ✕ ESLint (144ms)


    /Users/samselikoff/Projects/oss/jest-runner-eslint-issue-69/src/response.js
     1:14  error  Unexpected console statement  no-console
     1:14  error  'console' is not defined      no-undef
