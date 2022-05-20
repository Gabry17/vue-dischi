<template>
<main class="p-5">
    <div class="container">
        <AppGenre />
        <div v-if="loading">
            <div class="text-center bg-primary">LOADING</div>
        </div>
        <div v-else class="g-3 row row-cols-5">
            <AppMusicCard v-for="element in album" :key="element.author" :albumObj="element"/>
        </div>
    </div>
</main>
</template>

<script>

import AppMusicCard from './AppMusicCard.vue';
import AppGenre from './AppGenre.vue';
import axios from 'axios';

export default {
    name: 'AppMain',
    components: {
        AppMusicCard,
        AppGenre
    },
    data(){
        return{
            album: [],
            loading: true,
        }
    },
    created(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((resp) => {
            this.album = resp.data.response;
            this.loading = false;
        })
    }
}
</script>

<style lang="scss" scoped>

</style>