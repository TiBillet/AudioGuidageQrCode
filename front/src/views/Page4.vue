<template>
  <section class="zone-container overflow-hidden d-flex flex-column justify-content-center align-items-center" :style="{ backgroundImage: `url(${backgroundImagePg4})` }">
    <div class="zone-header d-flex justify-content-center align-items-center">
      <div class="d-flex flex-column justify-content-center align-items-center container-icons-vue" role="button"
           @click="goHome()">
        <BIconHouseFill class="icons-vue1  t2-5rem"/>
      </div>
    </div>

      <div class="zone-content d-flex flex-column align-items-center">
        <div class="zone-content-title d-flex flex-row  align-items-center">
          <h2>Zezer (fonnker ek zoizo)</h2>
        </div>
        <div class="zone-content-p">
          <p>Engagé par mes textes et mes choix musicaux,
            j’ai voulu dans cette oeuvre alerter en créole du danger que nous sommes,
            nous les êtres humains,
            pour les oiseaux et en général pour l’écosystème de la Terre.
          </p>
          <p>
            Les sons du jardin accompagnent ma voix et mes idées musicales s’harmonisent aux idées rythmiques des
            oiseaux
            (Merle maurice, martin).
          </p>
        </div>
      </div>

  </section>

</template>

<script setup>
import {useRouter} from 'vue-router'
// bootstrap-icons-vue - prefixed with BIcon. For example, the icon pause-fill is exported as BIconPauseFill
// icons list : https://icons.getbootstrap.com/

import {BIconHouseFill} from 'bootstrap-icons-vue'
import backgroundImagePg4 from "@/assets/images/Zezer-800x533.jpeg"

const router = useRouter()

function goHome() {
  const hauteur = document.querySelector('#app').clientHeight
  document.querySelector('#app').style.height = (2 * hauteur) + 'px'
  router.push('/')
}
</script>

<style scoped>
</style>
