<template>
  <div class="author">
      <label for="filterAuthor">Artisti:</label>
      <select name="filter author" id="filterAuthor">
          <option value="">All</option>
          <option value="bon jovi">Bon Jovi</option>
          <option value="queen">Queen</option>
          <option value="sting">Sting</option>
          <option value="steve gadd">Steve Gadd</option>
          <option value="iron maiden">Iron Maiden</option>
          <option value="eric clapton">Eric Clapton</option>
          <option value="deep purple">Deep Purple</option>
          <option value="metallica">Metallica</option>
          <option value="dave weckl">Dave Weckl</option>
          <option value="michael jackson">Michael Jackson</option>
      </select>
  </div>
</template>

<script>
export default {
    name: 'AppAuthor'
}
</script>

<style lang="scss" scoped>
.author{
    color: white;
    margin-bottom: 1em;
    label{
        margin-right: .5em;
    }
}
</style>