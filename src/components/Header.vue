<template>
  <header>
    <!-- header top  -->
    <div class="header-top">
      <div class="container-top">
          <div class="clock">
            <p><i class="fas fa-clock"></i> Open Hours: Mon - Sat - 9:00 - 18:00</p>
          </div>
          <div class="socials">
              <li><i class="fas fa-phone-alt"></i> +1(305)1234-5678</li>
              <li><i class="fas fa-envelope"></i> hello@example.com</li>
              <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
              <li><a href="#"><i class="fab fa-twitter"></i></a></li>
              <li><a href="#"><i class="fab fa-linkedin-in"></i></a></li>
          </div>
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
  color: $silver-sand;

  .container-top {
    width: 60%;
    height: 100%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .socials {
      display: flex;
      justify-content: space-between;
      width: 40%;
      list-style: none;
      font-weight: 200;
      font-size: 15px;

      .fab {
        color: $silver-sand;
      }
    }
    
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
