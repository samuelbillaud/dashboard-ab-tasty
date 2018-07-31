<template>
  <div class="container">
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
  .container {
    align-items: center;
    display: flex;
    width: 60%;
    margin: 10px auto;
  }

  .note {
    padding-right: 30px;
    margin-right: 30px;
    align-self: center;
    width: 40%;
  }

  p {
    align-self: center;
  }
</style>
