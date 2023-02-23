## Index

- [Scripts](#scripts)
- [Comments to separate dependencies](#comments-to-separate-dependencies)
- [Index css](#index-css)
- [ESLint rules](#eslint-rules)
- [Editor config](#editor-config)
- [Commands](#commands)
  - [Nextjs](#nextjs)
    - [npm](#nextjs-npm)
    - [yarn](#nextjs-yarn)
  - [Material UI](#material-ui)
    - [npm](#material-ui-npm)
    - [yarn](#material-ui-yarn)
  - [Material UI icons](#material-ui-icons)
    - [npm](#material-ui-icons-npm)
    - [yarn](#material-ui-icons-yarn)
  - [Roboto font](#roboto-font)
    - [npm](#roboto-font-npm)
    - [yarn](#roboto-font-yarn)
  - [Material UI and icons](#material-ui-and-icons)
    - [npm](#material-ui-and-icons-npm)
    - [yarn](#material-ui-and-icons-yarn)
  - [Create a eslint config file](#create-a-eslint-config-file)
    - [npm](#create-a-eslint-config-file-npm)
  - [Generate a tsconfig.json](#generate-a-tsconfigjson)
    - [npm](#generate-a-tsconfigjson-npm)
  - [Create react app](#create-react-app)
    - [npm](#create-react-app-npm)
    - [yarn](#create-react-app-yarn)
  - [Create react app with Typescript](#create-react-app-with-typescript)
    - [npm](#create-react-app-with-typescript-npm)
    - [yarn](#create-react-app-with-typescript-yarn)
  - [Install tailwind](#install-tailwind)
    - [npm](#install-tailwind-npm)
    - [yarn](#install-tailwind-yarn)
  - [Generate tailwind full file config](#generate-tailwind-full-file-config)
    - [npm](#generate-tailwind-full-file-config)-npm)

# Scripts

```bash
  "linter": "eslint --fix src/**/*.{ts,tsx}"
```

# Comments to separate dependencies

```bash
  // Third-party dependencies

  // Current project dependencies
```

# Index css

```bash
  * {
    margin: 0;
    padding: 0;
    list-style: none;
    /* user-select: none; */
    box-sizing: border-box;
  }

  body {
    font-family: "Roboto", sans-serif;
  }

  ::-webkit-scrollbar {
    width: 5px;
    opacity: 0;
    background: transparent;
  }

  ::-webkit-scrollbar:hover {
    opacity: 1;
  }

  ::-webkit-scrollbar-thumb {
    background-color: #9b59b6;
    border-radius: 5px;
  }

  img {
    width: 100%;
    height: 100%;
  }
```

# ESlint rules

```bash
  "no-multiple-empty-lines": [
    "error",
    {
      "max": 1
    }
  ]
```

# Editor config

```bash
  root = true

  [*.{js,ts,tsx}]
  blank_line_maximum = 1
  end_of_line = lf
  insert_final_newline = true
  trim_trailing_whitespace = true
```

# Commands

## Nextjs

#### npm

```bash
  npx create-next-app@latest
```

#### yarn

```bash
  yarn create next-app
```

## Material UI

#### npm

```bash
  npm install @mui/material @emotion/react @emotion/styled
```

#### yarn

```bash
  yarn add @mui/material @emotion/react @emotion/styled
```

## Material UI icons

#### npm

```bash
  npm install @mui/icons-material
```

#### yarn

```bash
  yarn add @mui/icons-material
```

## Roboto font

#### npm

```bash
  npm install @fontsource/roboto
```

#### yarn

```bash
  yarn add @fontsource/roboto
```

#### Then you can import it in your entry point like this:

```bash
  import '@fontsource/roboto/300.css';
  import '@fontsource/roboto/400.css';
  import '@fontsource/roboto/500.css';
  import '@fontsource/roboto/700.css';
```

## Material UI and icons

#### npm

```bash
  npm install @mui/material @emotion/react @emotion/styled @mui/icons-material
```

#### yarn

```bash
  yarn add @mui/material @emotion/react @emotion/styled @mui/icons-material
```

## Create a eslint config file

#### npm

```bash
  npm init @eslint/config
```

## Generate a tsconfig.json

#### npm

```bash
  tsc --init
```

## Create react app

#### npm

```bash
  npx create-react-app my-app
```

#### yarn

```bash
  yarn create react-app my-app
```

## Create react app with Typescript

#### npm

```bash
  npx create-react-app my-app --template typescript
```

#### yarn

```bash
  yarn create react-app my-app --template typescript
```

## Install tailwind

#### npm

```bash
  npm install tailwindcss autoprefixer postcss-cli
```

#### yarn

```bash
  yarn add tailwindcss autoprefixer postcss-cli
```

## Generate tailwind full file config

#### npm

```bash
  npx tailwindcss init tailwind.config.full.js --full
```