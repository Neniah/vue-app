<template>
  <div class="container">
    <main>
      <component :is="selected">
        <svg class="winebottle" aria.labelledy="title" xmlns="http://www.w3.org/2000/svg" viewBox="0 155 140 300">

        </svg>
      </component>
    </main>
    <aside>
      <h4>Name your wine</h4>
      <input v-model="label" maxlength="18" />
      <div class="button-row">
        <h4>Color</h4>
        <button @click="selected ='appBlack', labelColor = '#000000'">Black Label</button>
        <button @click="selected ='appWhite', labelColor = '#ffffff'">White Label</button>
        <input type="color" v-model="labelColor" defaultValue="#ff0000">
      </div>
    </aside>
  </div>
</template>

<script>
import Black from './components/Black.vue'
import White from './components/White.vue'

export default {
  data: function () {
    return {
      selected: 'appBlack',
      label: 'Label Name'
    }
  },
  name: 'app',
  components: {
    appBlack: Black,
    appWhite: White
  }
}
</script>

<style>
  @import "./assets/style.css";
</style>
