<template>
<h2>{{msg}}</h2>
<input type="text" v-model="testvar"/>
<button @click="alertMessage"> 나를 클릭해주세요 </button>
<PropsChildComponent :to-child="toChild"/>
<div>
<EmitChildComponent @click-child-button="alertEmitMessage(msg)"/>
</div>
</template>

<script>
import PropsChildComponent from './components/PropsChildComponent.vue'
import EmitChildComponent from './components/EmitChildComponent.vue'

export default {
  name: 'App',
  components: {
    PropsChildComponent,
    EmitChildComponent
  },
  data() {
    return {
      msg: "안녕하세요",
      testvar: "",
      toChild:"부모에서 자식으로 전달된 데이터입니다."
    };
  },
  methods: {
    alertMessage() {
      alert("경고! 클릭했습니다!");
    },
    alertEmitMessage(msg) {
      alert(msg);
    },
  },
}
</script>

<style>

</style>
