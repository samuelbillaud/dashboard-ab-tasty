<template>
  <div class="home">
    <header-title :title="applicationTitle"/>

    <ul>
      <li
        is="ListItem"
        v-for="(response, index) in allResponses"
        :key="index"
        :comment="response.comment"
        :note="response.note">
      </li>
    </ul>

    {{ msg }}
  </div>
</template>

<script>
import { services } from '@/mixins/services'

import HeaderTitle from '@/components/HeaderTitle'
import ListItem from '@/components/ListItem'

export default {
  name: 'Home',
  mixins: [services],
  data () {
    return {
      msg: 'Zizou'
    }
  },
  components: {
    HeaderTitle,
    ListItem
  },
  mounted () {
    console.log('services.data() : ', this.responses())
  },
  computed: {
    applicationTitle () {
      return this.responses().title
    },
    allResponses () {
      return this.responses().responses
    }
  }
}
</script>

<style scoped>
</style>
