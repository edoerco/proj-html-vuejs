<template>
  <div class="body">
    <div class="container">
      <div class="container-top">
        <span>CUSTOMER TESTIMONIALS</span>
        <div class="title-section">
          <h2>Trusted</h2>
          <div class="feedback">
            <h2>Feedback</h2>
          </div>
        </div>
        <p>We work intensively in search of ideals that can add up in the lives of our customers. This is what moves us and we are grateful for the recognition.</p>
      </div>
      <div class="container-bottom">
        <div class="card" v-for="(item, index) in feedbacks" :key="index">
        <img :src="require(`../assets/${item.photo}`)" :alt="item.name">
        <p>Praesent volutpat justo sit amet elementum malesuada. Present sagittis augue justo, in accumsan orci rhoncus at pellentesque.</p>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
        <div class="apex">"</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Feedback',
  data() {
    return {
      feedbacks: [
        {
          photo: 'img/logo-1.png',
          name: 'woo commerce'
        },
        {
          photo: 'img/logo-2.png',
          name: 'wordpress'
        },
        {
          photo: 'img/logo-3.png',
          name: 'pingdom'
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
  padding: 150px 0;

  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    width: 60%;
    height: 100%;
    margin: 0 auto;

    .container-top {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 75%;
    margin: 0 auto;
    text-align: center;

      span {
        color: $blue-chill;
        font-size: 15px;
        font-weight: bold;
      }

      .title-section {
        display: flex;
        align-items: center;
        font-size: 30px;
        margin: 20px 0;
        color: $white;

        .feedback {
          display: flex;
          align-items: center;
          background-color: rgba(03,83,84, 0.5);
          padding: 10px 15px;
          border-radius: 5px;
          margin-left: 10px;
        }
      }
    }

    .container-bottom {
      display: flex;
      justify-content: space-between;

      .card {
        position: relative;
        width: calc(100% / 3 - 40px);
        background-color: $shark;
        padding: 40px;
        border-radius: 15px;

        &:nth-child(2) {
          margin: 0 30px;
        }

        p {             // non mi prende il first-child
          margin: 10px 0  5px 0;
          line-height: 22px;
        }

        img {
          width: 120px;
          filter: invert(100%); // vi odio tanto <3
        }

        .apex {
          position: absolute;
          font-size: 100px;
          color: $mid-gray;
          right: 30px;
          bottom: -50px;
        }

      }
    }
  }
}

p {
  font-weight: 300;
  font-size: 17px;
  color: $silver-sand;
}

</style>