<template>
  <div class="container">
    <input type="checkbox" />
    <div class="toggle">
      <div class="toggle-button" v-on:click="toggle()"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ToggleSwitch",
  props: {
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    toggle: function () {
      let toggle = document.querySelector(".toggle");
      toggle.classList.toggle("active");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.container .toggle {
  position: absolute;
  top: 0;
  left: 0;
  width: 90px;
  height: 50px;
  background: #ccc;
  border-radius: 30px;
  transition: 0.4s;
}

.container .toggle.active {
  background: #6e6a6a;
}

.container .toggle.active .toggle-button {
  left: 45px;
}

.container .toggle .toggle-button {
  position: absolute;
  top: 5px;
  left: 5px;
  width: 40px;
  height: 40px;
  background: white;
  border-radius: 50%;
  cursor: pointer;
  transition: 0.4s;
}
</style>
