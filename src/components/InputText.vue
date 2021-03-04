<template>
  <input type="text" v-model="computedValue">
  <!--省略前はこの形と同義-- <input-text
    :value="form.name"
    @input="form.name = $event.target.value"
  >
  </input-text> -->
</template>

<script>
export default {
  props: {
    value: String,
  },
  computed: {
    computedValue: {
      get() {
        return this.value;
      },
      set(value) {
        this.$emit('input', value);
      }
    }
  }
}
</script>