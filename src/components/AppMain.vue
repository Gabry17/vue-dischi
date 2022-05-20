<template>
<main class="p-5">
    <div class="container">
        <AppGenre @searchChange="searchReceived($event)" />
        <AppAuthor />
        <div v-if="loading">
            <div class="text-center bg-primary">LOADING</div>
        </div>
        <div v-else class="g-3 row row-cols-5">
            <AppMusicCard v-for="element in valueGenre" :key="element.author" :albumObj="element"/>
        </div>
    </div>
</main>
</template>

<script>

import AppMusicCard from './AppMusicCard.vue';
import AppGenre from './AppGenre.vue';
import AppAuthor from './AppAuthor.vue';
import axios from 'axios';

export default {
    name: 'AppMain',
    components: {
        AppMusicCard,
        AppGenre,
        AppAuthor
    },
    data(){
        return{
            album: [],
            loading: true,
            text: ''
        }
    },
    methods: {
        searchReceived(elem){
            this.text = elem.toLowerCase();
        }
    },
    computed:{
        valueGenre(){
            const valueArray = this.album.filter((e) => {
                return e.genre.toLowerCase().includes(this.text)
            })
            return valueArray
            //console.log(this.album);
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