<template>
  <div id="app">
    <daylist />
  </div>
</template>

<script>
import daylist from "./components/dayList";

export default {
  name: "App",
  components: {
    daylist,
  },
};
</script>

<style>
* {
  background: #bea8aa;
}
</style>
