<script>
export default /*#__PURE__*/ {
  name: "VueMzcPrice",
  props: {
    cost: {
      type: Number,
      default: 0,
      required: true,
    },
    currency: {
      type: String,
      default: "₽",
    },
    olden: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    price() {
      return this.cost
        ? this.cost.toString().replace(/\B(?=(\d{3})+(?!\d))/g, " ")
        : "0";
    },
  },
};
</script>

<template>
  <span class="vue-mzc-price" :class="olden ? `vue-mzc-price--olden` : ''">
    <span class="vue-mzc-price__cost">{{ price }}</span>
    <span class="vue-mzc-price__currency">{{ currency }}</span>
  </span>
</template>

<style>
:root {
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
.vue-mzc-price {
  display: inline-block;
  font-family: inherit;
  font-size: 1.125em;
  font-size: var(--vue-mzc-price-font-size);
  font-weight: 700;
  font-weight: var(--vue-mzc-price-font-weight);
  line-height: 1.5em;
  line-height: var(--vue-mzc-price-line-height);
  white-space: nowrap;
  color: #222222;
  color: var(--vue-mzc-price-color);
}
.vue-mzc-price--olden {
  position: relative;
  font-size: 0.875em;
  font-size: var(--vue-mzc-price-olden-font-size);
  font-weight: 400;
  font-weight: var(--vue-mzc-price-olden-font-weight);
  line-height: 1em;
  line-height: var(--vue-mzc-price-olden-line-height);
  color: #999999;
  color: var(--vue-mzc-price-olden-color);
}
.vue-mzc-price--olden:after {
  content: "";
  display: block;
  position: absolute;
  left: 0;
  top: 45%;
  width: 100%;
  height: 1px;
  height: var(--vue-mzc-price-olden-line-height);
  background-color: #ff0000;
  background-color: var(--vue-mzc-price-olden-line-color);
  transform: rotate(-9deg);
}
.vue-mzc-price__currency {
  padding-left: 5px;
  padding-left: var(--vue-mzc-price-currency-gap);
}
</style>