<template>
  <div id="app" class="container p-3">
    <FormComment />
    <div class="dropdown-divider"></div>
    <Comments msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Comments from './components/Comments.vue'
import FormComment from './components/FormComment.vue'

export default {
  name: 'App',
  components: {
    Comments,
    FormComment
  }
}
</script>

<style>

</style>
