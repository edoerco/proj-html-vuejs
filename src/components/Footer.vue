<template>
  <footer>
    <div class="footer-top">
      <div class="container-top">
        <div class="col">
          <div class="nexgen">
            <div class="nex">
              <span>NEX</span>
            </div>
            <div class="gen">
              <span>GEN</span>
            </div>
          </div>
          <p>A Funcionale HTML Template for Corporate & Business.</p>
          <div class="contact-area">
            <div class="contact" v-for="(contact, index) in contacts" :key="index">
              <i :class="contact.font"></i>
              <span>{{contact.text}}</span>
            </div>
          </div>
          <button class="btn-2">GET IN TOUCH</button>
        </div>
        <div class="container-card">
          <!-- card 1 -->
          <div class="card">
            <h3>About</h3>
            <ul>
              <!-- l'angolo piu specifico richiede la versione pro -->
              <li v-for="(info, index) in about" :key="index">
                <i class="fas fa-chevron-right"></i><a href="info.url">{{info.text}}</a> 
              </li>
            </ul>
          </div>

          <!-- card 2 -->
          <div class="card">
            <h3>Transport</h3>
            <ul>
              <!-- l'angolo piu specifico richiede la versione pro -->
              <li v-for="(info, index) in transport" :key="index">
                <i class="fas fa-chevron-right"></i><a href="info.url">{{info.text}}</a> 
              </li>
            </ul>
          </div>

          <!-- card 3 -->
          <div class="card">
            <h3>Support</h3>
            <ul>
              <!-- l'angolo piu specifico richiede la versione pro -->
              <li v-for="(info, index) in support" :key="index">
                <i class="fas fa-chevron-right"></i><a href="info.url">{{info.text}}</a> 
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <div class="footer-bottom ">
      <div class="container-bottom-left">
        <p>Enjoy the low price. We are tracking any intention of privacy.</p>
        <p>© 2020 NEXGEN is Proudly Powered by <span>Codings</span>.</p>
      </div>
      <div class="container-bottom-right clearfix">
        <a href="#"><i class="fas fa-arrow-up"></i></a>
      </div>

    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      contacts: [
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
      ],

      about: [
        {
          text: 'The Company',
          url: '#'
        },
        {
          text: 'Istitutional',
          url: '#'
        },
        {
          text: 'Social & Event',
          url: '#'
        },
        {
          text: 'Innovation',
          url: '#'
        },
        {
          text: 'Environment',
          url: '#'
        },
        {
          text: 'Technology',
          url: '#'
        },
      ],

       transport: [
        {
          text: 'Industrialized',
          url: '#'
        },
        {
          text: 'Chemicals',
          url: '#'
        },
        {
          text: 'Packaged Liquids',
          url: '#'
        },
        {
          text: 'Construcrion',
          url: '#'
        },
        {
          text: 'Laminated Wood',
          url: '#'
        },
        {
          text: 'And others',
          url: '#'
        },
      ],

      support: [
        {
          text: 'Responsability',
          url: '#'
        },
        {
          text: 'Terms of Use',
          url: '#'
        },
        {
          text: 'About Cookies',
          url: '#'
        },
        {
          text: 'Privacy Policy',
          url: '#'
        },
        {
          text: 'Accessibility',
          url: '#'
        },
        {
          text: 'Information',
          url: '#'
        },
      ],
    }
  }
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
    padding: 150px 0;
    display: flex;
    justify-content: space-between;

    .col {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      width: 20%;
      height: 100%;

      .nexgen {
        display: flex;
        align-items: center;
        font-weight: 500;
        font-size: 20px;

        .nex {
          display: flex;
          justify-content: flex-end;
          background-color: rgba(03,83,84, 0.3);
          padding: 10px 0 10px 0;
          width: 90px;
          color: $blue-lagoon;
          letter-spacing: 5px;
          border-radius: 20px 0 0px 20px;
        }

        .gen {
          color: $silver-sand;
          letter-spacing: 5px;
          margin-left: 5px;
        }
      }

      .contact-area {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 90px;

        .contact {
          display: flex;
          align-items: center;


          i {
            color: $silver-sand;
            margin-right: 15px;
          }

          span {
            font-weight: 300;
            font-size: 17px;
            color: $silver-sand;
          }
        }
      }

      .btn-2 {
        padding: 15px 0px;
        color: $white;
        font-weight: 500;
        background-color: transparent;
        border-radius: 5px;
        letter-spacing: 2px;
        border: $blue-lagoon solid 1px;
        width: 160px;
      }
    }

    .container-card {
      display: flex;
      justify-content: space-between;
      width: 75%;
      
      .card {
        height: 100%;
        width: 30%;
        background-color: $shark;
        border-radius: 10px;
        padding: 50px;

        h3 {
          color: $white;
          font-size: 25px;
          margin-bottom: 15px;
        }

        li {
          display: flex;
          align-items: center;
          font-weight: lighter;
          list-style: none;
          margin-bottom: 10px;

          i {
            margin-right: 10px;
            color: $silver-sand;

          }

          a {
            color: $silver-sand;
            text-decoration: none;
          }
        }
      }
    }
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
    float: left;
    display: flex;
    align-items: center;
    justify-content: space-between;

    p {
      font-size: 15px;

      span {
        color: $blue-lagoon;
      }
    }
  }

  .container-bottom-right {
    height: 100%;
    width: 20%;
    float: right;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding: 20px;

    i {
      padding: 15px;
      font-size: 20px;
      background-color: darken($mid-gray, 30%);
      border-radius: 50%;
      color: darken($blue-lagoon, 18%);
    }
  }
}

.clearfix::after {
  content: "";
  clear: both;
  display: table;
}

p {
    font-weight: 300;
    font-size: 17px;
    color: $silver-sand;
}

</style>