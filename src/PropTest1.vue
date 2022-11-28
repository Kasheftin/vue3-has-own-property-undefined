<template>
  <pre>
    Object.prototype.hasOwnProperty.call(this, 'prop1') = {{ prop1Exists }}
    this.prop1 = {{ prop1 }}
  </pre>
</template>

<script>
export default {
  props: {
    prop1: {
      type: Number,
      default: 0
    }
  },
  computed: {
    prop1Exists() {
      return Object.prototype.hasOwnProperty.call(this, 'prop1')
    }
  }
}
</script>
