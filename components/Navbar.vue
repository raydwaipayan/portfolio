<template>
  <b-navbar class="px-5" type="is-light" fixed-top>
    <template slot="start">
      <b-navbar-item href="https://github.com/raydwaipayan">
        <b-icon pack="fab" icon="github" size="is-large" />
      </b-navbar-item>
      <b-navbar-item href="https://twitter.com/RayDwaipayan">
        <b-icon pack="fab" icon="twitter" size="is-large" />
      </b-navbar-item>
      <b-navbar-item href="https://www.linkedin.com/in/dwaipayan-ray-a2a655177/">
        <b-icon pack="fab" icon="linkedin" size="is-large" />
      </b-navbar-item>
    </template>
    <template slot="end">
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        About
      </b-navbar-item>
      <b-navbar-item href="#">
        Resume
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ path: '/blog' }">
        Blog
      </b-navbar-item>
    </template>
  </b-navbar>
</template>

<style>
.px-5{
    padding-left: 5vw;
    padding-right: 5vw;
}
</style>
