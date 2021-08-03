<template>
  <layout>
    <div>
      <h1>Posts2</h1>
      <ul>
        <li v-for="edge in $page.posts.edges" :key="edge.id">
          <g-link :to="edge.node.path">{{edge.node.title}}</g-link>          
        </li>
      </ul>
    </div>
  </layout>
</template>
<!--garphQl中查询数据-->
<page-query>
query {
  posts: allPost {
    edges{
      node {
        id
        title
        path
      }
    }
  }
}
</page-query>
<script>
import axios from 'axios'
export default {
  name: 'Posts2',
  
}
</script>

<style>

</style>