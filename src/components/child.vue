<template>
  <div class="child">
    <h4>this is child Component</h4>
    <input type="text" v-model="message" @keyup="send" />
    <p>收到来自父组件的消息: {{ messageFromFather }}</p>
  </div>
</template>


<script>
export default {
  name: "Child",
  props: ["messageFromFather"], // 通过props接受父组件传递过来的消息
  data() {
    return {
      message: "",
    };
  },
  methods: {
    send() {
      this.$emit("on-receive", this.message);
    },
  },
};
</script>


<style>
</style>
