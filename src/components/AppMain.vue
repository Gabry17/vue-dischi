<template>
<main class="p-5">
    <div class="container">
        <div class="row">
            <AppMusicCard />
        </div>
    </div>
</main>
</template>

<script>

import AppMusicCard from './AppMusicCard.vue';

export default {
    name: 'AppMain',
    components: {
        AppMusicCard
    }
}
</script>

<style lang="scss" scoped>
main{
    height: calc(100vh - 70px);
    background-color: #262660;
}

</style>