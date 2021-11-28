 <h1>Nuxt 3 - lodash</h1>
 
<p>
  <a href="https://www.npmjs.com/package/nuxt-lodash"><img src="https://badgen.net/npm/v/nuxt-lodash" alt="Version"></a>
  <a href="https://www.npmjs.com/package/nuxt-lodash"><img src="https://badgen.net/npm/license/nuxt-lodash" alt="License"></a>
  <a href="https://www.npmjs.com/package/nuxt-lodash"><img src="https://badgen.net/npm/types/nuxt-lodash" alt="Types"></a>
</p>
   
## 💡 About

[Lodash](https://lodash.com) auto-import module for [Nuxt3](https://nuxtjs.org).

## 📦 Install

```bash
npm i nuxt-lodash -D
```

## 💻 Usage

```js
import { defineNuxtConfig } from "nuxt3";

export default defineNuxtConfig({
  buildModules: [
    [
      "nuxt-lodash",
      {
        prefix: "use",
        exclude: ["map"],
        alias: [
          ["camelCase", "stringToCamelCase"], // will result in useStringToCamelCase
          ["kebabCase", "stringToKebabCase"], // will result in useStringToKebabCase
        ],
      },
    ],
  ],
});
```

## 🔨 Config

| Name      | Default | Description                                               |
| --------- | ------- | --------------------------------------------------------- |
| `prefix`  | `false` | string to prepend before each function (false to disable) |
| `exclude` | `[]`    | list of functions to exlude from auto-imports             |
| `alias`   | `[]`    | list of aliases to rename specific functions              |

## 💻 Example

```html
<template>
  <div>{{ text }}</div>
</template>
<script setup lang="ts">
  const text = useToUpper("it works!");
</script>
```

## 📄 License

[MIT License](https://github.com/cipami/nuxt-lodash/blob/master/LICENSE) © 2021 [Michal Čípa](https://github.com/cipami)
