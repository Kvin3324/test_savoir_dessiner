<template>
  <section>
    <h4>Votre école d'art en accès libre et illimité</h4>
    <div class="options container">
      <div class="row">
        <div
          v-for="(option, index) in optionsArray"
          :key="index"
        >
          <img :src="option.optSrcImg">
          <h5> {{ option.title }} </h5>
          <p>{{ option.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'content-app-school',
  props: {
    optionsArray: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style lang="scss" scoped>
section {
  background-color: #F8F8F8;

  h4 {
    padding: 4% 0;
    font-weight: bold;
    font-size: 25px;
  }

  .options {
    display: flex;
    justify-content: center;
    align-items: center;

    div {
      display: flex;
      align-items: center;
      flex-direction: column;

      h5 {
        font-weight: bold;
        color: black;
        font-size: 25px;
        padding-top: 20px;
      }

      p {
        width: 80%;
      }
    }
  }
}

@media screen and (max-width: 576px) {
  section {
    h4 {
      padding-top: 10%;
      font-size: 15px;
    }

    .options {
      justify-content: initial;
      align-items: initial;
      div {
        h5 {
          font-size: 15px;
        }
      }
    }
  }
}

@media screen and (min-width: 1200px) {
  section {
    height: 407px;
    .options {
      max-width: 100%;

      div {
        flex-direction: row;
        div {
          flex-direction: column;
          width: 33.33%;

          p {
            width: 78%;
          }
        }
      }
    }
  }
}
</style>