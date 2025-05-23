# Prettier Configuration File

This repository contains my custom Prettier configuration file. The purpose of this repository is to make it easy to clone and apply the same Prettier settings across different projects.

## Usage

- To use this configuration file, simply copy the `.prettierrc` file to the root of your project directory. You can do this manually or by running the following command:

```bash
curl -o .prettierrc https://raw.githubusercontent.com/emanuelefavero/prettier/main/.prettierrc
```

- Install Prettier and Prettier plugins in the root of your project directory:

```bash
npm i -D prettier prettier-plugin-organize-imports prettier-plugin-tailwindcss
```

- Adjust `./src/app/globals.css` to your CSS file where you import TailwindCSS: `@import 'tailwindcss'`;

> Note: You can use the `Prettier - Code formatter` extension in Visual Studio Code to format your code using Prettier
>
> Note; If you don't want to use the plugins, you can remove them from the `.prettierrc` file `”plugins”, “organizeImportsSkipDestructiveCodeActions”, “tailwindConfig”`

## .prettierrc

```json
{
  "semi": false,
  "singleQuote": true,
  "jsxSingleQuote": true,

  "tabWidth": 2,
  "bracketSpacing": true,
  "printWidth": 80,
  "useTabs": false,
  "arrowParens": "always",
  "htmlWhitespaceSensitivity": "css",
  "trailingComma": "all",

  "plugins": [
    "prettier-plugin-organize-imports",
    "prettier-plugin-tailwindcss"
  ],
  "organizeImportsSkipDestructiveCodeActions": true,
  "tailwindStylesheet": "./src/app/globals.css"
}
```

As you can see the settings are divided in 3 (*separated by spaces since json doesn’t allow comments*):

- Prettier settings that have values different from prettier defaults
- Default settings that I like to have available for quick changes
- Plugins and plugin related settings

## Plugins

- [prettier-plugin-organize-imports](https://www.npmjs.com/package/prettier-plugin-organize-imports) - This is a plugin that allows you to auto organise the code imports on save. Add "organizeImportsSkipDestructiveCodeActions": true, if you want to prevent the plugin from removing unused imports
- [prettier-plugin-tailwindcss](https://www.npmjs.com/package/prettier-plugin-tailwindcss/v/0.0.0-insiders.d539a72) - This plugin automatically sorts the tailwind classes in your code. It needs to have this prettier setting: "tailwindConfig": "./tailwind.config.ts"

> Note: Adjust the `tailwindStylesheet` setting to your CSS file where you import TailwindCSS: `@import 'tailwindcss'`;

## License

### MIT License

Copyright (c) 2024 Emanuele Favero

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Author

- [Emanuele Favero](https://emanuelefavero.com)
