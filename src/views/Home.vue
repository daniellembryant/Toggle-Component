<template>
  <div class="home">
    <div>
      <h3>ToggleSwitch - on/off</h3>
      <ToggleSwitch />
    </div>
    <!-- <div>
      <h1>ToggleSwitch - disabled</h1>
      <ToggleSwitch :disables="true" />
    </div> -->
  </div>
</template>

<script>
import ToggleSwitch from "@/components/ToggleSwitch.vue";

export default {
  name: "Home",
  components: {
    ToggleSwitch,
  },
};
</script>
