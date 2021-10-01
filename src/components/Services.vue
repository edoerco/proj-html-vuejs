<template>
  <div class="body">
    <div class="container"> 
      <span>ROAD TRANSPORT</span>
      <div class="title-section">
          <h2>Main</h2>
        <div class="services">
          <h2>Services</h2>
        </div>
      </div>
      <div class="text-button">
        <div class="text">
          <p>With all of this expertise and capability comes an unrivalled commitment to costomer service. We will work hard to undestand your needs in order to develop a productive,long-term partnership.</p>
        </div>
        <div class="button">
          <button class="btn-2">SEE ALL</button>
        </div>
      </div>
      <div class="container-cards">
        <div class="card" v-for="(service, index) in services" :key="index">
          <div class="items">
            <i id="logo" :class="service.item"></i>
            <i id="arrow" class="fas fa-arrow-right"></i>
          </div>
          <h4>{{service.title}}</h4>
          <p>{{service.text}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Services',
  data() {
    return {
      services: [
        {
          item: 'fas fa-truck-loading',
          title: 'Technology',
          text: 'We are continually focused on developing technology solutions adapted to our client\'s need',
        },
        {
          item: 'fas fa-temperature-low',
          title: 'Reefer Cargo',
          text: 'Regular and frequent monitoring from the receipt of the loaded container to final destination.',
        },
        {
          item: 'fas fa-boxes',
          title: 'Dry Cargo',
          text: 'We work with most types of dry cargo, from valuable cargo to the most dangerous requiring care.',
        },
      ]
    }
  }
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
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 60%;
    height: 100%;
    margin: 0 auto;
    padding: 150px 0;

    span {
      color: $blue-chill;
      font-size: 15px;
      font-weight: bold;
    }

    .title-section {
      display: flex;
      align-items: center;
      font-size: 30px;
      color: $white;

      .services {
        display: flex;
        align-items: center;
        background-color: rgba(03,83,84, 0.2);
        padding: 10px 15px;
        border-radius: 5px;
        margin-left: 10px;
      }
    }

    .text-button {
      display: flex;
      color: $white;

      .text {
        width: 70%;
      }

      .button {
        display: flex;
        justify-content: flex-end;
        width: 30%;

        .btn-2 {
          padding: 15px 25px;
          color: $white;
          font-weight: 500;
          background-color: transparent;
          border-radius: 5px;
          letter-spacing: 2px;
          border: $blue-lagoon solid 1px;
        }
      }
    }

    .container-cards {
      display: flex;
      width: 100%;
    }

    .card {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding: 40px;
      width: calc(100% / 3 - 20px);
      height: 300px;
      background-color: $shark;
      border-radius: 10px;

      &:nth-child(2) {
        margin: 0 30px;
      }

      .items {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;

        #logo {
          font-size: 35px;
          color: $blue-lagoon;
          background-color: rgba(03,83,84, 0.2);
          padding: 15px;
          border-radius: 50%;

        }

        #arrow {
          font-size: 25px;
          color: rgb(03,83,84,);
        }
      }

      h4 {
        color: $white;
        font-size: 25px;
      }
    }
  }

  p {
    font-weight: 300;
    font-size: 17px;
    color: $silver-sand;
  }
}

</style>