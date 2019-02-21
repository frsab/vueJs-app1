<template lang="html">

  <section class="recherche">
    <h1>recherche Component</h1>
    <div class="home">
      <ul class="posts">
        <li v-for="post in posts.listeResultat" :key="post.nom" class="post-item">
          <h1>{{ post.nom }}</h1>
          <h1>{{ post.prenom }}</h1>
          <h1>{{ post.taille }}</h1>
          <h1>{{ post.enCouple }}</h1>
        </li>
      </ul>
    </div>
  </section>
</template>

<script lang="js">
  export default  {
    name: 'recherche',
    props: [],
    mounted() {

    },
    data() {
      return {

      }
    },
    methods: {

    },
    computed: {
      /**
       *
        * @returns {*}
       */
      posts () {
        return {
          "listeCritere": [
            "nom",
            "prenom",
            "taille",
            "enCouple"
          ],
          "listeResultat": [
            {
              "nom": "fraja",
              "prenom": "saber",
              "taille": 180,
              "enCouple": false
            },
            {
              "nom": "fraj",
              "prenom": "ALbert",
              "taille": 120,
              "enCouple": true
            },
            {
              "nom": "Dubois",
              "prenom": "martin",
              "taille": 177,
              "enCouple": false
            },
            {
              "nom": "Hollande",
              "prenom": "François",
              "taille": 180,
              "enCouple": false
            }
          ]
        }
        //this.$store.state.posts
      }
    }
}
</script>

<style scoped>
  .posts {
    list-style: none;
    text-align: left;
  }

  .post-item + .post-item {
    border-top: 1px solid rgba(0, 0, 0, 0.1);
  }
</style>
