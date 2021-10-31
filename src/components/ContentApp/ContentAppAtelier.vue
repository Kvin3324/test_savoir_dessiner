<template>
  <section>
    <div class="container">
      <div class="row">
        <h4>L'atelier online</h4>
        <div class="col">
          <h2>Apprenez le dessin et la peinture depuis chez vous</h2>
          <button>S'inscrire gratuitement</button>
        </div>
      </div>
      <img src="../../assets/first_video.png" alt="first-video">
    </div>
  </section>
</template>

<script>
export default {
  name: 'content-app-atelier',
}
</script>

<style lang="scss" scoped>
section {
  display: flex;
  justify-content: center;
  margin-top: 1%;
  background-color: #FFE401;
  height: 60vh;
  background-image: url('../../assets/white_trace.svg');
  background-repeat: no-repeat;
  background-position: left 11% bottom 55%;;
  div {
    display: flex;
    align-items: center;
    div {
      display: flex;
      flex-direction: column;
      text-align: left;
      width: 57%;

      h4 {
        font-size: 18px;
        font-weight: bold;
        text-align: center;
        margin-right: 31%;
      }
      div {
        display: flex;
        align-items: flex-start;
        h2 {
          font-weight: bold;
          font-size: 52px;
          color: black;
        }
        button {
          font-weight: bold;
          padding: 20px;
          border-radius: 10px;
          background-color: black;
          color: white;
        }
      }
    }
  }
}

@media only screen and (max-width: 575px) {
  section {
    margin-top: 22%;
    background-size: 20%;
    background-position: left 21% bottom 28%;
    div {
      flex-direction: column-reverse;
      div {
        width: 87%;
          h4 {
            font-size: 12px;
            padding-top: 12px;
            margin-bottom: 0;
            margin-right: 35%;
          }
        div {
          padding: 10px 0;
          h2 {
            font-size: 23px;
          }
          button {
            padding: 8px;
            font-size: 10px;
          }
        }
      }
      img {
        width: 88%;
      }
    }
  }
}

@media screen and (max-width: 812px) {
  section {
    margin-top: 6%;
    div {
      justify-content: center;
    }
  }
}

@media screen and (min-width: 768px) and (max-width: 1024px) {
  section {
    background-position: left 11% bottom 25%;
    background-size: 10%;
    div {
      display: flex;
      flex-direction: column-reverse;
      div {
        width: 100%;
        align-items: initial;
        h4 {
          text-align: left;
          margin-left: 30px;
        }
        div {
          h2 {
            font-size: 33px;
          }
        }
      }
      img {
        width: 78%;
      }
    }
  }
}

@media screen and (min-width: 1200px) {
  section {
    background-position: left 15% bottom 76%;
    background-size: 9%;
    div {
      div {
        flex-direction: column;
        width: 100%;
        position: relative;

        h4 {
          margin-right: 0;
          position: absolute;
          bottom: 100%;
          right: 20%;
        }
        div {
          h2 {
            font-size: 60px;
            margin-bottom: 2%;
          }
        }
      }
    }
  }
}

</style>