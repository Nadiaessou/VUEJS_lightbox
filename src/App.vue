<template>
  <div id="app">
    <div v-if="title == 'one'">
        <a :href="'https://picsum.photos/id/' + n + '/800/600'" v-lightbox v-for="n in 9">
            <img :src="'https://picsum.photos/id/' + n + '/150/150'">
        </a>
    </div>
    <section>
        <div v-if="title == 'two'">
            <a :href="'https://picsum.photos/id/' + n + '/800/600?grayscale'" v-lightbox v-for="n in 9">
                <img :src="'https://picsum.photos/id/' + n + '/150/150?grayscale'">
            </a>
        </div>
    </section>
    <lightbox></lightbox>
    <button @click="title = 'one'">ONE</button>
    <button @click="title = 'two'">TWO</button>
  </div>
</template>

<script>
import Lightbox from './components/lightbox/Lightbox.vue'

export default {
    data () {
        return {
            title: 'one'
        }
    },
  components: {
      Lightbox
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
