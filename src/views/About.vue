<template>
  <div>
    <MyButton @my-event="toggleValue()" color="black" background="orange" />
    <span class="base" :class="useTheme && 'active'">
      {{ this.useTheme }}
    </span>
  </div>
</template>

<script>
import MyButton from "@/components/MyButton.vue";
export default {
  data() {
    return {
      useTheme: false,
    };
  },
  methods: {
    toggleValue() {
      this.useTheme = !this.useTheme;
    },
  },
  components: {
    MyButton,
  },
};
</script>

<style>
.base {
  font-size: 5rem;
  color: black;
}
.active {
  color: purple;
  font-weight: bold;
}
</style>
