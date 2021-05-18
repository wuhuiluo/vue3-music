<template>
  <div class="father">
    <h3>this is father component</h3>
    <input type="text" v-model="message" />
    <p>收到来自子组件的消息 {{ messageFromChild }}</p>
    <Child @on-receive="receive" :messageFromFather="message" />
  </div>
</template>


<script>
import Child from "./child.vue";
export default {
  data() {
    return {
      message: "",
      messageFromChild: "",
    };
  },
  components: {
    Child,
  },
  methods: {
    receive(msg) {
      console.log(msg);
      // 接受子组件的信息，并将其赋值给messageFromChild
      this.messageFromChild = msg;
    },
  },
};
</script>


<style>
</style>
