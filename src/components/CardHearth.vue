
<script>
export default {
  name: "CardHearth",
}
</script>

<template>
  <div class="hearth">
    <span>&hearts;</span>
  </div>
</template>

<style lang="scss" scoped>
  .hearth{
    position: absolute;
    top: 16px;
    right: 0;

    height: 50px;
    width: 50px;

    line-height: 50px;
    text-align: center;

    background-color: white;
    font-size: 20px;

    &:hover{
      color: red;
    }
  }
  
</style>