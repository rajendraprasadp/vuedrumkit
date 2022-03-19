<template>
  <div>
    <h1>Drumkit 123</h1>
    <h5>Press any key below on keyboard or through mouse</h5>
    <div class="keys">
      <Key v-for="(key, i) in keys" :sound="key" :key="i" />
    </div>
  </div>
</template>

<script>
import Key from "./components/Key.vue";
export default {
  name: "App",
  data() {
    return {
      keys: [
        {
          name: "boom",
          audio: require("./assets/sounds/boom.wav"),
          letter: "A",
        },
        {
          name: "clap",
          audio: require("./assets/sounds/clap.wav"),
          letter: "S",
        },
        {
          name: "hihat",
          audio: require("./assets/sounds/hihat.wav"),
          letter: "D",
        },
        {
          name: "kick",
          audio: require("./assets/sounds/kick.wav"),
          letter: "F",
        },
        {
          name: "openhat",
          audio: require("./assets/sounds/openhat.wav"),
          letter: "G",
        },
        {
          name: "snare",
          audio: require("./assets/sounds/snare.wav"),
          letter: "H",
        },
        {
          name: "ride",
          audio: require("./assets/sounds/ride.wav"),
          letter: "J",
        },
        {
          name: "tink",
          audio: require("./assets/sounds/tink.wav"),
          letter: "K",
        },
        {
          name: "tom",
          audio: require("./assets/sounds/tom.wav"),
          letter: "L",
        },
      ],
    };
  },
  components: { Key },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.keys {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
