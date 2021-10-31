<template>
  <section>
    <div class="content--section container">
      <div class="row">
        <img :src="sectionObj.imgSection">
        <div>
          <h3 :class="`section--${sectionObj.nameSection}`">{{ sectionObj.titleSection }}</h3>
          <img :src="sectionObj.secondaryImgSection">
          <p class="mt-3"> {{ sectionObj.descriptionSection }} </p>
          <button type="button" class="btn"> {{ sectionObj.btnContentSection }} </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'content-app-section',
  props: {
    sectionObj: {
      type: Object,
      default: () => {}
    }
  },
}
</script>

<style lang="scss" scoped>
  section {
    div {
      display: flex;
      justify-content: center;
      margin-bottom: 5%;

      div {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        width: 30%;
        text-align: left;
        margin-left: 6%;

        h3 {
          font-weight: bold;
          font-size: 30px;
          color: black;
        }

        img {
          margin: 5px 0;
        }

        button {
          border: 1px solid #000000;
          border-radius: 10px;
          color: black;
          font-weight: bold;
          margin-top: 7%;
          padding: 15px;
        }
      }
    }
  }

  @media screen and (max-width: 576px) {
    section {
      div {
        flex-direction: column;

        div {
          width: 100%;
          margin-left: 0;

          div {
            h3 {
              font-size: 19px;
            }
            button {
              padding: 8px;
              font-size: 12px;
            }
          }
        }
      }
    }
  }

  @media screen and (min-width: 768px) and (max-width: 1024px) {
    section {
      div {
        div {
          width: 100%;
          margin-left: 0;
        }
      }
    }
  }
  @media screen and (min-width: 1200px) {
    section {
      margin-bottom: 3%;
      div {
        margin: 0;
        div {
          flex-wrap: nowrap;
          flex-direction: row;
          width: inherit;
          margin-left: 38%;
          align-items: center;

          img {
            width: 90%;
          }

          div {
            display: flex;
            flex-direction: column;
            margin-left: 0;
            align-items: flex-start;
            img {
              width: 8%;
            }
            p {
              width: 45%;
              font-size: 20px;
            }
          }
        }
      }
    }

    .subscription--section {
      div {
        div {
          flex-wrap: nowrap;
          flex-direction: row-reverse;
          width: inherit;
          align-items: center;

          img {
            width: 90%;
          }

          div {
            display: flex;
            flex-direction: column;
            margin-left: 0;
            align-items: flex-start;
            img {
              width: 8%;
            }
            p {
              width: 45%;
              font-size: 20px;
            }
          }
        }
      }
    }
  }
</style>