<template>
  <div class="section">
    <p class="is-size-5 has-text-justified">
      Hey there! I am a 3rd year CS undergrad with big dreams.
      I like working with Open Source Technologies. Currently,
      am contributing to the Linux Kernel as a part of the LKMP
      program. And there are some amazing people who
      are keeping the community running.<br><br>

      Personally, I have worked with backend technologies more.
      My frontend exposure has been pretty much limited to Vue.js
      and Nuxt.js. I earlier worked on react but I have nearly forgot it.
      On the backend, I have quite a bit of experience working with Node.
      But nowadays I am more into Golang, because why won't anyone? It's
      a spectacular language to work with.<br><br>

      Apart from this I have written programs in C++ Qt framework.
      And yeah I know some hacky linux commands to make tasks easier.
      I have also worked with container technologies. I have a strong
      thing for Docker. It has pretty much made life easier for all of us.
      So that's it for me.
    </p>
  </div>
</template>

<script>
export default {
  props: {
    sites: {
      type: Array,
      default: null
    }
  }
}
</script>

<style scoped>
.pb-5{
    padding-bottom: 5px;
}
</style>
