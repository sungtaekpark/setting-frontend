# Setting Frontend Project
1. React/Typescript
2. ESLint/Prettier
   

## CRA template typescript
1. `npx create-react-app [project name] --template typescript`
2. `npm i @types/react`

## ESLint / Prettier setting
1. module 설치
- `npm install -D eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser`
- `npx install-peerdeps --dev eslint-config-airbnb`

2. root 경로에 `.eslintrc ` 파일 생성 및 내용 추가
```
{
  "env": {
    "browser": true,
    "es6": true,
    "node": true
  },
  "parser": "@typescript-eslint/parser",
  "plugins": ["@typescript-eslint","import"],
  "extends": [
    "airbnb",
    "airbnb/hooks",
    "prettier/react",
    "plugin:@typescript-eslint/recommended",
    "prettier/@typescript-eslint",
    "plugin:prettier/recommended"
  ],
  "globals": {
    "Atomics": "readonly",
    "SharedArrayBuffer": "readonly"
  }, 
  "parserOptions": {
    "ecmaVersion": 2020,
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "rules": {
    "linebreak-style": 0,
    "import/no-dynamic-require": 0,
    "import/no-unresolved": 0,
    "import/prefer-default-export": 0,
    "global-require": 0,
    "import/no-extraneous-dependencies": 0,
    "jsx-quotes": ["error", "prefer-single"],
    "react/jsx-props-no-spreading": 0, 
    "react/forbid-prop-types": 0,
    "react/jsx-filename-extension": [2, { "extensions": [".js", ".jsx", ".ts", ".tsx"] }],
    "import/extensions": 0,
    "no-use-before-define": 0, 
    "@typescript-eslint/no-empty-interface": 0,
    "@typescript-eslint/no-explicit-any": 0,
    "@typescript-eslint/no-var-requires": 0,
    "no-shadow": "off",
    "react/prop-types": 0,
    "no-empty-pattern": 0,
    "no-alert": 0,
    "react-hooks/exhaustive-deps": 0
  },
  "settings": { 
    "import/parsers": {
      "@typescript-eslint/parser": [".ts", ".tsx", ".js"] 
    }, 
    "import/resolver": { 
      "typescript": "./tsconfig.json" 
    }
  }
}
```
3. root 경로에 `.prettierrc` 파일 생성 및 내용 추가
```
{
  "parser": "typescript",
  "singleQuote": true,
  "printWidth": 110,
  "tabWidth": 2,
  "useTabs": false,
  "semi": true,
  "quoteProps": "as-needed",
  "jsxSingleQuote": true,
  "trailingComma": "all",
  "arrowParens": "always",
  "endOfLine": "auto",
  "bracketSpacing": true,
  "jsxBracketSameLine": false,
  "requirePragma": false,
  "insertPragma": false,
  "proseWrap": "preserve",
  "vueIndentScriptAndStyle": false 
  }
  ```

4. ESLint / Prettier VScode 확장 설치
5. Default formatter 설정
- file -> default setting -> setting -> "default formatter" 검색 -> esbenp.prettier-vscode 를 선택 -> VSCode 재부팅

