<template>
<main class="p-5">
    <div class="container">
        <div class="row">
            <AppMusicCard v-for="element in album" :key="element.author"/>
        </div>
    </div>
</main>
</template>

<script>

import AppMusicCard from './AppMusicCard.vue';
import axios from 'axios';

export default {
    name: 'AppMain',
    components: {
        AppMusicCard
    },
    data(){
        return{
            album: []
        }
    },
    created(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((resp) => {
            this.album = resp.data.response;
        })
    }
}
</script>

<style lang="scss" scoped>
main{
    height: calc(100vh - 70px);
    background-color: #262660;
}

</style>