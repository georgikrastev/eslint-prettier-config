# General

VSCode configuration of ESLint and Prettier to work with React

## Dev Dependencies

Install the following packages as dev dependency:
* eslint
* eslint-config-prettier
* eslint-plugin-prettier
* eslint-plugin-react
* prettier

## Prettier Config

An empty file called `.prettierrc` should be created at the root of the project. This file contains a configuration object.

Add the following to it:

```
{
	"semi": false,
	"singleQuote": true,
	"tabWidth": 4,
	"useTabs": true,
	"arrowParens": "avoid" 
}
```

For more information about config options search the web.


## ESLint Config

In the root of the project run `eslint --init` and follow the instructions:

**How would you like to use ESLint?**
To check syntax and find problems

**What types of modules does your project use?**
JavaScript modules (import/export)

**Which framework does your project use?**
React

**Does your project use TypeScript?**
No

**Where does your code run?**
Browser

**What format do you want your config file to be in?**
JSON

**Would you like to install them now with npm?**
Yes


After completing the process a `.eslintrc.json` is created. This file contains a configuration object.

Update it so it looks like this:

```
{
    "env": {
        "browser": true,
        "es6": true
    },
    "extends": [
        "eslint:recommended",
        "plugin:prettier/recommended",
        "plugin:react/recommended"
    ],
    "globals": {
        "Atomics": "readonly",
        "SharedArrayBuffer": "readonly"
    },
    "parserOptions": {
        "ecmaFeatures": {
            "jsx": true
        },
        "ecmaVersion": 2018,
        "sourceType": "module"
    },
    "plugins": [
        "react",
        "prettier"
    ],
    "rules": {
        "prettier/prettier": "error"
    }
}
```
