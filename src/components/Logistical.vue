<template>
  <div class="body">
    <div class="container-top"></div>
    <div class="container-bottom"></div>
  </div>
</template>

<script>
export default {
  name: 'Logistical',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';

.body {
  width: 100%;
  height: 700px;
  background-color: $gray-nurse;

  .container-top {
    width: 45%;
    height: 400px;
    margin: 0 auto;
    background-color: black; //rimuovere il bc
  }

  .container-bottom {
    width: 75%;
    height: 300px;
    margin: 0 auto;
    background-color: white; // rimuovere il bc
  }
}

</style>