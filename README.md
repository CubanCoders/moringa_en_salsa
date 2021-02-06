# moringa_en_salsa

## Configuring .babelrc, .eslint.json and .prettifierrc

Just create those three files and add the following base code to each:

- .babelrc:
```
    {
        "presets": ["@babel/preset-env"],
        "plugins": ["@babel/transform-runtime"]
    }
```
- .eslint.json:
```
    {
        "env": {
            "browser": true,
            "es6": true,
            "node": true,
            "mocha": true
        },
        "extends": ["airbnb-base"],
        "globals": {
            "Atomics": "readonly",
            "SharedArrayBuffer": "readonly"
        },
        "parserOptions": {
            "ecmaVersion": 2020,
            "sourceType": "module"
        },
        "rules": {
            "indent": ["warn", 2],
            "linebreak-style": ["error", "unix"],
            "quotes": ["error", "single"],
            "semi": ["error", "always"],
            "no-console": 1,
            "comma-dangle": [0],
            "arrow-parens": [0],
            "object-curly-spacing": ["warn", "always"],
            "array-bracket-spacing": ["warn", "always"],
            "import/prefer-default-export": [0]
        }
    }
```
- .prettifierrc:
```
    {
        "trailingComma": "es5",
        "tabWidth": 4,
        "semi": true,
        "singleQuote": true
    }
```