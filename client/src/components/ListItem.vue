<template>
  <div>
    <p>{{ comment }}</p>
    <my-note :note="note"/>
  </div>
</template>

<script>
import MyNote from '@/components/Note'

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
  },
  components: {
    MyNote
  }
}
</script>

<style scoped>

</style>
