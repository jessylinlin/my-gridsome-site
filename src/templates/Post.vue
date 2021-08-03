<template>
  <layout>
    <div>
      <h1>Post page</h1>
      <h2>{{$page.post.title}}</h2>
      <p>{{$page.post.content}}</p>
    </div>
  </layout>
</template>
<page-query>
query($id: ID!) {
  post(id: $id) {
    id
    title
    content
  }
}
</page-query>
<script>
export default {
  name: 'PostPage',
  metaInfo() {
    return {
      title: this.$page.post.title
    }
  }
}
</script>

<style>

</style>