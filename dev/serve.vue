<script>
import Vue from 'vue';
import VueMzcPrice from '@/vue-mzc-price.vue';
import './serve.css';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueMzcPrice
  }
});
</script>

<template>
  <div id="app">
    <div class="row">
      <div class="item">
        <vue-mzc-price :cost="1024" />
      </div>
      <div class="item">
        <vue-mzc-price :cost="2048" olden />
      </div>
    </div>
    <div class="row">
      <div class="item">
        <vue-mzc-price :cost="134680" />
      </div>
      <div class="item">
        <vue-mzc-price :cost="149500" olden />
      </div>
    </div>
  </div>
</template>
