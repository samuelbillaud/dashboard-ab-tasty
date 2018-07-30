<template>
  <div>
    <p>{{ comment }}</p>
    <p>{{ note }}</p>
  </div>
</template>

<script>
export default {
  name: 'ListItem',
  props: {
    comment: {
      type: String,
      required: true
    },
    note: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>

</style>
