<template>
  <div>
    <h2>{{ title }}</h2>
    <slot name="head"></slot>
    <slot>default slot</slot>
    <slot name="foot"></slot>
  </div>
</template>

<script>
  export default {
    beforeDestroy() {
      console.log('beforeDestroy');
    },
    props: {
      title: {
        type: String,
      }
    },
    destroyed() {
      console.log('destroyed');
    },
  }
</script>