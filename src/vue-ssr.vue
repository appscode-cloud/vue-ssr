<template>
  <transition name="appscode-vue-ssr-wrapper" v-bind="$attrs" v-on="$listeners">
    <slot></slot>
  </transition>
</template>

<script>
export default {
  name: "Ssr", // vue component name
  props: {
    eid: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      innerHTML: "",
    };
  },
  beforeMount() {
    const elem = document.getElementById(this.eid);
    this.innerHTML = elem && elem.innerHTML;
  },
  mounted() {
    const elem = document.getElementById(this.eid);
    if (elem && this.innerHTML) elem.innerHTML = this.innerHTML;
  },
};
</script>
