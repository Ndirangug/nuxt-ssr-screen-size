# nuxt-ssr-screen-size-typescript

<!---

Get easy and reactive access to the width and height of your screen.

# nuxt-ssr-screen-size and vue-screen-size

It is well known that the screen dimensions cannot be determined from the CLI or SSR, for that same reason when this script is run from a server environment it will be given default width and height values (1024 x 768), and in the In case of being executed from the client, the corresponding dimensions will be shown with their respective reactivity.

Relax and forget about the message "the window is not defined"

![alt text](https://i.imgur.com/Gi0TFBs.png "nuxt-ssr-screen-size")

### Links

[View demo](https://#)

[View on npm](https://#)

[View on GitHub](https://github.com/promosis/nuxt-ssr-screen-size)

### Install

```bash
# npm
npm i github:Ndirangug/nuxt-ssr-screen-size

```
or
```yarn
# npm
yarn add github:Ndirangug/nuxt-ssr-screen-size

```


### About

Sometimes when building an app you need to have access to the screen's dimensions. Usually that's going to be done in the css using `@media` - but sometimes you need to access that info right in your JavaScript.

The issue with this is you have to worry about adding event listeners and then removing them later. We wanted to just be able to import something quickly and then be able to forget about it later. So this `mixin` does just that - just use `Vue.use()` or `mixins: [],` and you're off.

There is something to consider - where and how you include this library. There are two ways, make sure to be aware of the differences:

### Usage Example 1 - Whole app has access (Not Recommended)

In this usage - your whole app - and every child component - has access to the `$vssWidth`, `$vssHeight`, and `$vssEvent` variables. This is sorta pollutive though, as multiple instances of the mixin are initialized and it's kinda wasteful. The is due to the way Vue mixins are passed down to child components. You can read more about this [here](https://vuejs.org/v2/guide/mixins.html#Global-Mixin). The second example is recommended.

```javascript
import NuxtSSRScreenSize from 'nuxt-ssr-screen-size'
Vue.use(NuxtSSRScreenSize)

// Access `this.$vssWidth`, `this.$vssHeight`, and `this.$vssEvent` anywhere in your app.
```

### Usage Example 2 - Just the component you install it on has access - (Recommended)

In this usage - the component you install it on will have access to the `$vssWidth`, `$vssHeight`, and `$vssEvent` variables. This may be a bit more restrictive, but it's less wasteful and should give you better performance.

```javascript
import NuxtSSRScreenSize from 'nuxt-ssr-screen-size'

export default {
    ...
    mixins: [NuxtSSRScreenSize.NuxtSSRScreenSizeMixin],
    ...
}

// Access `this.$vssWidth`, `this.$vssHeight`, and `this.$vssEvent` in your component.
```
### Variables

| name | type | description |
|--------|------------|-------------|
| $vssWidth | Number | The width of your screen |
| $vssHeight | Number | The height of your screen |
| $vssEvent | Object | The event object data from the resizing event. |

### Methods

| method | parameters | description |
|--------|------------|-------------|
| $vssDestroyListener | none | Force the removal of the attached event listener |

### Development

```bash
# install dependencies
npm install

# serve with hot reload
npm run watch

# run the tests
npm run test

# build demo page
npm run build:example

# build
npm run build

# publish to npm
npm publish
```

### Other

Go ahead and fork the project! Submit an issue if needed. Have fun!

### License

[MIT](http://opensource.org/licenses/MIT)

Packaged with a mixture of [vue-lib-template](https://github.com/biigpongsatorn/vue-lib-template) and [vue-sfc-rollup](https://github.com/team-innovation/vue-sfc-rollup).

-->
