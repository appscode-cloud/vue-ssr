<script>
import Vue from 'vue';
import VueSsr from '@/vue-ssr.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueSsr
  }
});
</script>

<template>
  <div id="app">
    <vue-ssr />
  </div>
</template>
