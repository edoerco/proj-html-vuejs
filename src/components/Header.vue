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
      <div class="overlay">
        <div class="container-bottom">
          <div class="info">
            <div class="nexgen">
              <div class="nex">
                <span>NEX</span>
              </div>
              <div class="gen">
                <span>GEN</span>
              </div>
            </div>
            <div class="nav">
                <li><a href="#">HOME</a></li>
                <li><a href="#">ABOUT</a></li>
                <li><a href="#">SERVICES</a></li>
                <li><a href="#">PROCESS</a></li>
                <li><a href="#">TESTIMONIALS</a></li>
                <li><a href="#"><i class="far fa-user"></i></a></li>
                <li><button class="btn-1">GET IN TOUCH</button></li>
            </div>
          </div>
          <!-- creare il secondo div contenente il titolo i paragrafi e i due bottoni  -->
          <div class="title">
            <span>LOGISTICS SERVICES</span>
            <h1>CARGO TRASPORT</h1>
            <p>Fractional or exclusive road cargo transpotation to all regions, with small, medium and large vehicles.</p>
            <div class="button-title">
              <button class="btn-1">GET IN TOUCH</button>
              <button class="btn-2">READ MORE</button>
            </div>
          </div>
        </div>
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
    font-weight: 200;
    font-size: 15px;

    .socials {
      display: flex;
      justify-content: space-between;
      width: 40%;
      list-style: none;

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

  .overlay {
    height: 100%;
    width: 100%;
    background-color: rgba(0,0,0,0.5);
  }

  .container-bottom {
    width: 60%;
    height: 100%;
    margin: 0 auto;
    padding-top: 30px;

    .info {
      display: flex;
      align-items: center;

      .nexgen {
      display: flex;
      align-items: center;
      font-weight: 500;
      font-size: 20px;

        .nex {
          display: flex;
          justify-content: flex-end;
          background-color: rgba(03,83,84, 0.3);
          color: $blue-lagoon;
          padding: 10px 0 10px 0;
          width: 90px;
          letter-spacing: 5px;
          border-radius: 20px 0 0px 20px;
        }

        .gen {
          color: $silver-sand;
          letter-spacing: 5px;
        }
      }

      .nav {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        list-style: none;
        width: 95%;
        font-weight: 500;

        li a {
          margin: 0 20px;
          text-decoration: none;
          color: $white;

        }

      }
    }

    .title {
      margin-top: 150px;
      width: 600px;
      height: 500px;

      span {
        color: $blue-chill;
        letter-spacing: 1px;
      }

      h1 {
        font-size: 70px;
        color: $white;
        margin: 10px 0 40px 0;
      }

      p {
        color: $silver-sand;
        font-size: 18px;
        letter-spacing: 2px;
        margin-bottom: 55px;
      }
    }
  }
}

.btn-1 {
  padding: 15px 25px;
  color: $white;
  font-weight: 500;
  background-color: $blue-lagoon;
  border-radius: 5px;
  letter-spacing: 2px;
  border: none;
}

.btn-2 {
  padding: 15px 25px;
  color: $white;
  font-weight: 500;
  background-color: transparent;
  border-radius: 5px;
  letter-spacing: 2px;
  border: $blue-lagoon solid 1px;
  margin-left: 20px;
}
</style>
