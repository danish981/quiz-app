<script setup>

const props = defineProps(['quiz'])

</script>

<template>
  <div class="card col-md-3 m-2 p-0 pb-2 text-dark border-0" style="height: 15rem;">
    <img :src="quiz.img"
         alt="the quiz image"
         style=" object-fit: cover;">
    <div class="card-body p-0 ml-3">
      <p class="card-text font-weight-bold mt-2 mb-1">{{ props.quiz.name }}</p>
      <p class="card-text">{{ props.quiz.questions.length }} questions </p>
    </div>
  </div>
</template>


<style scoped>

.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
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
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
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