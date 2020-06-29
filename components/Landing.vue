<template>
  <div class="hero is-light is-fullscreen">
    <div class="container py-av">
      <div class="columns is-fullwidth">
        <div class="column is-full">
          <div class="container">
            <div class="avatar">
              <img src="/images/dwaip.jpg">
            </div>
          </div>
          <div class="my-5 container has-text-centered">
            <h1 class="is-size-3 has-text-weight-semibold">
              Heyloo! This is Dwaipayan.
            </h1>
            <p class="is-size-5">
              Developer | Security Enthusiast
            </p>
            <p class="is-size-5 has-text-grey">
              pgp: <a href="http://keyserver.ubuntu.com/pks/lookup?op=get&search=0x01bdc75808d68e0f">public key</a>
            </p>
            <div class="container">
              <p class="is-size-4 has-text-grey-dark py-more">
                Learn more about me!
              </p>
              <div class="arrow-down" @click.prevent="">
                <b-icon pack="fas" icon="arrow-down" size="is-large" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  </div>
</template>

<style scoped>
.arrow-down{
  cursor: pointer;
}
.is-fullscreen{
  min-height: calc(100vh - 6rem);
}
.py-av{
  padding-top: 24vh;
}
.py-more{
  padding-top: 16vh;
}
@media only screen and (max-width:770px){
  .py-av{
    padding-top: 20vh;
  }
  .py-more{
    padding-top: 10vh;
  }
}
.my-5{
  margin-top: 10vh;
}
.avatar{
    width: 14rem;
    height: 100%;
    position: relative;
    margin: 0 auto;
}
img {
    display: block;
    border-radius: 50%;
    position: absolute;
    bottom: -43px;
    border: 4px solid white;
}
</style>
