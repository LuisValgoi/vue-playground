<template>
  <div>
    <FormComment v-on:add-comment="addComment"/>
    <div class="dropdown-divider"></div>
    <div class="container">
      <h1>Comments</h1>
      <p v-if="this.comments.length === 0">No comment for now...</p>
      <Comment v-else v-on:delete-comment="deleteComment" :comments="comments" />
    </div>
  </div>
</template>

<script>
  import FormComment from '../components/FormComment.vue'
  import Comment from '../components/Comment.vue'
  
  export default {
    components: {
      FormComment,
      Comment
    },
    data() {
      return {
        comments: []
      }
    },
    methods: {
      formatComment(value) {
        if (value.trim() === '') {
          return 'N/A'
        }
      },
      deleteComment(index) {
        this.comments.splice(index, 1)
      },
      addComment(comment) {
        this.comments.push(comment)
      }
    }
  }
</script>