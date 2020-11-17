<template>
  <div>
    <Navbar />
    <div id="top" class="hero is-light is-fullscreen">
      <div class="container">
        <div class="columns is-fullwidth">
          <div class="column is-full my-5">
            <div class="container">
              <div class="avatar">
                <img src="~/assets/dwaip.jpg">
              </div>
            </div>
            <div class="my-5 container has-text-centered">
              <h1 class="is-size-3 has-text-weight-semibold">
                Hey! This is Dwaipayan.
              </h1>
              <p class="is-size-5">
                Developer | Linux Enthusiast
              </p>
              <p class="is-size-5 has-text-grey">
                pgp: <a href="http://keyserver.ubuntu.com/pks/lookup?op=get&search=0x01bdc75808d68e0f">public key</a>
              </p>
              <div class="container">
                <p class="is-size-4 has-text-grey-dark py-more">
                  Learn more about me!
                </p>
                <div
                  v-scroll-to="{
                    el: '#about',
                    duration: 400,
                    easing: 'linear',
                    offset: -50,
                    force: true
                  }"
                  class="arrow-down"
                >
                  <b-icon pack="fas" icon="arrow-down" size="is-large" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="hero is-light is-fullscreen is-fullheight">
      <div id="about" class="container pu-5">
        <h1 class="is-size-3 has-text-weight-semibold has-text-centered">
          About me
        </h1>
        <div class="columns is-centered">
          <div class="column is-10-desktop">
            <About />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from './Navbar'
import About from './About'
export default {
  components: {
    Navbar,
    About
  }
}
</script>
<style scoped>
.arrow-down{
  cursor: pointer;
}

.is-fullscreen{
  min-height: calc(100vh - 5.5rem);
}

.py-more{
  padding-top: 16vh;
}

.pu-5{
  padding-top: 5vh;
}

.my-5{
  margin-top: 5vh;
}

.avatar{
    max-width: 15rem;
    height: auto;
    margin: 0 auto;
}

img {
    border-radius: 50%;
    border: 4px solid white;
}

.round{
    border-radius: 1%;
    border: 1rem solid white;
}

</style>
