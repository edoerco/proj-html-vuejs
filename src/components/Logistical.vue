<template>
  <div class="body">
    <div class="container-top">
      <span>HOW IT WORKS IN PRACTICE</span>
      <div class="title-section">
        <div class="logistical">
          <h2>Logistical</h2>
        </div>
        <h2>Procedure</h2>
      </div>
      <p>We work whit innovative methodologies to ensure that the entire delivery process is done from start to finish as planned</p>
    </div>
    <div class="container-bottom">
      <div class="line">
        <div class="col" v-for="(procedure, index) in procedures" :key="index">
          <div class="number">
            <span>0{{procedure.number}}</span>
          </div>
          <h3>{{procedure.title}}</h3>
          <p>{{procedure.text}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Logistical',
  data() {
    return {
      procedures: [
        {
          number: 1,
          title: 'Collection of information',
          text: 'Lorem ipsum dolor sit amet consectetur.'
        },
        {
          number: 2,
          title: 'Service Invoice Sending',
          text: 'Lorem ipsum dolor sit amet consectetur.'
        },
        {
          number: 3,
          title: 'Withdrawal of Cargo',
          text: 'Lorem ipsum dolor sit amet consectetur.'
        },
        {
          number: 4,
          title: 'Transport Customer Order',
          text: 'Lorem ipsum dolor sit amet consectetur.'
        },
        {
          number: 5,
          title: 'Successful Delivery',
          text: 'Lorem ipsum dolor sit amet consectetur.'
        }
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
  height: 650px;
  background-color: $gray-nurse;

  .container-top {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 35%;
    height: 350px;
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

        .logistical {
          display: flex;
          align-items: center;
          background-color: rgba(03,83,84, 0.2);
          padding: 10px 15px;
          border-radius: 5px;
          margin-right: 10px;
          color: $blue-lagoon;
        }
    }

  }


  .container-bottom {
    width: 100%;

    .line {
      position: relative;
      display: flex;
      justify-content: center;
      width: 100%;
      height: 5px;
      background: rgba(03,83,84, 0.2);

      .col {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        width: 250px;
        height: 200px;
        margin: 0 30px;
        padding: 0 12px;

        .number {
          position: absolute;
          display: flex;
          align-items: center;
          justify-content: center;
          height: 50px;
          width: 50px;
          background-color: $bermuda;
          color: $blue-lagoon;
          border-radius: 50%;
          top: -20px;
          font-size: 20px;
          font-weight: 700;
        }

        h3 {
          font-size: 25px;
          margin: 50px 0 30px 0;
          font-weight: 500;
        }
      }
    }
  }
}

p {
  font-weight: 300;
  font-size: 17px;
  color: $mid-gray;
}

</style>