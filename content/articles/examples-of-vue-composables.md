---
title: Examples of vue composables
description: TODO
tags: Vue, Composition api
---
## Countdown timer
```js
import { ref } from '@vue/composition-api'
export default function() {
  const running = ref(false)
  ...
}
```

## Authorization composable
```js
import { ref } from '@vue/composition-api
const token = ref('')

export default function() {
  const setToken = (tokenValue) => 
    token.value = tokenValue
  return {
    setToken,
    token
  }
}
```

