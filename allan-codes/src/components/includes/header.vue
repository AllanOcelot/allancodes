<template>
    <header>
        <div class="container">
            <div class="row">
                <div class="col">
                    <router-link to="/">[AllanCodes]</router-link>
                </div>
                <div class="col align-self-end">
                    <div id="nav">
                        <router-link to="/blog">Blog</router-link>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<script>
export default {
  name: 'headerComponent'
}
</script>
<style>
    header {
        position: fixed;
        top: 0;
        width: 100%;
        z-index: 100;
        background: #00000096;
        border-bottom: 1px solid #ffffff38;
    }

    header #nav {
        float: right;
        font-weight: 400;
    }
    header nav a {
        font-weight: 100;
    }
</style>
