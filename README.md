# Essential Tools Every Programmer Should Know to Level Up

In this space, I will show you tools that you must know to grow as a developer. It includes best practices and linters.

## 1) Editor config

`.editorconfig` is a plugin for your Code Editor or IDE that allows you to configure the way in which the source code of your project is formatted, with this it is possible to keep the code consistent in a simple way.

You need to install an extension in vscode to be able to run it
[Install now](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

### How to use it?

Go to the root of your project and create a new file called

```bash
.editorconfig
```

paste the following code

```bash
root = true

[*]
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
end_of_line = lf
# editorconfig-tools is unable to ignore longs strings or urls
max_line_length = off

[CHANGELOG.md]
indent_size = false
```

| Configuration                     | Explanation                                                 |
| --------------------------------- | ----------------------------------------------------------- |
| `root = true`                     | Applies to the root directory of the project                |
| `[*]`                             | Applies to all file types in the project                    |
| `indent_style = space`            | Sets the indentation style to spaces                        |
| `indent_size = 2`                 | Specifies each level of indentation to consist of 2 spaces  |
| `charset = utf-8`                 | Defines the character encoding as UTF-8                     |
| `trim_trailing_whitespace = true` | Removes trailing whitespace at the end of lines             |
| `insert_final_newline = true`     | Adds an empty line at the end of each file                  |
| `end_of_line = lf`                | Sets the line ending style to LF (Unix-style line endings)  |
| `max_line_length = off`           | Disables enforcement of a maximum line length for all files |
| `[CHANGELOG.md]`                  | Applies specifically to files named "CHANGELOG.md"          |
| `indent_size = false`             | Disables indentation size specifically for "CHANGELOG.md"   |

## 2) Eslint

is a static code analysis tool for identifying problematic patterns found in JavaScript code.

### How to use it?

Open your terminal

run the next command

```bash
npm init @eslint/config
```

you will see 3 ways to use eslint

```bash
? How would you like to use ESLint? …
  To check syntax only
▸ To check syntax and find problems
  To check syntax, find problems, and enforce code style
```

| Option                                                 | Description                                                                  |
| ------------------------------------------------------ | ---------------------------------------------------------------------------- |
| To check syntax only                                   | Validates code syntax and reports errors and warnings.                       |
| To check syntax and find problems                      | Detects common problems and potential bugs in addition to syntax validation. |
| To check syntax, find problems, and enforce code style | Enforces code style rules along with syntax checking and problem detection.  |

### Some rules that some day you will need

#### No multiple empty lines

This configuration ensures that your code does not have more than one consecutive empty line, helping to maintain code readability and consistency.

```bash
"rules": {
    "no-multiple-empty-lines": [ "error", { "max": 1 } ]
}
```

| Configuration  | Explanation                                                               |
| -------------- | ------------------------------------------------------------------------- |
| `"error"`      | Indicates that if the rule is violated, it should be treated as an error. |
| `{ "max": 1 }` | Sets the maximum number of allowed consecutive empty lines to 1.          |

#### No console logs

Is used to identify and report any uses of the console object in your JavaScript code. It is generally recommended to avoid using console.log() or other console methods in production code, as they can affect performance and may expose sensitive information.

```bash
"rules": {
    "no-console": "error"
}
```

| Configuration | Description                                                                                  |
| ------------- | -------------------------------------------------------------------------------------------- |
| `"off"`       | Turns off the rule, meaning no reporting will be generated for `console` usage.              |
| `"warn"`      | Generates a warning for each occurrence of `console` usage.                                  |
| `"error"`     | Generates an error for each occurrence of `console` usage. This indicates a stricter policy. |

#### indent your `Switch`

The "SwitchCase: 1" configuration specifically sets the indentation level for switch case statements. With this configuration, the code inside each case statement will be indented one level deeper than the switch statement itself, improving the visual separation between different cases.

```bash
"rules": {
     indent: [ "error", 2, { SwitchCase: 1 } ],
}
```

| Configuration           | Description     |
| ----------------------- | --------------- |
| Indent Level            | `"error"`       |
| Spaces per Indent Level | `2`             |
| Switch Case Indentation | `SwitchCase: 1` |

### Eslint commands

Automatically fixes common code issues and errors for TypeScript, TypeScript JSX, and JavaScript files in the "src" directory. It analyzes the code, identifies problems like coding mistakes or formatting inconsistencies.

```bash
"lint:fix": "eslint --fix src/**/*.{ts,tsx,js}"
```

## Error Lens

It will show you real-time alerts while you work on your web development project. This will allow you to minimize typing errors.

[Install now](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)

## ES7+ React/Redux/React-Native snippets

Allows you to have shortcuts to create react components easily.

### Shortcut

```bash
rfc
```

### Component

```bash
import React from 'react'

export default function index() {
  return (
    <div>index</div>
  )
}
```

### Shortcut

```bash
rafc
```

### Component

```bash
import React from 'react'

export const index = () => {
  return (
    <div>index</div>
  )
}
```

## Rest client

Allows you to send, cancel and restart HTTP requests from the text editor.

you should [install](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) it

### How to use it?

Create a folder, after that, create a file with the extension `.rest`

#### example

```bash
getUser.rest
```

paste this code to check it

```bash
GET https://api.github.com/users/jsmarenco
```

### Separte yours imports

```bash
// Third-party dependencies

// Current project dependencies
```
### But, Why?

| Benefit         | Description                                                                   |
| --------------- | ----------------------------------------------------------------------------- |
| Clarity         | Provides clear visual separation between third-party and project dependencies |
| Organization    | Helps organize imports in a structured manner                                 |
| Scalability     | Facilitates management of a growing number of dependencies                    |
| Maintainability | Simplifies adding or removing imports without affecting other statements      |
