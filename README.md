# real-world-vue

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### json-server

```
npm i -g json-server

json-server --watch db.json
```

### Mutation and action

In a component method, a mutation can be commited but it's better to dispatch an action that will commit a mutation.

### Vuex modules

#### Option 1

`/store/index.js`

```js
import * as name from '@/store/modules/name.js'
```

`/store/modules/name.js`

```js
export const state = { ... }
export const mutations = { ... }
export const actions = { ... }
export const getters = { ... }
```

#### Option 2


`/store/index.js`

```js
import name from '@/store/modules/name.js'
```

`/store/modules/name.js`

```js
export default {
  state: { ... },
  mutations: { ... },
  actions: { ... },
  getters: { ... }
}
```

#### mutations

Mutations should not be called from other Vuex Modules.
Mutations should only be called from Actions inside the current Module.
