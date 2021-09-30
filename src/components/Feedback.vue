<template>
  <div class="body">
    <div class="container">

    </div>
  </div>
</template>

<script>
export default {
  name: 'Feedback',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';


.body {
  width: 100%;
  height: 800px;
  background-color: $woodsmoke;

  .container {
    width: 60%;
    height: 100%;
    margin: 0 auto;
    background-color: rgb(173, 119, 119);
  }
}

</style>