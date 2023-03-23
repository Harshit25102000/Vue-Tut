<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>ID</th>
          <th>Name</th>
          <th>Singer</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="song in songs" :key="song.id">
          <td>{{ song.id }}</td>
          <td>{{ song.name }}</td>
          <td>{{ song.singer }}</td>
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
      songs: [
        { id: 1, name: "Shape of You", singer: "Ed Sheeran" },
        { id: 2, name: "Blinding Lights", singer: "The Weeknd" },
        { id: 3, name: "Uptown Funk", singer: "Mark Ronson ft. Bruno Mars" },
        { id: 4, name: "All of Me", singer: "John Legend" },
        { id: 5, name: "Despacito", singer: "Luis Fonsi ft. Daddy Yankee" },
        { id: 6, name: "Closer", singer: "The Chainsmokers ft. Halsey" },
        { id: 7, name: "Thinking Out Loud", singer: "Ed Sheeran" },
        { id: 8, name: "Hello", singer: "Adele" },
        { id: 9, name: "Bad Guy", singer: "Billie Eilish" },
        { id: 10, name: "Someone Like You", singer: "Adele" },
      ],
    };
  },
};
</script>
