<template>
  <button @click="clickButton"> 자식이 만든 버튼입니다. </button>
</template>

<script>
export default {
    name: "EmitChildComponent",
    emits: ["clickChildButton"],
    methods: {
        clickButton() {
            this.$emit("clickChildButton", "자식이 보낸 데이터입니다.");
        },
    },
};
</script>

<style>

</style>