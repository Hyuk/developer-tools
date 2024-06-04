# Linter

린터는 소스 코드를 분석하여 프로그래밍 오류, 버그, 스타일 오류 및 의심스러운 구조를 식별하는 도구입니다. 또한 코딩 표준을 강제하는 데 사용할 수 있습니다.

[Linter Docs](https://eslint.org/docs/latest/use/getting-started)

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
