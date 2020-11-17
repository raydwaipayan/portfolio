<template>
  <b-navbar class="px-5" type="is-light" fixed-top>
    <template slot="start">
      <div class="horizontal">
        <b-navbar-item href="https://github.com/raydwaipayan">
          <b-icon pack="fab" icon="github" size="is-large" />
        </b-navbar-item>
        <b-navbar-item href="https://twitter.com/RayDwaipayan">
          <b-icon pack="fab" icon="twitter" size="is-large" />
        </b-navbar-item>
        <b-navbar-item href="https://www.linkedin.com/in/dwaipayan-ray-a2a655177/">
          <b-icon pack="fab" icon="linkedin" size="is-large" />
        </b-navbar-item>
      </div>
    </template>
    <template slot="end">
      <b-navbar-item>
        <div
          @click.prevent="scrollToEle('#top')"
        >
          Home
        </div>
      </b-navbar-item>
      <b-navbar-item>
        <div
          @click.prevent="scrollToEle('#about')"
        >
          About
        </div>
      </b-navbar-item>
      <b-navbar-item :href="require('../assets/dwaipayan_cv.pdf')">
        Resume
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ path: '/blog' }">
        Blog
      </b-navbar-item>
    </template>
  </b-navbar>
</template>

<script>
export default {
  data () {
    return {
      options: {
        easing: 'linear',
        offset: -60,
        force: true
      }
    }
  },
  methods: {
    scrollToEle (ele) {
      if (this.$nuxt.$route.path !== '/') {
        this.$router.push({ path: `/${ele}` })
        return
      }
      this.$nextTick(() => {
        this.$scrollTo(ele, 400, this.options)
      })
    }
  }
}
</script>
<style>
.px-5{
  padding-left: 5vw;
  padding-right: 5vw;
}
.horizontal{
  display: flex;
  flex-direction: row;
}
</style>
