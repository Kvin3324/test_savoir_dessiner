<template>
  <section>
    <div>
      <img :src="sectionObj.imgSection">
      <div>
        <h3 :class="`section--${sectionObj.nameSection}`">{{ sectionObj.titleSection }}</h3>
        <img :src="sectionObj.secondaryImgSection">
        <p class="mt-3"> {{ sectionObj.descriptionSection }} </p>
        <button type="button" class="btn"> {{ sectionObj.btnContentSection }} </button>
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
    // imgSection: {
    //   type: String,
    //   default: ''
    // },
    // titleSection: {
    //   type: String,
    //   default: ''
    // },
    // secondaryImgSection: {
    //   type: String,
    //   default: ''
    // },
    // descriptionSection: {
    //   type: String,
    //   default: ''
    // },
    // btnContentSection: {
    //   type: String,
    //   default: ''
    // },
  }
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
</style>