<template>
  <div>
    <div id="comments" v-for="(comment, index) in comments" :key="index">
      <div class="card mb-3">
      <div class="card-body">
      <a href="#" class="btn btn-link ml-0 float-right" v-on:click.prevent="deleteComment(index)">Excluir</a>
      <h5 class="card-title">Author: {{comment.name}}</h5>
      <p class="card-text">Comment: {{formatComment(comment.comment)}}</p>
      </div>
      </div>
    </div>
  </div>
</template>

<script>  
  export default {
    props: {
      comments: Array,
    },
    methods: {
      formatComment(value) {
        if (value.trim() === '') {
          return 'N/A'
        }
      },
      deleteComment(index) {
        this.$emit('delete-comment', {
          index: index
        })
      }
    }
  }
</script>