<template>
    <div class="blog-block">
        <div class="title">
            <h3>{{Title}}</h3>
            <span><i class="fas fa-calendar-alt"></i> {{PostDate}}</span>
        </div>
        <div class="header-image" v-if="BGSource" v-bind:style="{ backgroundImage: 'url(' + BGSource + ')' }"></div>
        <div class="content">
            <div class="text" v-html="Content"></div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'headerComponent',
    props: ['Title', "BGSource", "Content", "PostDate", "ID"]
}
</script>
<style>
    .blog-block {
        width: 80%;
        border-radius: 4px;
        border: 1px solid #2f3e4f;
        position: relative;
        margin: 0 auto;
        overflow: hidden;
    }
    .blog-block .title {
        width: 100%;
        height: auto;
        padding: 10px 20px;
        border-bottom: 1px solid #000;
        position: absolute;
        top: 0;
        left: 0;
        background: rgba(47, 62, 79, 0.75);
    }
    .blog-block .title h3 {
        height: auto;
        font-size: 2em;
        margin: 0 auto;
        display: inline-block;
        font-weight: 600;
        cursor: default;
        letter-spacing: 1px;
        color: #fff;
        text-transform: uppercase;
    }
    .blog-block .title span {
        float: right;
        padding: 5px 10px;
        background: #fff;
        color: #2f3e4f;
        border-radius: 6px;
        position: relative;
        top: 5px;
        cursor: default;
    }
    .blog-block .title span i {
        margin-right: 5px;
    }
    .blog-block .header-image {
        width: 100%;
        height: 320px;
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center center;
    }
    .blog-block .content {
        width: 100%;
        padding: 40px 20px;
    }
</style>
