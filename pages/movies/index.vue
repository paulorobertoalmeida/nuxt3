<script lang="ts" setup>
const query = ref("");

function search(){
    $fetch(`http://www.omdbapi.com/?apikey=3c7b1eef&s=${query.value}`)
}
</script>

<template> 
  <div>
    <form @submit.prevent="search" action="">
        <input type="text" v-model="query"/>
        <button class="bg-slate-900 m-3 p-3 rounded-lg font-semibold text-white ">Search</button>
    </form>
  </div>
</template>

<style scoped></style>
