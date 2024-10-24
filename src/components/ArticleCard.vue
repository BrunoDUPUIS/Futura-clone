<script setup>
const props = defineProps({
  infos: Object,
})
const categoriesColors = {
  sciences: ['#be80ff', '#6325ff'],
  sante: ['#ff6b9f', '#ff4e52'],
  planete: ['#9fcb5c', '#069849'],
  maison: ['#fa9761', '#ff5957'],
  tech: ['#49adfa', '#2a3df7'],
}
console.log(props.infos.category)
</script>
<template>
  <div>
    <div class="card container">
      <img :src="infos.image" alt="" />
      <div class="cardCategory">
        <p>
          <span>{{ infos.category }}</span>
        </p>
        <p>{{ infos.subCategory }}</p>
      </div>
      <div class="cardTitle">
        <h2>{{ infos.title }}</h2>
        <p>{{ infos.date }}</p>
      </div>
    </div>
  </div>
</template>
<style scoped>
.cardTitle {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.cardTitle p {
  font-size: 10px;
  color: grey;
}
.cardCategory {
  display: flex;
  gap: 10px;
  margin-bottom: 5px;
}
h2 {
  font-size: 12px;
  font-family: Merriweather, serif;
}
img {
  width: 100%;
  height: 290px;
  object-fit: cover;
}
.card {
  /* border: 1px solid red; */
  height: 390px;
  width: 235px;
}
span {
  color: v-bind('categoriesColors[infos.category][0]');
}
</style>
