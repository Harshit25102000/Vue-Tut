
import HelloWorld from './components/HelloWorld.vue';


import { RouterLink, RouterView } from 'vue-router'




 
<template>
  <div>
    <p>Submitted By Harshit Singh PRN-20070122050</p>
    <table >
      <thead>
        <tr>
          <th style="color:blue;">ID</th>
          <th style="color:blue;">Name</th>
          <th style="color:blue;">Singer</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="song in songs" :key="song.id">
          <td style="color:aqua;">{{ song.id }}</td>
          <td style="color:aqua;">{{ song.name }}</td>
          <td style="color:aqua;">{{ song.singer }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Create object array songs
      books: [
        { id: 1, name: "Shape of You", author: "Ed Sheeran",pages:"20",status="issued" },
        { id: 2, name: "Blinding Lights", author: "The Weeknd",pages:"20",status="issued" },
        { id: 3, name: "Uptown Funk", author: "Mark Ronson ft. Bruno Mars",pages:"20",status="issued" },
        { id: 4, name: "All of Me", author: "John Legend" ,pages:"20",status="issued"},
        { id: 5, name: "Despacito", author: "Luis Fonsi ft. Daddy Yankee",pages:"20",status="issued" },
        { id: 6, name: "Closer", author: "The Chainsmokers ft. Halsey",pages:"20",status="issued" },
        { id: 7, name: "Thinking Out Loud", author: "Ed Sheeran",pages:"20",status="issued" },
        { id: 8, name: "Hello", author: "Adele" ,pages:"20",status="issued"},
        { id: 9, name: "Bad Guy", author: "Billie Eilish",pages:"20",status="issued" },
        { id: 10, name: "Someone Like You", author: "Adele",pages:"20",status="issued" },
      ],
    };
  },
};
</script>
 


<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
