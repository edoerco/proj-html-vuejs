<template>
  <div class="body">
    <div class="container">

    </div>
  </div>
</template>

<script>
export default {
  name: 'Results',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';

.body {
  width: 100%;
  height: 600px;
  background-image: url('../assets/img/bg-10.jpg');
  background-position: center;

  .container {
    width: 60%;
    height: 100%;
    margin: 0 auto;
    background-color: #fff; // rimuovere il bc
  }
}
</style>