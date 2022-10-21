# vite-plugins

A collection of useful Vite plugins.

```sh
npm install --save-dev vite-plugins
```

```ts
import { defineConfig } from 'vite'
import { externalizeDeps, nodePolyfills } from 'vite-plugins'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [
    externalizeDeps({
      nodeBuiltins: false,
    }),
    nodePolyfills({
      protocolImports: true,
    }),
  ],
})
```

## Included plugins

- [vite-plugin-externalize-deps](https://github.com/voracious/vite-plugin-externalize-deps) A configurable Vite plugin to help externalize your dependencies (including subpaths)
- [vite-plugin-node-polyfills](https://github.com/voracious/vite-plugin-node-polyfills) A Vite plugin to polyfill Node's Core Modules for browser environments.
