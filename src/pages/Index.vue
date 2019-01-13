<template>
  <Layout>
    
    
    <p v-for="post in $page.posts.edges">
      <g-link :to="post.node.path" class="links">
        <h3>{{ post.node.title }}</h3>
      </g-link>
    </p>

  </Layout>
</template>


<page-query>
query Posts {
  posts: allPost {
    edges {
      node {
        title
        path
      }
    }
  }
}
</page-query>
<script>
export default {
 // ..
}
</script>

<style>
.links {
 text-decoration: none;
 
}
</style>
