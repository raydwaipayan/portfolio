<template>
  <div class="hero is-light is-fullheight">
    <div class="columns has-text-centered is-desktop is-vcentered">
      <div class="column">
        <vue-typed-js
          :start-delay="1000"
          :back-speed="20"
          :strings="['Henlo Stranger', 'I can convert coffee to code', 'Welcome to my site!']"
          :type-speed="60"
          @onComplete="showBtn++"
        >
          <h1 class="typing is-size-2 has-text-weight-medium" />
        </vue-typed-js>
        <transition name="fade">
          <b-button
            v-if="showBtn"
            type="is-light"
            class="is-size-5"
            inverted
            outlined
            @click.prevent="changeState"
          >
            Enter
          </b-button>
        </transition>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    changeState: {
      type: Function,
      default: () => {}
    }
  },
  data () {
    return {
      showBtn: 0
    }
  }
}
</script>

<style scoped>
.columns {
  display: flex;
  height: calc(100vh - 5rem);
  align-self: center;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
