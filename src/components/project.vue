<template>
    <div class="project-cont">
        <h1>{{ titleCont }}</h1>
        <p>{{ msgCont }}</p>
    </div>
</template>

<script>
export default {
    name:'ProjectVue',
    props:[
        'titleCont' ,
        'msgCont' ,
    ],
}
</script>
<style>
body{
    color: wheat;
}
</style>