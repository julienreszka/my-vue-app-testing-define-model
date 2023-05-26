# Testing defineModel

The purpose of this repository is te demonstrate the power of defineModel

## Project setup

```bash
pnpm install
```

### Compiles and hot-reloads for development

```bash
pnpm dev
```

### What to look at

`vite.config.js`:

```js
export default defineConfig({
  plugins: [
    vue({
      script: {
        defineModel: true,
      },
    }),
  ],
});
```

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).
