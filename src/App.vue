
<script setup>
  import { ref, watch } from 'vue';
  import quizzesJson from './data/data.json';
  import Card from './components/Card.vue';
  
  const quizzes = ref(quizzesJson);


  const search = ref('');

  watch(search, () => {
    if(search.value) {
      quizzes.value = quizzes.value.filter(quiz => quiz.name.toLowerCase().includes(search.value.toLowerCase()));
    } else {
      quizzes.value = quizzesJson;
    }
  })

</script>

<template>
  <main>
    <div class="container mt-3">
      <header class="d-flex justify-content-between align-items-center">
        <h1>Quizzes</h1>
        <input type="text" v-model.trim="search" class="form-control ml-4 w-25" placeholder="search ...">
      </header>
      <div class="row mt-4">

        <!-- <div class="card col-md-3 m-2 p-0 pb-2 text-dark border-0" style="height: 15rem;" v-for="quiz in quizzes"  :key="quiz.id" >
          <img :src="quiz.img" alt="the quiz image" style=" object-fit: cover;">
          <div class="card-body p-0 ml-3" >
            <p class="card-text font-weight-bold mt-2 mb-1">{{ quiz.name }}</p>
            <p class="card-text">{{ quiz.questions.length }} questions</p>
          </div>
        </div> -->


        <Card v-for="quiz in quizzes" :key="quiz.id" :quiz="quiz" />

      </div>
    </div>
  </main>
</template>


<style scope>

.show {
  display: flex;
}

</style>







