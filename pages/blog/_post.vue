<template>
  <div class="container">
    <div class="columns is-centered">
      <div class="column is-10-tablet">
        <div class="title">{{ attributes.title}}</div>
        <div v-html="content" class="content"></div>
      </div>
    </div>
  </div>
</template>

<script>
const fm = require("front-matter");
var md = require("markdown-it")({
  html: true,
  typographer: true
});

export default {
  async asyncData({ params }) {
    try {
      console.info(params.post);
      const fileContent = await import(`~/blog/${params.post}.md`);

      let res = fm(fileContent.default);
      console.log(res.attributes)
      return {
        attributes: res.attributes,
        content: md.render(res.body)
      };
    } catch (error) {
      console.log(error);
      return false;
    }
  },
  data(){
      return{
          attributes: {
              title: null,
          },
          content: null
      }
  }
}
</script>
