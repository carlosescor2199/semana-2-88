<template>
  <div id="app">
    <NavBar />
    <Carousel />
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
        <NewsCard
          v-for="(notice, index) in this.news.slice(0, 4)"
          :key="index"
          :author="notice.author"
          :title="notice.title"
          :description="notice.description"
          :url="notice.url"
          :image="notice.urlToImage"
          :date="notice.publishedAt"
        />
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import Carousel from "./components/Carousel";
import NewsCard from "./components/NewsCard";
import axios from "axios";
export default {
  name: "App",
  data() {
    return {
      news: [],
    };
  },
  components: {
    NavBar,
    Carousel,
    NewsCard,
  },
  methods: {
    async getNews() {
      const res = await axios.get(
        "http://newsapi.org/v2/top-headlines?country=co&category=technology&apiKey=2ab63997a09846ffa5bc1f3f43455b70"
      );
      this.news = res.data.articles;
    },
  },
  mounted() {
    this.getNews();
  },
};
</script>
