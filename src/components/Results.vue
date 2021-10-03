<template>
  <div class="body">
    <div class="container">
      <div class="title">
        <span>WHAT ARE WE DOING</span>
        <div class="title-section">
          <div class="results">
            <h2>Results</h2>
          </div>
            <h2>in Numbers</h2>
        </div>
      </div>

      <div class="container-number">
        <div class="number" v-for="(result, index) in results" :key="index">
          <span>{{result.number}}</span>
          <p>{{result.text}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Results',
  data() {
    return {
      results: [
        {
          number: 128,
          text: 'Certifications'
        },
        {
          number: 230,
          text: 'Employees'
        },
        {
          number: 517,
          text: 'Customers'
        },
        {
          number: 94,
          text: 'Countries Served'
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
  height: 600px;
  background-image: url('../assets/img/bg-10.jpg');
  background-position: center;
  padding: 150px 0;

  .container {
    width: 60%;
    height: 100%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;

    .title {
      text-align: center;
    }

    .title span {
      color: $blue-chill;
      font-size: 15px;
      font-weight: bold;
    }

    .title-section {
      display: flex;
      align-items: center;
      font-size: 30px;
      color: $white;
      margin-top: 15px;


      .results {
        display: flex;
        align-items: center;
        background-color: rgba(03,83,84, 0.2);
        padding: 10px 15px;
        border-radius: 5px;
        margin-right: 10px;
      }
    }

    .container-number {
      width: 100%;
      display: flex;
      justify-content: space-around;

      .number {
      display: flex;
      flex-direction: column;
      text-align: center;

        span {
          color: $blue-chill;
          font-size: 45px;
          font-weight: bold;
          margin-bottom: 15px;
        }

        p {
          color: $white;
          font-size: 25px;
          font-weight: bold;
        }
      }
    }
  }
}
</style>