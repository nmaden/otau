<template>
  <div id="app" @click="hideMenu">
     <div class="menuBlock" @click="menuBlock">
     </div>
     <router-view></router-view>
  </div>
</template>



<script>
// Import styles project
import './assets/style/color.css';
import './assets/style/fonts.css';
 
export default {
  name: 'app',
  methods: {
      
      hideMenu() {
          this.$emit('hideNotif');
          this.$emit('hideApps');
          this.$emit('hideLogout');
      },
      menuBlock() {
          var menu = document.querySelector('.sidebar');
          var opM = document.querySelector('.menuBlock'); 
          menu.style.transition = ".5s";
          menu.style.left = "-320px";
          opM.style.display = "none";
      },
  },
}
</script>

<style lang="scss"> 
* {
  color: var(--main-project-color);
  font-family: Lato;
  margin: 0;
  padding: 0;
}
.notif__wrap {
  display: flex;
  flex-wrap: wrap;
}
 .sign__page {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      .sign__top_image {
          font-size: 40px;
          margin-bottom: 20px;
          color: var(--main-kenes-blue);
      }
      @media only screen and (max-width: 764px) {
        width: 100%;
      }
      .sign__page__title {
        font-weight: bold;
        font-size: 26px;
        margin-bottom: 20px;
        color: #333;
      }
      .sign__page__block {
        display: flex;
        flex-direction: column;
        input {
            border-radius: 30px;
            border:1px solid  var(--main-kenes-blue);
            outline: none;
            width: 100%;
            padding: 20px;
            margin-bottom: 20px;
            @media only screen and (max-width: 764px) {
                width: 90%;
            }
        }
        ::placeholder {
          color: #333;
        }
        a {
            text-align: center;
            text-decoration: underline;
            cursor: pointer;
            text-transform: uppercase;
            width: 100%;
            outline: none;
            border: none;
            color: var(--main-kenes-blue);
            padding: 20px;
            @media only screen and (max-width: 764px) {
                width: 90%;
            }
        }
        button {
          cursor: pointer;
          text-transform: uppercase;
          width: 100%;
          border-radius: 30px;
          outline: none;
          border: none;
          background-color:var(--main-kenes-blue);
          padding: 20px;
          margin-bottom: 10px;
          @media only screen and (max-width: 764px) {
             width: 90%;
          }
          p {
            color: white;
            font-weight: bold;
          }
        }
        button:hover {
          background-color: #285bb6;
        }
      }
      
    }
body {
  background: var(--main-user-page-color);
}

.menuBlock {
   width: 100%;
   height: 100%;
   position: fixed;
   top: 0;
   background: rgba(0, 0, 0, 0.5);
   z-index: 999;
   display: none;
}




    .notif__column {
        display: flex;
        flex-direction: column;
    }
    .notif__row {
        display: flex;
        flex-direction: row;
    }
    .notif__ac {
        align-items: center;
    }
    .notif__jb {
        justify-content: space-between;
    }
    .notif__100 {
        width: 100%;
    }
    .notif__mb__xs {
        margin-bottom: 10px;
    }
     .notif__mb__s {
        margin-bottom: 20px;
    }
    .notif__mr__xs {
        margin-right: 5px;
    }
    .notif__mr__s {
        margin-right: 10px;
    }
    .notif__mr__l {
        margin-right: 20px;
    }
    .notif__fs {
        align-items: flex-start;
    }

    .notif__modal {
            display: flex;
            justify-content: center;
            align-items: center;
            position: fixed;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
            .notif__title {
              
                font-size: 20px;
                color: gray;
                align-self: center;
                margin-bottom: 20px;
                color: var(--main-kenes-blue);
                text-transform: uppercase;
            }
            .notif__modal__form {
                background: white;
                align-self: center;
                align-items: center;
                justify-content: center;
                padding: 20px;
                width: 80%;
                border-radius: 10px;
            }
            button,a {
                    text-align: center;
                    text-decoration: none;
                    width: 70%;
                    border-radius: 20px;
                    padding: 15px;
                    border: none;
                    outline: none;
                    background: var(--main-kenes-blue);
                    color: white;
            }
            a {
                width: 60%;
                background: #ccc;
            }
            input,select {
                background: #ccc;
                color:white;
                padding: 7px;
                border-radius: 20px;
                border: none;
                outline: none; 
                padding-left: 10px;
                width: 100%;

            }
            .notif__submit {
               background: #683fcc;
            }
            .notif__modal__input {
              border-radius: 20px;
              padding: 15px;
              background: white;
              border: 1px solid #ccc;
              color:#683fcc;
            }
            .notif__label {
              align-self: flex-start;
              color: gray;
              font-size: 16px;
            }
            .notif__title2 {
              font-size: 20px;
              color: #683fcc;
              font-weight: bold;
            }
    }
</style>
