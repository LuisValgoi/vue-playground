<template>
  <div class="container">
    <h1>Form</h1>

    <!-- author input -->
    <div class="input-group mb-3">
      <div class="input-group-prepend">
        <span class="input-group-text" id="basic-addon1">@</span>
      </div>
      <input type="text" class="form-control" placeholder="Type your name here" aria-label="Username">
    </div>

    <div class="row mb-3">

      <!-- comment input -->
      <div class="col col-11">
        <div class="input-group">
          <div class="input-group-prepend">
            <span class="input-group-text" id="basic-addon1">Comment</span>
          </div>
          <input type="text" class="form-control" placeholder="Insert your comment here" aria-Comment="Username">
        </div>
      </div>

      <!-- add button -->
      <div class="col col-1" style="width: 100%">
        <div >
          <a href="#" class="btn btn-primary float-right">Add</a>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
</script>