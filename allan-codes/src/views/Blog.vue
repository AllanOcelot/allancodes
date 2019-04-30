<template>
    <div class="page-wrapper">
        <headerComponent />

        <div class="blog-intro">
            <h1>The blog</h1>
            <p>Ramblings of a madman!</p>
        </div>

        <div class="blog-container">
            <div class="container">
                <div class="row">
                    <blog v-for="item in blogs"
                        :title="item.Title"
                        :BGSource="item.BGSource"
                        :Content="item.Content"
                        :PostDate="item.Date"
                    />
                </div>
            </div>
        </div>


    </div>
</template>
<script>
import axios from 'axios';
import headerComponent from '../components/includes/header.vue';
import blog from '../components/single/blog.vue';

export default {
    name: 'Blog',
    components: {
        headerComponent,
        blog,
    },
    data: function() {
        return {
            blogs: {
            },
        }
    },
    methods: {
        allBlogs: function(){
          var self = this;
          axios.get('/scripts/getblogs.php')
          .then(function (response) {
             self.blogs = response.data;
          })
          .catch(function (error) {
             console.log(error);
          });
        },
    },
    beforeMount(){
        this.allBlogs();
    },
}
</script>
<style>
    .blog-container{
        padding-top: 50px;
        margin-bottom: 100px;
    }
</style>
