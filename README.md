 <h1>Nuxt 3 - lodash</h1>
 
<p>
  <a href="https://www.npmjs.com/package/nuxt-lodash"><img src="https://badgen.net/npm/v/nuxt-lodash" alt="Version"></a>
  <a href="https://www.npmjs.com/package/nuxt-lodash"><img src="https://badgen.net/npm/license/nuxt-lodash" alt="License"></a>
  <a href="https://www.npmjs.com/package/nuxt-lodash"><img src="https://badgen.net/npm/types/nuxt-lodash" alt="Types"></a>
</p>
   
## 💡 About

<h4><a href="https://lodash.com/">Lodash</a> auto-import module for <a href="https://nuxtjs.org/">Nuxt3</a>, supports custom prefix, list of exludes and list of aliases<h4>
   
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
          ["camelCase", "stringToCamelCase"], // will result it useStringToCamelCase
          ["kebabCase", "stringToKebabCase"], // will result it useStringToKebabCase
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

[MIT License](https://github.com/cipami/nuxt-lodash/blob/master/LICENSE) © 2021-PRESENT [Michal Čípa](https://github.com/cipami)
