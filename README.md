# vue-mzc-price
Simple Vue2 price component

![](demo.png)

[Online demo](https://codesandbox.io/s/serene-joliot-728ku?file=/src/App.vue)

## Installation
```sh
npm install vue-mzc-price --save
```

## Usage
```js
import VueMzcPrice from "vue-mzc-price";
import "vue-mzc-price/src/vue-mzc-price.css";

export default {
  components: {
    VueMzcPrice,
  },
};
```
```html
<vue-mzc-price :cost="1024" />
<vue-mzc-price :cost="2048" olden />
```
## Customize
```css
.vue-mzc-price {
  --vue-mzc-price-font-size: 1.125em;
  --vue-mzc-price-font-weight: 700;
  --vue-mzc-price-line-height: 1.5em;
  --vue-mzc-price-color: #222222;
  --vue-mzc-price-olden-font-size: 0.875em;
  --vue-mzc-price-olden-font-weight: 400;
  --vue-mzc-price-olden-line-height: 1em;
  --vue-mzc-price-olden-color: #999999;
  --vue-mzc-price-olden-line-height: 1px;
  --vue-mzc-price-olden-line-color: #ff0000;
  --vue-mzc-price-currency-gap: 5px;
}
```