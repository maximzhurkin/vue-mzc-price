<script>
export default /*#__PURE__*/ {
  name: "VueMzcPrice", // vue component name
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