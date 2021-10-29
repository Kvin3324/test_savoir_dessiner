<template>
  <footer>
    <div class="about__company">
      <img src="../assets/white_logo.svg" alt="white-logo">
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
      :class="`about__${workshop.workshopName}`"
      :key="index"
    >
      <div class="about__commerce--title">
        <img :src="workshop.workshopTrace" alt="">
        <h4>{{ workshop.workshopName }}</h4>
      </div>
        <p>{{ workshop.workshopAddress }}</p>
        <p>{{ workshop.workshopPhone }}</p>
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
  }
</style>