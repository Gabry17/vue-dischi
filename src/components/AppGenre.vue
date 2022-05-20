<template>
  <div class="select">
    <label for="filterGenre">Generi:</label>
    <select name="filter genre" id="filterGenre" v-model='searchGenre' @change="$emit('searchChange', searchGenre)">
        <option value="">All</option>
        <option value="pop">Pop</option>
        <option value="rock">Rock</option>
        <option value="metal">Metal</option>
        <option value="jazz">Jazz</option>
    </select>
  </div>
</template>

<script>
export default {
    name: 'AppGenre',
    data(){
        return{
            searchGenre: ''
        }
    }
}
</script>

<style lang="scss" scoped>
.select{
    margin-bottom: 1em;
    label{
    color: white;
    margin-right: .5em;
    }
}
</style>