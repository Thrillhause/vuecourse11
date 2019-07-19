<template>
  <div>
    <div id="on" @click="switched(true)" :class="{active: value}">On</div>
    <div id="off" @click="switched(false)" :class="{active: !value}">off</div>
  </div>
</template>

<script>
export default {
  props: ["value"],
  methods: {
    switched(isOn) {
      this.$emit("input", isOn);
    }
  }
};
</script>

<style>
#on,
#off {
  width: 40px;
  height: 20px;
  background-color: lightgray;
  padding: 2px;
  display: inline-block;
  margin: content-box;
  cursor: pointer;
  text-align: center;
}
#on:hover,
#on:active {
  background-color: lightgreen;
}
#off:hover,
#off:active {
  background-color: lightcoral;
}
</style>
