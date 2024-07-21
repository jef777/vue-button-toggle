<template>
  <div class="toggle-container">
    <p class="toggle-header">Toogle Button Test</p>
    <button :class="buttonClass" @click="toggleSwitch">{{ switchText }}</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      button_state: false,
    }
  },
  computed: {
    switchText() {
      return this.button_state ? 'OFF' : 'ON'
    },
    buttonClass() {
      return this.button_state ? 'button-off' : 'button-on'
    },
  },
  methods: {
    toggleSwitch() {
      this.button_state = !this.button_state
    },
  },
}
</script>
<style scoped>
.toggle-container {
  display: grid;
  justify-items: center;
}
.toggle-header {
  font-size: 20px;
  font-weight: 300;
}
button {
  padding: 10px 25px;
  font-size: 18px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.6s, color 0.6s, transform 0.3s;
}
button:hover {
  opacity: 0.8;
  transform: scale(1.1);
}
.button-on {
  background-color: #4caf50;
  color: white;
}

.button-off {
  background-color: #f44336;
  color: white;
}

button:hover {
  opacity: 0.8;
}
</style>
