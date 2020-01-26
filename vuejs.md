# Vue.js Convention
## [Repository](https://github.com/WhatCodeProject/Vue)
## 프로젝트 구조

-   assets
    -   컴파일되지 않는 정적 파일
-   components
    -   header
    -   footer
    -   dialog
-   views
    -   login.vue
    -   register.vue
-   plugins
    -   vuetify.js
-   routes
    -   route.js
-   store(Vuex 관리)
    -   state.js
    -   getter.js
    -   mutations.js
    -   actions.js
-   apis
    -   api.js
-   static
    -   .css
-   utils
    -   bus.js
-   App.vue
-   main.js

## 코딩 컨벤션

#### Component name

-   export default를 통해 vue 인스턴스를 생성한다.

```js
export default {
  name: 'TodoItem',
  // ...
}
```

#### Component data

-   data()는 아래와 같이 사용한다.

```js
export default {
  data () {
    return {
      foo: 'bar'
    }
  }
}
```

#### Component props

-   props를 타입을 명시한다.

```js
props: {
  status: String
}
```

#### for문에서 key값을 사용하기

```js
<ul>
  <li
    v-for="todo in todos"
    :key="todo.id"
  >
    {{ todo.text }}
  </li>
</ul>
```

#### 한 tag에서 for, if를 같이 사용하면 안 된다.

```js
<ul v-if="shouldShowUsers">
  <li
    v-for="user in users"
    :key="user.id"
  >
    {{ user.name }}
  </li>
</ul>
style은 scoped를 사용한다.
<style scoped>
</style>
```

#### 메서드는 카멜 케이스를 사용한다.

```js
methods: {
    publicMethod() {
    }
  }
```

#### 컴포넌트는 파스칼 케이스로 생성한다.

-   prefix를 붙인다. Group이 있다면 Group에 맞게 없다면 The로 표기한다.
-   TheSlidbar.vue
-   BaseButton.vue
-   BaseTable.vue

#### 이하 Style Guide는 Vue.js 공식 Style Guide를 따른다.

-   [참고](https://vuejs.org/v2/style-guide/#Private-property-names-essential)
