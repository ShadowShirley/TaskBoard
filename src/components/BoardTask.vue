<script setup lang="ts">

const props = defineProps({
  taskId: { type: String, required: true, default:"id"},
  person: {type: String, required: true, default:"Пидор"},
  taskName:{type: String, required: true, default:"Пидор"},
})

</script>

<template>
  <div class="task">
    <div class="taskInfo taskInfo__theme">
      <div>
        {{props.taskId}}
      </div>
      <div>
        {{props.person}}
      </div>
    </div>
    <div class="mainTask">
      <span class="mainTask__rule">
        {{props.taskName}}
      </span>
    </div>
  </div>
</template>

<style scoped>

.task{
  height: 16%;
  margin-bottom: 4px;
  border-radius: 4px;
  box-sizing: border-box;
  border: 1px solid #121212 ;
  min-width: max-content;
}

.taskInfo{
  display: flex;
  justify-content: space-between;
  height: 30%;
  align-items: center;
  padding: 0 8px;
  background: #202020;
}

.taskInfo__theme{
  font-size: small;
  color: #999999;
  font-family: Corbel, serif;
}

.mainTask{
  height: 70%;
  padding: 4px 4px;
  box-sizing:border-box;
  font-family: Georgia, sans-serif;
}

.mainTask__rule{
  width: 100%;
  height: 100%;
  overflow-wrap: break-word;
  display: flex;
  align-items: center;
}

</style>