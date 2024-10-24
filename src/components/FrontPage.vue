<script setup>
const props = defineProps({ article: Object })
// console.log(props.article)
</script>
<template>
  <main class="container">
    <img :src="article.image" alt="" />

    <div class="frontPageCategory">
      <span
        ><p>{{ article.category.toUpperCase() }}</p></span
      >
      <p>{{ article.subCategory.toUpperCase() }}</p>
    </div>
    <div class="frontPageTitle">
      <h2>
        <span>{{ article.title }}</span>
      </h2>
    </div>

    <div class="frontPageTeaser">{{ article.teaser }}</div>
  </main>
</template>

<style scoped>
h2 {
  font-family: Merriweather, serif;
}
h2 span {
  background-color: black;
  line-height: 35px;
  padding: 3px;
  /* border: 1px solid red; */
}
.frontPageCategory > span {
  color: #be80ff;
}
main {
  height: 300px;
  margin-top: 66px;
  position: relative;
  margin-bottom: 20px;
  /* border: 3px solid green; */
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: bottom;
}
.frontPageCategory {
  /* border: 1px solid blue; */
  border-left: 5px solid #be80ff;
  display: flex;
  gap: 15px;
  width: 128px;
  justify-content: center;
  position: absolute;
  top: 60px;
  left: 60px;
  color: white;
  background-color: black;
  font-size: 10px;
  padding: 5px;
}
.frontPageTitle {
  border-left: 5px solid #be80ff;
  position: absolute;
  top: 71px;
  left: 60px;
  color: white;
  width: 600px;
  font-size: 25px;
  margin-top: 9px;
}

.frontPageTeaser {
  position: absolute;
  top: 160px;
  left: 60px;
  color: white;
  width: 620px;
  /* border: 1px solid yellow; */
  padding: 10px;
  font-size: 12px;
  line-height: normal;
  background-color: rgba(0, 0, 0, 0.446);
}
</style>
