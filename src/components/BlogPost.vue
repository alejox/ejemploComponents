<script setup>
/* defineProps(['title', 'text', 'colorText', 'id']); */

defineProps({
  title: String,
  id: Number,
  body: {
    type: String,
    default: 'Sin descripción',
  },
  cambiarFavorito: Function,
});
</script>

<template>
  <div class="card">
    <div class="card-body">
      <img src="../assets/Avatar.png" alt="" />
      <h5 class="card-title">{{ id }} - {{ title }}</h5>
      <p>{{ body }}</p>
      <button @click="cambiarFavorito(title)" class="btn btn-outline-primary">
        Favorito
      </button>
    </div>
  </div>
</template>
