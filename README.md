

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

Those commands are so useful

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
