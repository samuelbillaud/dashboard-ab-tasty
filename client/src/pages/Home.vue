<template>
  <div class="home">
    <header-title :title="applicationTitle"/>

    {{ msg }}
  </div>
</template>

<script>
import { services } from '@/mixins/services'

import HeaderTitle from '@/components/HeaderTitle'

export default {
  name: 'Home',
  mixins: [services],
  data () {
    return {
      msg: 'Zizou'
    }
  },
  components: {
    HeaderTitle
  },
  mounted () {
    console.log('services.data() : ', this.responses())
  },
  computed: {
    applicationTitle () {
      return this.responses().title
    }
  }
}
</script>

<style scoped>
</style>
