<template>
  <section class="discover">
    <div class="discover__title">
      <h3>Découvrez et créez, tout <br/> simplement</h3>
      <div class="description--section">
        <p>
          Des centaines de cours et live à la difficulté progressive pour maitriser les bases, affirmer sa pratique et développer
          <br/> une approche personnelle du dessin.
        </p>
      </div>
    </div>
    <div class="discover__programs container-fluid">
      <div class="row">
        <div
          class="card discover__programs--card col-10 col-md-8 col-xl-3 col-xxl-3 mb-2"
          v-for="(program, index) in programsArray"
          :key="index"
        >
          <img :src="program.imgSrc" class="img--card">
          <div
            class="card--tags"
          >
          <div
            v-for="(tag, index) in program.cardTags"
            :class="`tag--${tag.tag}`"
            :key="index"
          >
            <img :src="tag.iconTag" alt="">
            <span> {{ tag.name }} </span>
          </div>
        </div>
          <h4 class="card-title"> {{ program.title }} </h4>
          <p class="card-text"> {{ program.description }} </p>
          <div class="card--button">
            <button type="button" class="btn"> {{ program.buttonName }} </button>
          </div>
        </div>
      </div>
    </div>
    <button type="button" class="btn btn--all--courses"> Voir tous les cours </button>
  </section>
</template>

<script>
export default {
  name: 'content-app-discover',
  props: {
    programsArray: {
      type: Array,
      default: () => []
    }
  },
}
</script>

<style lang="scss" scoped>
  .discover {
    margin-top: 5%;
    &__title {
      background-image: url('../../assets/yellow_trace.svg');
      background-repeat: no-repeat;
      background-position: center;
      h3 {
        color: black;
        font-size: 30px;
        font-weight: bold;
      }
    }

    &__programs {
      display: flex;

      &--card {
        background-color: #FCFCFC;
        border: 1px solid #E8E8E8;
        border-radius: 10px;
        padding: 10px;
        margin: 0 10px;
        height: 50vh;

        .img--card {
          height: 50%;
        }

        .card--tags {
          display: flex;
          align-items: center;
          font-size: 12px;
          padding: 10px 0;
          div {
            margin: 0 10px;
          }
        }

        .card-title {
          text-align: left;
          color: black;
          margin-top: 15px;
          font-weight: bold;
          font-size: 24px;
        }
        .card-text {
          font-size: 14px;
          text-align: left;
        }
        .card--button {
          display: flex;
          flex-direction: row-reverse;
          button {
            background-color: #FFE401;
            color: black;
            border-radius: 10px;
            padding: 10px;
            font-weight: bold;
          }
        }
      }
    }
    .btn--all--courses {
      background-color: #EFEFEF;
      padding: 10px;
      border-radius: 10px;
      color: black;
      font-weight: bold;
      margin: 5% 0 10% 0;
    }
  }

  @media screen and (max-width: 576px) {
    .discover {
      margin-top: 15%;
      margin-bottom: 22%;
      &__title {
        background-size: 10%;
        background-position: top;
        h3 {
          font-size: 22px;
        }
        .description--section {
          p {
            font-size: 15px;
          }
        }
      }

      .discover__programs {
        div {
          div {
            margin: 0 8px;
            h4 {
              margin-top: 0;
              font-size: 18px;
            }
            p {
              margin: 0;
              font-size: 12px;
            }
            .card--button {
              margin-top: 2px;
              button {
                padding: 6px;
                font-size: 13px;
              }
            }
          }
        }
      }
    }
  }

  @media screen and (min-width: 712px) and (max-width: 1024px) {
    .discover {
      &__title {
        background-position: left 48% top 23%;
        background-size: 5%;
      }

      &__programs {
        div {
          display: flex;
          justify-content: center;
        }
      }
    }
  }

@media screen and (min-width: 1200px) {
  .discover {
    &__title {
      background-size: 5%;
      background-position: left 49% bottom 20%;
    }
    &__programs {
      div {
        display: flex;
        justify-content: center;
        margin-top: 20px;
        .card {
          .card--button {
            justify-content: flex-start;
          }
        }
      }
    }
  }
}
</style>