<!-- <script> -->
<!-- // Options API -->
  <!-- // export default{
  //   // In Options Api Data comes first and then methods
  //   data(){
  //     return{
  //       name: 'John Doe',
  //       status: 'active',
  //       tasks: ['Task One', 'Task Two', 'Task three'] ,
  //     };
  //   },
  //   methods: {
  //     toggleStatus(){

  //     }
  // }
// }  -->

<!-- Composition API -->
<!-- <script setup>
import { ref } from 'vue';
    const name = ref("John Doe");
    const status = "active";
    const tasks = ['Task one'];

    const toggleStatus = () => {
      if(status.value === 'active'){
        this.status = 'active';
      }else if (this.status === 'pending'){
        this.status = 'pending';
      }else{
        this.status = 'inactive';
      }
    };
</script> -->


<script setup>
  import Navbar from './components/Navbar.vue';
  import { RouterView } from 'vue-router';

</script>

<template>
  <Navbar />
  <RouterView />
</template> 


<!-- <template>
  <div>
    <h1>Latest News</h1>
    <div v-if="error" class="error">{{ error }}</div>
    <div v-if="loading">Loading...</div>
    <div v-if="!loading && news.length">
      <div v-for="(article, index) in news" :key="index" class="news-article">
        <h2>{{ article.title }}</h2>
        <p>{{ article.description }}</p>
        <a :href="article.url" target="_blank">Read more</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      news: [],
      loading: true,
      error: null,
    };
  },
  methods: {
    async fetchNews() {
      try {
        const response = await fetch('https://newsapi.org/v2/top-headlines?country=us&apiKey=644b47ad580e41d38073cb521e256928');
        const data = await response.json();

        if (response.ok) {
          this.news = data.articles;
        } else {
          this.error = data.message || 'Failed to load news';
        }
      } catch (error) {
        this.error = 'An error occurred while fetching news';
      } finally {
        this.loading = false;
      }
    },
  },
  mounted() {
    this.fetchNews();
  },
};
</script>

<style>
/* Add some basic styling */
.news-article {
  margin-bottom: 20px;
}
.error {
  color: red;
}
</style> -->
