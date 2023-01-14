# React version 18 update eslint and prettier

## Install prettier
```
npm i -D prettier eslint-plugin-prettier eslint-config-prettier
```

## My archive `.eslintrc.js`
```js
module.exports = {
  env: {
    browser: true,
    es2021: true,
    jest: true,
    node: true,
  },
  extends: [
    'eslint:recommended',
    'plugin:react/recommended',
    'plugin:react-hooks/recommended',
    'plugin:prettier/recommended',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parser: '@babel/eslint-parser',
  parserOptions: {
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 'latest',
    sourceType: 'module',
  },
  plugins: ['react', 'prettier', 'react-hooks'],
  settings: {
    react: {
      version: 'detect',
    },
  },
  rules: {
    'react/react-in-jsx-scope': 'off',
  },
};
```
> ## There may be updates or many other modifications. But this is the starting base of the file.

## My archive `.prettierrc.js`
```js
module.exports = {
  arrowParens: 'always',
  bracketSpacing: true,
  endOfLine: 'lf',
  htmlWhitespaceSensitivity: 'ignore',
  insertPragma: false,
  jsxSingleQuote: false,
  printWidth: 80,
  proseWrap: 'always',
  quoteProps: 'as-needed',
  requirePragma: false,
  semi: true,
  singleQuote: true,
  tabWidth: 2,
  trailingComma: 'all',
  useTabs: false,
  vueIndentScriptAndStyle: false,
  embeddedLanguageFormatting: 'off',
};
```
## Important: If you use the VS Code extension for `Prettier`, point the project's `.prettierrc.js` path in the extension settings. To do so, just add this to VS Code settings.json:
```json
{
  "prettier.configPath": "./.prettierrc.js"
}
```
## Create the `.babelrc.json` file in the root of the project with the following data:
```json
{
  "presets": ["@babel/preset-env", "@babel/preset-react"]
}
```
