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

- Adjust `./tailwind.config.ts` to your Tailwind config file extension (e.g. `.js`)

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
  "tailwindConfig": "./tailwind.config.ts"
}
```

As you can see the settings are divided in 3 (*separated by spaces since json doesn’t allow comments*):

- Prettier settings that have values different from prettier defaults
- Default settings that I like to have available for quick changes
- Plugins and plugin related settings

## Plugins

- [prettier-plugin-organize-imports](https://www.npmjs.com/package/prettier-plugin-organize-imports) - This is a plugin that allows you to auto organise the code imports on save. Add "organizeImportsSkipDestructiveCodeActions": true, if you want to prevent the plugin from removing unused imports
- [prettier-plugin-tailwindcss](https://www.npmjs.com/package/prettier-plugin-tailwindcss/v/0.0.0-insiders.d539a72) - This plugin automatically sorts the tailwind classes in your code. It needs to have this prettier setting: "tailwindConfig": "./tailwind.config.ts"

> Note: Adjust the `tailwindConfig` setting to your Tailwind config file extension (e.g. `.js`)
