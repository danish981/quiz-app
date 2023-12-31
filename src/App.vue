
<script setup>
  import { ref } from 'vue';
  import quizzesJson from './data/data.json';
  const quizzes = ref(quizzesJson);

  const search = ref('');
  
</script>

<template>
  <main>
    <div class="container mt-3">
      <header class="d-flex justify-content-between align-items-center">
        <h1>Quizzes</h1>
        <input type="text" v-model.trim="search" class="form-control ml-4 w-25" placeholder="search ...">
      </header>
      <div class="row mt-4">

        <div class="card col-md-3 m-2 p-0 pb-2 text-dark border-0" style="height: 15rem;" v-for="quiz in quizzes"  :key="quiz.id" >
          <img :src="quiz.img" alt="the quiz image" style=" object-fit: cover;">
          <div class="card-body p-0 ml-3" >
            <p class="card-text font-weight-bold mt-2 mb-1">{{ quiz.name }}</p>
            <p class="card-text">{{ quiz.questions.length }} questions</p>
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

.card img {
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
  cursor: pointer;
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







