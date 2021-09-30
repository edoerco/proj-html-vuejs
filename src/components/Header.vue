<template>
  <header>
    <!-- header top  -->
    <div class="header-top">
      <div class="container-top">

      </div>
    </div>

    <!-- header bottom  -->
    <div class="header-bottom">
      <div class="container-bottom">

      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';

.header-top {
  width: 100%;
  height: 50px;
  background-color: #21333e;

  .container-top {
    width: 60%;
    height: 100%;
    margin: 0 auto;
  }
}

.header-bottom {
  width: 100%;
  height: 850px;
  background-image: url('../assets/img/bg-9.jpg');

  .container-top {
    width: 60%;
    height: 100%;
    margin: 0 auto;
  }
}

</style>
