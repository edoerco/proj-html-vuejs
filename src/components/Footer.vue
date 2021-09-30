<template>
  <footer>
    <div class="footer-top">
      <div class="container-top"></div>
    </div>

    <div class="footer-bottom ">
      <div class="container-bottom-left"></div>
      <div class="container-bottom-right clearfix"></div>

    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss'; 

.footer-top {
  width: 100%;
  height: 600px;
  background-color: $woodsmoke;

  .container-top {
    width: 60%;
    height: 100%;
    margin: 0 auto;
    background-color: #fff;
  }
}

.footer-bottom {
  width: 100%;
  height: 100px;
  background-color: black;

  .container-bottom-left {
    width: 60%;
    height: 100%;
    margin-left: 20%;
    background-color: lightpink; // rimuovere il bc
    float: left;
  }

  .container-bottom-right {
    height: 100%;
    width: 20%;
    background-color: red; // rimuovere il bc
    float: right;
  }
}

.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
</style>