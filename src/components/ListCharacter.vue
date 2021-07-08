<template>
  <div class="text center row g-5">
    <div v-for="(item, index) in listCharacter" :key="index" class="col carta">
      <Character :details="item" />
    </div>
  </div>
</template>

<script>
// import "axios";
import axios from "axios";
import Character from "@/components/Character.vue";

export default {
  name: "ListCharacter",
  components: {
    Character,
  },
  data() {
    return {
      apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
      listCharacter: [],
    };
  },
  created() {
    this.getCharacters();
  },
  methods: {
    getCharacters() {
      axios
        .get(this.apiURL)
        .then((res) => {
          // Creo un array di oggetti che è uguale all'array dell'API che mi sono andato a collegare
          // console.log(res.data);
          this.listCharacter = res.data.response;
          console.log(this.listCharacter);
        })
        .catch((error) => {
          console.log("Errore:", error);
        });
    },
  },
};
</script>

<style scoped lang="scss" >
.text {
  width: 70%;
}
.carta {
  padding-bottom: 40px;
  max-height: 600px;
  cursor: pointer;
  &:hover {
    z-index: 5;
  }
}
</style>