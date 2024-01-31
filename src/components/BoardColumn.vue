<script setup lang="ts">

import BoardTask from "@/components/BoardTask.vue";

const props = defineProps({
  name: { type: String, required: true, default:"Name"},
  comment: {type: String, required: false, default:"Я гей"}
})

</script>

<template>
  <div class="box__all box__all_theme">
    <div class="header__column">

      <div class="box__named">
        {{ props.name }}
      </div>
      <span class="box__comments">
        {{props.comment}}
      </span>
    </div>

    <div class="box__tasks">

      <board-task v-for="task in [1,2,3]"></board-task>
    </div>

    <div class="box__button">
      <button class="adderTask adderTask__theme">
        <span id="plus">
          &#43;
        </span>
        <span>
          Add item
        </span>
      </button>
    </div>
  </div>
</template>

<style scoped>
.box__all{
  flex-direction: column;
  margin-right: 8px;
  flex-wrap: nowrap;
  width: 300px;
  min-width: 20%;
  display: flex;
  box-sizing: border-box;
  height: 100%;
}

.box__all_theme{
  border: 1px solid gray;
  background: #404040;
  border-radius: 8px;
}

.header__column{
  height: 10%;
  padding: 8px 4px;
}
.box__named{
  font-weight: bolder;
  margin-bottom: 4px;
}

.box__comments{
  color: rgba(176, 176, 176, 0.91);
  box-sizing: border-box;
}
.box__tasks{
  height: 80%;
  padding: 0 3px 4px 4px;
  box-sizing: border-box;
  flex-grow: 1;
  overflow-y: auto;
}

.box__tasks::-webkit-scrollbar {
  width: 1px;
}

.box__button{
  height: 10%;
}
.adderTask__theme{
  font-weight: bold;
  font-size: medium;
}

.adderTask:hover{
  color: #a6a6a6;
  cursor: pointer;
}

.adderTask{
  height: 100%;
  width: 100%;
  text-align: center;
  background: unset;
  border-radius: 0 0 8px 8px;
  box-sizing:border-box;
  border-width: 0;
}

#plus{
  font-weight: bolder;
}

</style>