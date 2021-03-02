<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <div v-for="(msg, idx) in this.messages" :key="idx">
      <p :id="'c' + idx" :style="{ 'font-size': fontSize + 'rem' }">
        {{ msg }}
      </p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  data() {
    return {
      messages: ["Hello", "World!"],
      fontSize: 6,
    };
  },
  components: {
    // HelloWorld,
  },
};
</script>

<style>
#c0 {
  color: red;
}
#c1 {
  color: blue;
}
</style>