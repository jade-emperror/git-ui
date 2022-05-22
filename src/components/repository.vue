<template>
    <div class="overview-cont">
        <h1 class="title"><slot>
        </slot></h1>
        <p class="title">this page is cooking</p>
    </div>
</template>
<script>

export default{
    name:'RepositoryVue',
}
</script>
<style>
.title{
    color: #cccccc;
}
</style>