<template>
      <div class="m-auto">
        <h1 class="text-2xl text-center">DC Heroes {{heroesCount}}</h1>
        <ul>
          <li class="flex justify-between" v-for="(hero, index) in dcHeroes" :key="hero.name">
            <div>{{ hero.name }}</div>
            <button @click="removeHero(index)"> x</button>
          </li>
        </ul>
        <form class="mt-10" @submit.prevent="addHero">
          <input class="border rounded" v-model.trim="newHero" placeholder="Type Hero name here">
          <button class="border rounded bg-gradient-to-r from-red-700 to-pink-500 text-white" type="submit">Add Hero</button>
        </form>
      </div>
</template>

<script>
export default {
    data() {
        return {
            newHero: "",
            dcHeroes: [
                {name:'SuperGirl'},
                {name:'Flash'},
                {name:'SuperMan'},
                {name:'Batman'},
                {name:'Arrow'}
            ],
        } 
    },

methods: {
    addHero() {
      if(this.newHero !== '') {
        this.dcHeroes.push({name: this.newHero})
        this.newHero = ''
      }
    },

    removeHero(index) {
      this.dcHeroes = this.dcHeroes.filter((hero, i) => i !== index)
    },

  },  
  computed: {
    heroesCount() {
      return this.dcHeroes.length
    },
  },


}

 

</script>
    
<style>

</style>