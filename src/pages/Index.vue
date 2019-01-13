<template>
  <Layout>
    
    
    <p v-for="{ node } in $page.allPost.edges" :key="node._id">
      <g-link :to="node.path" class="links">
        <h3>{{ node.title }}</h3>
      </g-link>
    </p>

  </Layout>
</template>


<page-query>
query Posts {
  allPost {
    edges {
      node {
        _id
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
