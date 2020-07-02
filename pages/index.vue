<template>
  <div v-if="state===0" class="section has-background-light">
    <Intro1 :increment="increment" />
  </div>
  <div v-else-if="state===1" class="section has-background-light">
    <Landing />
  </div>
</template>

<script>
import Landing from '../components/Landing'
import Intro1 from '../components/Intro1'

export default {
  name: 'HomePage',

  components: {
    Landing,
    Intro1
  },
  layout: 'nonav',
  data () {
    return {
      state: 0
    }
  },
  methods: {
    increment () {
      this.state = this.state + 1
    }
  }
}
</script>
