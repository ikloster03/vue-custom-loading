# Vue Custom Loading

[![Greenkeeper badge](https://badges.greenkeeper.io/ikloster03/vue-custom-loading.svg)](https://greenkeeper.io/)
Custom full overlay loading with spinner for Vue. Select light or dark overlay and insert your spinner.

```
<template>
    <Loading :show="show"></Loading>
</template>
<script>    
    import Loading from 'vue-custom-loading';
    
    export default {
      components: {
        Loading
      },
       data(){
           return {
               show: false,
           }
       }
    }
</script>
<style scoped>

</style>
```

## Install

### NPM

```
npm install vue-custom-loading --save
```

### YARN

```
yarn add vue-custom-loading
```

## Webpack

| Command   | Options                               |
| :----     | :------                               |
| dev       | webpack-dev-server --env development  |
| build     | static build                          |

## Examples

![Alt Text](https://github.com/ikloster03/vue-custom-loading/raw/master/img/example.gif)


[vue-custom-loading example](https://ikloster03.github.io/vue-custom-loading/)

## Settings

| Option    | Type      | Default   | Description                                  |
| :------   | :----     | :-------  | :-----------                                 |
| `show`    | Boolean   | false     | Show or hide loader                          |
| `overlay` | String    | 'light'   | Color of overlay: 'light', 'dark' or 'none'  |

## Custom spinner

Example of custom loader (spinner).

```
<template>
    <Loading 
        :show="show"
        :overlay="overlay"
    >
    <div slot="loader">
        <div class="special-loader-style">Loading ...</div>
    <div>
    </Loading>
</template>
<script>    
    import Loading from 'vue-custom-loading';
    
    export default {
      components: {
        Loading
      },
       data(){
           return {
               show: false,
               overlay: 'dark,
           }
       }
    }
</script>
<style scoped>
    .special-loader-style {
        color: #fff;
    }
</style>
```

You can add your own loader (spinner) in slot 'loader'. 
Although you can add loader's styles in tag style.

## Contact me

- Site: [ikloster03.github.io](https://ikloster03.github.io)
- E-mail: <ikloster@yandex.ru>
- Telegram channel: [t.me/ikloster95](https://t.me/ikloster95)

## [CHANGELOG](https://github.com/ikloster03/vue-custom-loading/blob/master/CHANGELOG.md)


## [LICENSE](https://github.com/ikloster03/vue-custom-loading/blob/master/LICENSE)

Copyright (c) 2017 Monastyrev Ivan <ikloster@yandex.ru>. Licensed under the [MIT license](https://github.com/ikloster03/vue-custom-loading/blob/master/LICENSE). 

