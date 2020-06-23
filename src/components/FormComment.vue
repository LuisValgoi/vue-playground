<template>
  <div class="container">
    <h1>Form</h1>

    <!-- Author -->
    <div class="input-group mb-3">
      <div class="input-group-prepend">
        <span class="input-group-text" id="basic-addon1">@</span>
      </div>
      <input type="text" class="form-control" placeholder="Type your name here" v-model="name">
    </div>

    <!-- Comment & Add -->
    <div class="row mb-3">
      <div class="col col-11">
        <div class="input-group">
          <div class="input-group-prepend">
            <span class="input-group-text" id="basic-addon1">...</span>
          </div>
          <input type="text" class="form-control" placeholder="Type your comment here" v-model="comment">
        </div>
      </div>

      <div class="col col-1" style="width: 100%">
        <button v-on:click="addComment" type="submit" class="btn btn-primary float-right">Add</button>
      </div>
    </div>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        name: '',
        comment: ''
      }
    },
    methods: {
      addComment() {
        if (this.name.trim() === '') {
          return;
        }

        this.$emit('add-comment', {
          name: this.name,
          comment: this.comment
        })

        this.name = '';
        this.comment = '';
      }
    }
  }
</script>