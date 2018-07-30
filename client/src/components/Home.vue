<template>
  <div class="home">
      {{ msg }}
  </div>
</template>

<script>
import { services } from '@/mixins/services'

export default {
  name: 'Home',
  mixins: [services],
  data () {
    return {
      msg: 'Zizou'
    }
  },
  mounted () {
    console.log('services.data() : ', this.responses())
  }
}
</script>

<style scoped>
</style>
