<template>
  <footer class="container">
    <div class="row">
      <div class="about__company col">
        <img src="../assets/white_logo.svg" alt="white-logo" class="white--logo">
        <a href="mailto:info@savoirdessinerparis.fr">info@savoirdessinerparis.fr</a>
        <div class="about__company__medias">
          <img src="../assets/insta_icon.svg" alt="insta-icon">
          <img src="../assets/fb_icon.svg" alt="fb-icon">
          <img src="../assets/pinterest_cion.svg" alt="pinterest-icon">
          <img src="../assets/yt_icon.svg" alt="yt-icon">
        </div>
      </div>
      <div
        v-for="(workshop, index) in workshopsArr"
        :class="`about__${workshop.workshopName} col`"
        :key="index"
      >
        <div class="about__title">
          <img :src="workshop.workshopTrace" alt="">
          <h4>Atelier {{ workshop.workshopName }}</h4>
        </div>
          <p>{{ workshop.workshopAddress }}</p>
          <p>{{ workshop.workshopPhone }}</p>
      </div>
    </div>
  </footer>
</template>

<script>
import BlueTrace from "../assets/blue_trace.svg";
import RedTrace from "../assets/red_trace.svg";
import GreenTrace from "../assets/green_trace.svg";
export default {
  name: 'footer-app',
  data() {
    return {
      workshopsArr: [
        {
          workshopTrace: BlueTrace,
          workshopName: 'commerce',
          workshopAddress: '8 rue de l’Abbé Groult, 75015 Paris',
          workshopPhone: '06 65 30 88 59',
        },
        {
          workshopTrace: RedTrace,
          workshopName: 'Vaugirard',
          workshopAddress: '2 rue Petel, 75015 Paris',
          workshopPhone: '06 65 30 88 59',
        },
        {
          workshopTrace: GreenTrace,
          workshopName: 'Saint-Ambroise',
          workshopAddress: '73 boulevard Voltaire, 75011 Paris',
          workshopPhone: '06 60 75 77 73',
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  footer {
    background-color: black;
    display: flex;
    justify-content: space-around;
    height: 402px;
    align-items: center;
    color: white;

    .about__company {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: space-between;

      img {
        margin-bottom: 20px;
      }

      a {
        margin-bottom: 10px;
        text-decoration: none;
        color: white;
      }

      &__medias {
        img {
          margin-right: 8px;
        }
      }
    }

    div {
      .about__title {
        display: flex;
        align-items: center;

        img {
          margin-right: 10px;
        }
        h4 {
          margin-bottom: 0;
        }
      }

      p {
        font-size: 14px;
        margin: 0;
        text-align: left;
        margin-left: 26px;
      }
    }
  }

  @media screen and (max-width: 576px) {
    footer {
      div {
        .about__company {
          .white--logo {
            width: 42%;
          }
          a {
            font-size: 12px;
          }

          &__medias {
            display: flex;
            img {
              width: 14%;
            }
          }

        }
        div {
          .about__title {
            text-align: left;
          }
        }
        div:nth-child(2) {
          margin-bottom: 14px;
        }
      }
    }
  }

  @media screen and (min-width: 768px) {
    footer {
      margin: 0;
      max-width: 100%;
      div {
        div {
          .white--logo {
            width: 90%;
          }
        }
        .about__company__medias {
          img {
            margin-right: 2px;
          }
        }
      }
    }
  }

  @media screen and (min-width: 1200px) {
    footer {
      margin-top: 8%;
      div {
        width: 100%;
        div {
          .white--logo {
            width: 46%;
          }
          div {
            display: flex;
            justify-content: flex-start;
          }
        }
      }
    }
  }
</style>