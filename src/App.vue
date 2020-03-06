<template>
  <div class="all-champion-container">
    <Champion name="AATROX" description="THE DARKIN BLADE" />
    <Champion name="AHRI" description="THE NINE-TAILED FOX" />
    <Champion name="AKALI" description="THE ROGUE ASSASSIN" />
    <Champion name="ALISTAR" description="THE MINOTAUR" />
    <Champion name="AMUMU" description="THE SAD MUMMY" />
    <Champion name="ANIVIA" description="THE CRYOPHOENIX" />
    <Champion name="ANNIE" description="THE DARK CHILD" />
    <Champion name="APHELIOS" description="THE WEAPON OF THE FAITHFUL" />
    <Champion name="ASHE" description="THE FROST ARCHER" />
    <Champion name="AURELION SOL" description="THE STAR FORGER" />
    <Champion name="AZIR" description="THE EMPEROR OF THE SANDS" />
  </div>
</template>

<script>
import Champion from './components/Champion.vue';

export default {
  name: 'App',
  components: {
    Champion,
  },
}
</script>

<style>
body {
  background-color: lightgray;
}

.all-champion-container {
  text-align: center;
  color: #2c3e50;
}
</style>
