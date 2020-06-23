<template>
  <div>
    <!-- Form-->
    <FormComment v-on:add-comment="addComment"/>
    
    <!-- Divider -->
    <div class="dropdown-divider"></div>

    <!-- List -->
    <div class="container">
      <h1>Comments</h1>

      <!-- Empty Message -->
      <p v-if="this.comments.length === 0">No comment for now...</p>

      <!-- Cards -->
      <div v-else id="comments" v-for="(comment, index) in comments" :key="index">
        <div class="card mb-3">
          <div class="card-body">
            <a href="#" class="btn btn-link ml-0 float-right" v-on:click.prevent="deleteComment(index)">Excluir</a>
            <h5 class="card-title">Author: {{comment.name}}</h5>
            <p class="card-text">Comment: {{comment.comment}}</p>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
  import FormComment from './FormComment.vue'
  
  export default {
    components: {
      FormComment
    },
    data() {
      return {
        comments: []
      }
    },
    methods: {
      deleteComment(index) {
        this.comments.splice(index, 1)
      },
      addComment(comment) {
        this.comments.push(comment)
      }
    }
  }
</script>