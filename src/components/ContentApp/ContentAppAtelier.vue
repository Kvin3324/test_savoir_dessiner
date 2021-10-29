<template>
  <section>
    <div>
      <div>
        <h4>L'atelier online</h4>
        <div>
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
</style>