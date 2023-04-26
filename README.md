# <div align="center" >Facilities Management Project Coding Conventions</div>

<h3 align="center">The sef of guidelines for team to follow a project</h3>

---

1. **Function Name** should be named as verb

```typescript
const signIn = (async() = {});
```

2. **Variable Name** should be named as noun

```typescript
const name: string = 'User Name';
```

3. **Boolean Variable Name** should be started with prefix _"is"_ or _"has"_

```typescript
const isPasswordMatched: boolean = false;
```

4. **File Naming Style** should be use ke-bab style <span style="color:yellow">_ke-bab."type".ts_</span>

```typescript
add - address.dto.ts;
auth.controller.ts;
```

5. **Function Naming Style** should be use camelCase

```typescript
const signIn = (async() = {});
```

6. **Class & Interface & Type Naming Style** should be use PasCal style

```typescript
class AddAddressUseCaseInput {}

interface AddressProps {
  street: string | null | undefined;
}
type CatName = 'miffy' | 'boris' | 'mordred';
```

7. **Attributes Naming Order** should be follow with the alphabet order

```typescript
const object = {
  age: 19,
  family: 'home',
  name: 'Object',
};
```

8. **If Statement Declaration** should be make with the curly brace block instead of inline-code

```typescript
if (isValid) {
  /* Do somethin*/
}
```

9. **PRETTIER** should be config as below

```typescript
{
	"singleQuote": true,
	"tabWidth": 2,
	"semi": true,
	"trailingComma": "all"
}

```

10. **ESLINT** should be config as below

```typescript
module.exports = {
  parser: '@typescript-eslint/parser',
  parserOptions: {
    project: 'tsconfig.json',
    sourceType: 'module',
  },
  plugins: ['@typescript-eslint/eslint-plugin'],
  extends: [
    'plugin:@typescript-eslint/recommended',
    'plugin:prettier/recommended',
  ],
  root: true,
  env: {
    node: true,
    jest: true,
  },
  ignorePatterns: ['.eslintrc.js'],
  rules: {
    '@typescript-eslint/interface-name-prefix': 'off',
    '@typescript-eslint/explicit-function-return-type': 'off',
    '@typescript-eslint/explicit-module-boundary-types': 'off',
    '@typescript-eslint/no-explicit-any': 'off',
  },
};
```

11. **Testing convention** should be follow with the AAA pattern when writing unit test

```typescript
1) Arrange
2) Act
3) Assert
```

10. **Export Convention** every folder should have index.ts file to use it as importing

```typescript
export * from './app.router';
```

11. **Comment Convention** should be use _/\*\*/_ for commenting not _//_

```typescript
/* Arrange */
/* Act */
/* Assert */
```

13. **No Console log** when commit
14. **Git Pre-push / Pre-commit Hooks** should be use with **husky** libary

Enable Git hooks:

```
npm husky install
```

Automatically have Git Hooks enabled after intsall:

```

npm pkg set scripts.prepare="husky install"
```
15. Google TypeScript Style Guide 
[REFERENCE](https://google.github.io/styleguide/tsguide.html)
