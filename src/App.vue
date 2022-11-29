<template>
  <h1>Router</h1>

  <div class="div-router">
    <button @click="gotoPage('/pageA')">A</button><br>
    <button @click="gotoPage('/pageB')">B</button><br>
    <button @click="gotoPage('/pageC')">C</button><br>
  </div>

  <div class="div-router">
    <router-link to="/pageA">PageA</router-link><br>
    <router-link to="/pageB">PageB</router-link><br>
    <router-link to="/pageC">PageC</router-link><br>
    <router-link :to="{ name: 'user' , params: { userId: 1 }}">User 1</router-link><br>
  </div>
  <div class="div-router">
    <button @click="gotoUser">User 2</button>
  </div>
  <router-view></router-view>
</template>

<script>

export default {
  name: "App",
  methods: {
    gotoPage(route) {
      // this.$router.push(route);
      this.$router.replace(route);
    },
    gotoUser() {
      this.$router.push({ name: "user", params: { userId: 2 } })
    }
  }
}
</script>

<style>
.div-router {
  border: 1px solid black;
  text-align: center;
  display: flex;
  flex-flow: nowrap row;
  justify-content: space-evenly;
  padding: 30px;
}
</style>
