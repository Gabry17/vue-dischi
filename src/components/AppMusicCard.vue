<template>
    <div class=" p-3 m-1 my-bg-color col-lg-2 col-md-3 text-center">
        <img :src="albumObj.poster" alt="">
        <h3>{{ albumObj.title }}</h3>
        <p>{{ albumObj.author }}</p>
        <p>{{ albumObj.year }}</p>
    </div>
</template>

<script>
export default {
    name: 'AppMusicCard',
    props:{
            albumObj: Object
        }
}
</script>

<style lang="scss" scoped>
div{
    color: white;
    p{
        color: gray;
    }
}

.my-bg-color{
    background-color: #36364a;
}
</style>