<template>
  <div>
      <ul>
        <li
          v-for="(number, index) in (total + 1)"
          :key="index"
          :class="index <= note ? 'full' : ''">
            {{ index }}
          </li>
      </ul>
  </div>
</template>

<script>
import { services } from '@/mixins/services'

export default {
  name: 'Note',
  mixins: [services],
  props: {
    note: {
      type: Number,
      required: true
    }
  },
  computed: {
    total () {
      return this.responses().maxNote
    }
  },
  methods: {
    displayNote () {

    }
  }
}
</script>

<style scoped>
  div {
    border-right: 2px solid #162a3b;
  }

  ul {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  li {
    flex-direction: row;
    width: 25px;
    height: 25px;
    border: 1px solid #ededed;
    border-radius: 50%;
    margin: 3px;
    vertical-align: middle;
    line-height: 25px;
    color: #162a3b;
    list-style-type: none;
  }

  .full {
    background: #162a3b;
    color: #fff;
  }
</style>
