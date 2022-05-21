<template>
  <div class="home">
    <div>
      <h3>ToggleSwitch - on/off</h3>
      <ToggleSwitch key="default" />
    </div>
    <br />
    <div id="disabled-switch">
      <h3>ToggleSwitch - disabled</h3>
      <ToggleSwitch key="disabled" :disabled="true" />
    </div>
  </div>
</template>

<script>
import ToggleSwitch from "@/components/ToggleSwitch.vue";
// Importing the toggle switch compnent to render it on the screen
export default {
  name: "Home",
  components: {
    ToggleSwitch,
  },
};
</script>

<style scoped>
#disabled-switch {
  padding-top: 20px;
}
</style>
