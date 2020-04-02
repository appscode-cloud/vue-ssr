<script>
import Vue from "vue";
import Ssr from "@/vue-ssr.vue";

export default Vue.extend({
  name: "ServeDev",
  components: {
    Ssr,
  },
});
</script>

<template>
  <div id="app">
    <ssr eid="vue-ssr-demo">
      <h1 id="vue-ssr-demo">
        Hi, use me to preserve your server side rendered html :)
      </h1>
    </ssr>
  </div>
</template>
