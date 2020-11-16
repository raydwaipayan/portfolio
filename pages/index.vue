<template>
  <div v-if="!state">
    <Intro1 :change-state="changeState" />
  </div>
  <div v-else>
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
  mounted () {
    const visit = this.$cookies.get('visited')

    if (visit) {
      this.state = visit === '0' ? 0 : 1
    }
    this.$cookies.set('visited', '1', {
      path: '/',
      maxAge: 60 * 60 * 5
    })
  },
  methods: {
    changeState () {
      this.state = !this.state
    }
  }
}
</script>
