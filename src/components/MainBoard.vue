<script setup lang="ts">

</script>

<template>
  <div class="section">
    <div class="adderColumn__settings">
      <button class="adderColumn adderColumn__theme">
        +
      </button>
  </div>

  </div>
</template>

<style scoped>
.section{
  display: flex;
  flex-direction: row;
  justify-content: center;
  height: 600px;
  flex-wrap: nowrap;
  align-items: center;
}
.adderColumn:hover{
  color: #494949;
  cursor: pointer;
}
.adderColumn__settings{
  display: flex;
  align-content: center;
  padding: 0 28px;
}

.adderColumn__theme{
  font-weight: bolder;
  font-size: large;
  background: #999999;
  border-width: 1px;
}
</style>