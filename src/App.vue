<script setup>
import Header from './components/Header.vue'
import FrontPage from './components/FrontPage.vue'
import ArticleCard from './components/ArticleCard.vue'
import Footer from './components/Footer.vue'
import articles from './assets/articles'
// console.log(articles.articlesList)
</script>

<template>
  <Header />
  <main>
    <FrontPage :article="articles.frontPage" />
    <div class="displayCard">
      <ArticleCard
        v-for="infos in articles.articlesList"
        :key="infos.id"
        :infos="infos"
      />
    </div>
  </main>
  <Footer />
</template>

<style scoped>
.displayCard {
  /* border: 2px solid green; */
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 1000px;
  margin: 0 auto;
  gap: 20px;
}
</style>
