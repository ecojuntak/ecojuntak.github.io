<template>
    <div class="blog-section">
        <h1 class="section-title">Blog Post</h1>

        <v-container fluid grid-list-md>
            <v-layout row wrap>
                <div class="card-group" v-for="blog in activeBlogs" :key="blog.title">
                    <a :href=blog.url target="_blank" class="blog-card" >
                        <v-card class="ml-3" aspect-ratio="2.75">
                            <v-img :src="blog.src" height="200px" > </v-img>

                            <v-card-title primary-title>
                            <div>
                                <h2 style="text-decoration: none;"> {{blog.title}} </h2>
                            </div>
                            </v-card-title>
                        </v-card>
                    </a>
                </div>
            </v-layout>
        </v-container>

        <div class="text-xs-center">
            <v-pagination v-model="page" :length="totalPage" :dark="true" color="rgb(29, 185, 84)" :total-visible="6" circle @input="updateBlogList"> </v-pagination>
        </div>
    </div>
</template>

<script>
import blogs from '../data/blog.json'

export default {
  name: "Blog",
  data() {
    return {
      blogs: blogs,
      page: 1,
      itemPerPage: 4,
      totalPage: 1,
      activeBlogs: []
    };
  },
  methods: {
    updateBlogList: function() {
      this.activeBlogs = [];
      const begin = (this.page * this.itemPerPage) - (this.itemPerPage)
      let end = (this.page * this.itemPerPage) - 1
      
      if(end > this.blogs.length - 1) {
        end = this.blogs.length - 1
      }

      for(let i=begin ; i <= end; i++) {
        this.activeBlogs.push(this.blogs[i])
      }
    },
  },
  mounted() {
    this.totalPage = Math.ceil(this.blogs.length / this.itemPerPage);
    this.updateBlogList()
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Fira+Sans');

.blog-section {
  padding: 10px;
  margin-top: 15px;
}

h1 {
  font-family: "K2D", sans-serif;
  color: rgb(29, 185, 84);
  font-size: 30px;
  padding-left: 40px;
}

.blog-card {
  text-decoration: none;
}

.blog-card :hover {
  color: rgb(29, 185, 84);
}

.card-group {
  width: 50%;
  margin-top: 20px;
  font-family: 'Fira Sans', sans-serif;
}

.section-title::after {
  content: "\258B";
  color: rgba(33, 33, 33, 1.0);
  animation: blink-animation 1.1s infinite;
  animation-timing-function: ease;
  animation-delay: 0.5s;
  margin-left: 5px;
}

@media screen and (max-width: 850px) {
  .card-group {
    width: 100%;
    font-family: 'Fira Sans', sans-serif;
  }
}
</style>
