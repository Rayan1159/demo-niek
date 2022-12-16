<template>
  <div class="container">
    <!--
      Met @click.prevent bind je een event listener voor klik functies en gebruik je automatisch event.preventDefault();
    -->
    <button class="button" @click.prevent="toggleText">Klik op mij</button>


    <!--
      Met v-if kan je conditioneel renderen. Het maakt gebruik van javascript's if functie
      Dus als de waarde van this.showText true is laat hij de div met hallo wereld erin zien.
      Als deze false is niet en wordt de markup uit de dom verwijdert
    -->
    <div v-if="showText">
      Hallo Wereld
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    toggleText() {
      if (this.showText === false) {
        this.showText = true
      } else {
        this.showText = false;
      }
    }
  },
  data() {
    return {
      showText: false
    }
  }
}
</script>

<style scoped>
  .container {
    display: flex;
  }

  .container button {
    border: 1px solid black;
    color: white;
    background: red;
  }
</style>