<template>
  <div class="badge">
    <img :src="'/images/' + icon + '.svg'" alt="">
  </div>
</template>

<script setup>


const props = defineProps({
  icon: {
    type: String,
    required: true,
  }
})


</script>

<style>
.badge {
  width: 65px;
  height: 65px;
  background: #0098E9;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>