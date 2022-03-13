# @jbeche/vite-vue2-i18n-loader

## Installation

npm:

```sh
npm i --save-dev @jbeche/vite-vue2-i18n-loader
```

## Usages

```js
import { createI18nPlugin } from '@jbeche/vite-vue2-i18n-loader';

export default defineConfig({
  plugins: [createVuePlugin(), createI18nPlugin()],
});
```

Then, we can write the i18n blocks in the vue component file:

```vue
<template>
  <p>{{ $t('hello') }}</p>
</template>

<i18n>
{
  "en": {
    "hello": "Hello World!"
  },
  "zh": {
    "hello": "你好，世界！"
  }
}
</i18n>
``` 

We can also use import for json files 
```vue
<i18n src="./exemple.json"></i18n>
```
