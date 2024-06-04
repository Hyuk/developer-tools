# Linter

Linter is a tool that analyzes source code to flag programming errors, bugs, stylistic errors, and suspicious constructs. It can also be used to enforce a coding standard.

## Installation

```bash
npm install --save-dev eslint @eslint/js
```

## Initialize ESLint

```bash
touch eslint.config.js
```

## Example ESLint configuration (eslint.config.js)

```javascript
import js from "@eslint/js";

export default [
  js.configs.recommended,
  {
    files: ["src/**/*.js"],
    ignores: ["**/*.config.js", "!**/eslint.config.js"],
    rules: {
      semi: ["error", "never"],
      "prefer-const": "error",
      "no-unused-vars": "warn",
      "no-undef": "warn"
    }
  }
];
```

## Lint code using the ESLint CLI

```bash
$ npx eslint project-dir/ file1.js
```
