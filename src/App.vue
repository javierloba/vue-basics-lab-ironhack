<template>
  <div class="center">
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
  </div>
  <router-view />
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
.center {
  width: 100vw;
  display: flex;
  justify-content: center;
  gap: 40px;
}
</style>
