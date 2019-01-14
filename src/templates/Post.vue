<template>
  <Layout>
  <div>
    <div v-html="$page.post.date"/>
    <div v-html="$page.post.content"/> 
  </div>
  </Layout>
</template>

<page-query>
query Post ($path: String!) {
  post (path: $path) {
    title
    content
    date (format: "D MMMM, YYYY")
  }
}
</page-query>

<script>
export default {
  metaInfo() {
    return {
      title: this.$page.post.title
    };
  }
};
</script>