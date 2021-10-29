<template>
  <section>
    <content-app-atelier></content-app-atelier>
    <content-app-school :optionsArray="optionsArr"></content-app-school>
    <content-app-discover :programsArray="programsArr" ></content-app-discover>
    <!-- <content-app-courses></content-app-courses> -->
    <content-app-section :sectionObj="sectionCoursesObj"></content-app-section>
    <content-app-section :sectionObj="sectionSubscriptionObj" class="subscription--section"></content-app-section>
  </section>
</template>

<script>
import ContentAppAtelier from './ContentAppAtelier.vue';
import ContentAppSchool from './ContentAppSchool.vue';
import ContentAppDiscover from './ContentAppDiscover.vue';
// import ContentAppCourses from './ContentAppCourses.vue';
import ContentAppSection from './ContentAppSection.vue';
import PictureImg from "../../assets/portrait_img.png";
import LandscapeImg from "../../assets/header-paysage-pastel-panorama.png";
import TravelBoardImg from "../../assets/carnet-panorama.png";
import PingMapIcon from "../../assets/ping_map.svg";
import CoursesImg from "../../assets/courses_img.png";
import PencilsImg from "../../assets/pencils_img.png";
import TraceImg from "../../assets/trace_img.svg";
import PlayIcon from "../../assets/play_btn.svg";
import LikeIcon from "../../assets/like.svg";
import LevelIcon from "../../assets/level_icon.svg";
import ClockIcon from "../../assets/clock_icon.svg";

export default {
  components: {
    ContentAppAtelier,
    ContentAppSchool,
    ContentAppDiscover,
    // ContentAppCourses,
    ContentAppSection
  },
  name: 'content-app',
  data() {
    return {
      optionsArr: [
        {
          optSrcImg: PingMapIcon,
          title: "A la carte",
          description: "+ de 150 heures de cours accessibles où vous voulez, quand vous voulez.",
        },
        {
          optSrcImg: PlayIcon,
          title: "Accessible à tous",
          description: "Débutants comme confirmés, nos cours vous accompagnent pas à pas dans toutes vos envies.",
        },
        {
          optSrcImg: LikeIcon,
          title: "Sans engagement",
          description: "vous êtes libre d'annuler votre abonnement à tout moment !",
        },

      ],
      programsArr: [
        {
          imgSrc: PictureImg,
          cardTags: [
            {
              iconTag: LevelIcon,
              name: 'Tous niveaux',
              tag: 'level'
            },
            {
              iconTag: ClockIcon,
              name: '7h',
              tag: 'time'
            },
            {
              iconTag: '',
              name: '11 cours',
              tag: 'courses'
            },
          ],
          title: 'Le portrait réaliste',
          description: "Toutes les techniques pour réaliser des portraits plus vrais que nature.",
          buttonName: 'Commencer',
        },
        {
          imgSrc: LandscapeImg,
          cardTags: [
            {
              iconTag: LevelIcon,
              name: 'Tous niveaux',
            },
            {
              iconTag: ClockIcon,
              name: '7h',
            },
            {
              iconTag: '',
              name: '11 cours',
            },
          ],
          title: 'Le paysage au pastel',
          description: "Apprenez à réaliser de superbes payasages au pastel gras avec Maxime et Nathan !",
          buttonName: 'Commencer',
        },
        {
          imgSrc: TravelBoardImg,
          cardTags: [
            {
              iconTag: LevelIcon,
              name: 'Tous niveaux',
            },
            {
              iconTag: ClockIcon,
              name: '7h',
            },
            {
              iconTag: '',
              name: '11 cours',
            },
          ],
          title: 'Autour du carnet de voyage',
          description: "Apprenez à dessiner en toute liberté et à réaliser des carnets de voyages remplis de vie ! ",
          buttonName: 'Commencer',
        },
      ],
      sectionCoursesObj: {
        nameSection: 'courses',
        imgSection: CoursesImg,
        titleSection: 'Explorez vos sens artistiques',
        secondaryImgSection: TraceImg,
        descriptionSection: "Quelque soit votre niveau, découvrez des centaines de cours accessibles partout, à tout moment. Pour vous exercer pas à pas en dessin et en peinture, à votre rythme.",
        btnContentSection: 'Démarrer les cours en ligne',
      },
      sectionSubscriptionObj: {
        nameSection: 'subscription',
        imgSection: PencilsImg,
        titleSection: 'Découvrez toutes les techniques',
        secondaryImgSection: TraceImg,
        descriptionSection: "Laissez vous guider exercice par exercice, conseil par conseil, pour découvrir et pratiquer toutes les disciplines du dessin et de la peinture.",
        btnContentSection: "Je m'abonne",
      }
    }
  },
}
</script>

<style lang="scss">
.subscription--section {
  div {
    flex-direction: row-reverse;
    div {
      .section--subscription {
        width: 59%;
      }
    }
  }
}
</style>