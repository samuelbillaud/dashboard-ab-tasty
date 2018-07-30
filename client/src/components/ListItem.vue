<template>
  <div>
    <my-note :note="note" class="note"/>
    <p>{{ comment }}</p>
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
  div {
    display: flex;
    align-items: flex-start;
    flex-wrap: wrap;
    margin: 30px;
  }

  .note {
    padding-right: 30px;
    margin-right: 30px;
    align-self: center;
  }

  p {
    align-self: center;
  }
</style>
