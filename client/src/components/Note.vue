<template>
  <div>
      <ul>
        <li
          v-for="(number, index) in total"
          :key="index"
          :class="index <= note ? 'full' : ''">
            {{ index }}
          </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'Note',
  data () {
    return {
      total: 11
    }
  },
  props: {
    note: {
      type: Number,
      required: true
    }
  },
  methods: {
    displayNote () {

    }
  }
}
</script>

<style scoped>
  li {
    display: inline-block;
    width: 25px;
    height: 25px;
    border: 1px solid #ededed;
    border-radius: 50%;
    margin: 3px;
    vertical-align: middle;
    line-height: 25px;
    color: #162a3b;
  }

  .full {
    background: #162a3b;
    color: #fff;
  }
</style>
