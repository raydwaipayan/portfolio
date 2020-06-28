<template>
  <div class="container">
    <h1 class="is-size-3">
      Henlo random user! Welcome to Dwai Writes.
    </h1>
    <div v-for="post in posts" :key="post.name">
      <nuxt-link :to="getPermalink(post.name)">
        {{ post.name }}
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ params }) {
    const resolve = await require.context('~/blog/', true, /\.md$/)
    const imports = resolve.keys().map((key) => {
      const [, name] = key.match(/\/(.+)\.md$/)
      return {
        name
      }
    })
    return {
      posts: imports
    }
  },
  data () {
    return {
      prefix: 'blog'
    }
  },
  methods: {
    getPermalink (post) {
      return `${this.prefix}/${post}`
    }
  }
}
</script>
