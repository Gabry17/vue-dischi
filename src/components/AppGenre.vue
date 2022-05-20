<template>
  <div class="select">
    <select name="" id="" v-model='searchGenre'>
      <option value=""></option>
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

</style>