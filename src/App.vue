
<script setup>
  import { ref } from 'vue';

</script>

<template>
  <main>

    <div class="container mt-3">
      <header class="d-flex justify-content-between align-items-center">
        <h1>Quizzes</h1>
      </header>
      <div class="row">

        <div class="card col-md-3 m-2 p-0"  >
          <div class="card-body">
            <h5 class="card-title">Quiz title</h5>
            <p class="card-text">quiz text and notes</p>
            <p class="card-footer text-muted">quiz date</p>
          </div>
        </div>
        
        <div class="card col-md-3 m-2 p-0"  >
          <div class="card-body">
            <h5 class="card-title">Quiz title</h5>
            <p class="card-text">quiz text and notes</p>
            <p class="card-footer text-muted">quiz date</p>
          </div>
        </div>

        <div class="card col-md-3 m-2 p-0"  >
          <div class="card-body">
            <h5 class="card-title">Quiz title</h5>
            <p class="card-text">quiz text and notes</p>
            <p class="card-footer text-muted">quiz date</p>
          </div>
        </div>
    
      </div>
    </div>
  </main>
</template>


<style scope>

.show {
  display: flex;
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  border-radius: 5px;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.card-title {
  font-size: 1.1rem;
  font-weight: 600;
}

.card-text {
  font-size: 0.9rem;
}

.card-footer {
  font-size: 0.8rem;
}
</style>







