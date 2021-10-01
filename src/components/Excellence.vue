<template>
  <div class="body">
    <div class="container">
      <div class="col-left">
        <span>WHO WE ARE</span>
        <div class="title-section">
          <div class="excellence">
            <i class="far fa-gem"></i>
            <h2>Excellence</h2>
          </div>
          <h2>in Transport</h2>
        </div>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo minus repellendus atque iusto possimus mollitia corrupti ea. Sed vitae tellus et aliqet fermentum non locus. </p>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, cumque modi expedita consequuntur soluta. Pellenteque quis susctipt magna.
        </p>
        <div class="lorem">
          <p><i>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis eaque est inventore architecto consequuntur. Sed nis nisi, retrum sit amet elit. </i></p>
        </div>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. </p>
        <ul>
          <li>Lorem ipsum dolor sit amet</li>
          <li>Consectetur adipiscing elit</li>
          <li>Integer molestie lorem at massa</li>
          <li>Facilitatis in pretium nisl aliquet</li>
          <li>Dapibus hendrerit mauris curabitur</li>
        </ul>
      </div>
      <div class="col-right">
        <h3>Vehicle Types</h3>
        <div class="veicles">
          <div v-for="(truck, index) in trucks" :key="index" class="veicle">
            <img :src="require(`../assets/${truck.photo}`)" :alt="truck.size">
            <div class="text-veicle">
              <h4>{{truck.size}}</h4>
              <span>Max Weight {{truck.weight}} Kg</span>
            </div>
          </div>
        </div>
        <div class="certification">
          <h3>Certifications</h3>
          <div class="images">
            <img src="../assets/img/certificate.png" alt="">
            <img src="../assets/img/certificate.png" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Excellence',
  data() {
    return {
      trucks: [
        {
          photo: 'img/truck.png',
          size: 'Light',
          weight: 1200
        },
        {
          photo: 'img/truck.png',
          size: 'Medium',
          weight: 6000
        },
        {
          photo: 'img/truck.png',
          size: 'Heavy',
          weight: 24000
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
  height: 900px;
  background-color: $white;

  .container {
    display: flex;
    justify-content: space-between;
    width: 60%;
    height: 100%;
    margin: 0 auto;
    padding: 150px 0;


    .col-left {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      width: 65%;
      height: 100%;
      color: $mid-gray;

      p,
      li {
        font-weight: 300;
        font-size: 17px;
      }

      span {
        color: $blue-chill;
        font-size: 15px;
        font-weight: bold;
      }

      .title-section {
        display: flex;
        align-items: center;
        font-size: 30px;

        h2 {
          color: black;
        }

        .excellence {
          display: flex;
          align-items: center;
          background-color: rgba(03,83,84, 0.2);
          padding: 10px 15px;
          border-radius: 5px;
          margin-right: 10px;
          color: $blue-lagoon;


          h2 {
            color: $blue-lagoon;
          }

          i {
            font-size: 40px;
            margin-right: 10px;
          }
        }
      }

      .lorem {
        height: 70px;
        width: 90%;
        padding: 15px 0 15px 20px;
        border-left: 5px solid rgba(03,83,84, 0.2);
      }

    }

    .col-right {
      width: 30%; 
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      h3 {
        font-size: 25px;
        letter-spacing: 1px;
      }

      .veicles {
        height: 300px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }

      .veicle {
        display: flex;
        align-items: center;
        height: 100px;
        padding: 20px 0;


        &:nth-child(2) {
          border-top: 1px solid black;
          border-bottom: 1px solid black;

        }

        img {
          width: 100px;
          background-color: rgba(03,83,84, 0.2);
          padding: 10px;
          border-radius: 5px;
          margin-right: 20px;
          box-shadow: 2px 2px 9px -5px #000000;
        }

        .text-veicle {
          display: flex;
          flex-direction: column;
          justify-content: space-evenly;
          height: 100%;
          
          h4 {
            font-size: 25px;
          }

          span {
            font-weight: 300;
            font-size: 17px;
          }
        }
      }

      .images {
        display: flex;
        justify-content: space-between;
        margin-top: 20px;

        img {
          width: 150px;
          background-color: #fff;
          box-shadow: 2px 2px 9px -5px #000000;
        }
      }
    }
  }
}
</style>