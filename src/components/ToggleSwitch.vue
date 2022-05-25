<template>
  <div class="container">
    <div class="toggle">
      <!-- Used the v-on click event selector -->
      <div class="toggle-button" v-on:click="toggle()"></div>
    </div>
  </div>
</template>

<script>
export default {
  //To render the component as disabled, I added a disabled prop
  name: "ToggleSwitch",
  props: {
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    //Using the querySelector method to access the toggle class and set the state to active using the built in toggle method
    toggle: function () {
      let toggle = document.querySelector(".toggle");
      toggle.classList.toggle("active");
    },
  },
};
</script>

<style>
.container {
  position: relative;
  top: 50%;
  left: 50%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.container .toggle {
  position: relative;
  width: 90px;
  height: 50px;
  background: lightgray;
  border-radius: 30px;
  transition: 0.4s;
}

.container .toggle.active {
  background: #6e6a6a;
}

.container .toggle.active .toggle-button {
  left: 50px;
}

.container .toggle .toggle-button {
  position: relative;
  top: 5px;
  left: 3px;
  width: 38px;
  height: 38px;
  background: #ffff;
  border-radius: 50%;
  cursor: pointer;
  transition: 0.4s;
}
</style>
