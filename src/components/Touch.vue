<template>
  <div class="body">
    <div class="container">
      <div class="col-left">
        <div class="title">
          <span>SEND A MESSAGE</span>
          <div class="title-section">
            <h2>Get in</h2>
            <div class="touch">
              <h2>Touch</h2>
            </div>
          </div>
          <p>We will respond to your message as soon as possible.</p>
        </div>
        <form>
          <input type="text" placeholder="Name">
          <input type="text" placeholder="Email">
          <input type="text" placeholder="Phone">
          <select name="" id="">
            <option value="">More info</option>
          </select>
          <!-- occhio alla scritta all'interno, non corrisponde -->
          <textarea cols="64" rows="5" placeholder="Message"></textarea>  
        </form>
      <button class="btn-1">SEND</button>
      </div>

      <div class="col-right">
        <div class="example">
          <h5>Example inc.</h5>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
          <p>Praesent diam lacus, dapibus sed imperdiet consectetur.</p>
        </div>
        <div class="contact-area">
          <div class="contact" v-for="(item, index) in items" :key="index">
            <i :class="item.font"></i>
            <span>{{item.text}}</span>
          </div>
        </div>
        <button class="btn-2">VIEW MAP</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Touch',
  data() {
    return {
      items: [
        {
          font: 'fas fa-phone-alt',
          text: '+1 (305) 1234-5678',
        },
        {
          font: 'fas fa-envelope',
          text: 'hello@example.com',
        },
        {
          font: 'fas fa-map-marker-alt',
          text: 'Main Avenue, 987',
        },
      ]
    }
  }
}
</script>


<style scoped lang="scss">
@import '../style/vars.scss';


.body { 
  width: 100%;
  height: 850px;
  background-color: $white;

  .container {
    width: 60%;
    height: 100%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    padding: 140px 0;

    .title {
      display: flex;
      flex-direction: column;
    }

    .col-left {
      display: flex;
      flex-direction: column;
      justify-content: center;
      width: 60%;
      height: 100%;

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

        h2 {
          color: black;
        }

        .touch {
          display: flex;
          align-items: center;
          background-color: rgba(03,83,84, 0.2);
          padding: 10px 15px;
          border-radius: 5px;
          margin-left: 10px;
          color: $blue-lagoon;

          h2 {
            color: $blue-lagoon;
          }
        }
      }

      form {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        width: 100%;
        margin: 75px 0 20px 0;

        input,
        select,
        textarea {
          padding: 15px;
          font-size: 18px;
          font-weight: 300;
          color: $mid-gray;
          border: none;
          outline: none;
          background-color: $gray-nurse;

          // nessun metodo trovato per cambiare il font del textarea
          // &::placeholder {
          //   font-size: 18px;
          //   font-weight: 300;
          //   }
        }

        // select {
        //   nessun metodo trovato per spostare la freccia
        // }

        input,
        select {
          width: calc(100% / 2 - 10px);
          margin-bottom: 20px;
        }

        input,
        textarea {
          border-radius: 5px;
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
        width: 100px;
        font-size: 15px;

        &:hover {
          cursor: pointer;
        }
      }
    }

    .col-right {
      display: flex;
      flex-direction: column;
      width: 35%;

      .example {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 160px;

        h5 {
          font-size: 20px;
        }

        p {
          letter-spacing: 1px;
        }
      }

      .contact-area {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 170px;
        margin: 60px 0 25px 0;

        .contact {
          display: flex;
          align-items: center;
          color: $blue-lagoon; 

          i {
            font-size: 20px;
            height: 45px;
            width: 45px;
            border-radius: 50%;
            background-color: rgba(3, 83, 84, 0.2);
            margin-right: 10px;
            display: flex;
            justify-content: space-around;
            align-items: center;
          }

          span {
            font-size: 18px;
            font-weight: 300;
          }
        }
      }

      .btn-2 {
        padding: 15px 25px;
        color: $blue-lagoon;
        font-size: 16px;
        font-weight: 300;
        background-color: transparent;
        border-radius: 5px;
        letter-spacing: 2px;
        border: $blue-lagoon solid 1px;
        width: 150px;

        &:hover {
          cursor: pointer;
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