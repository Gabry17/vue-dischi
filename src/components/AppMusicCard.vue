<template>
    <div class="mr-1 p-3 my-bg-color text-center">
        <img :src="albumObj.poster" alt="">
        <h3>{{ albumObj.title }}</h3>
        <h4>{{ albumObj.genre }}</h4>
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