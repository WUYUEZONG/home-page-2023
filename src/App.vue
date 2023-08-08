<script setup>
import notes from './components/note'


</script>

<template>
  <div class="board">
    <div class="content">
      <div v-for="note in notes" :key="note.id" class="item">
        <h2>{{ note.title }}</h2>
        <p>{{ note.content }}</p>
        <div class="time">{{ note.time }}</div>
      </div>
    </div>
    <div class="footer">
      <div class="ft-content">
        <div v-for="i in 5" :key="i" class="item">壹</div>
      </div>
    </div>
  </div>
</template>

<style>

@font-face {
  font-family: 'kkzt';
  src: url('/public/kuaikanshijieti.otf');
}
@font-face {
  font-family: 'dtjbt';
  src: url('/public/DingTalk JinBuTi.ttf');
}
@font-face {
  font-family: 'hmsct';
  src: url('/public/HarmonyOS_Sans_SC_Thin.ttf');
}

body {
  padding: 0;
  margin: 0;
  /* font-family: Arial, Helvetica, 'Microsoft YaHei', '黑体', sans-serif; */
}

.footer {
  /* display: flex;  */
  display: none;
  justify-content: center;
  align-items: center;
  height: 60px;
  position: fixed;
  bottom: 0;
  width: 100vw;
  /* background-color: #f8f8f8; */
}

.ft-content {
  max-width: 80vw;
  width: 1000px;
  display: flex;
  justify-content: center;
  overflow-x: auto;
  gap: 15px;
}

.ft-content .item {
  padding: 10px;
  border-radius: 6px;
}

.board {
  display: flex;
  height: calc(100vh - 60px);
  justify-content: center;
  overflow-y: auto;
  background: url('/src/assets/3.webp') no-repeat \ cover;
}

.board .content {
  max-width: 60vw;
  text-align: center;
  padding-top: calc(30vh - 100px);
}
.board .content .item {
  padding-top: 100px;
}

.board .content .item p {
  font-size: 1.2rem;
  line-height: 2.2rem;
  color: #333333;
  font-weight: 100;
}

.board .content .item .time {
  font-size: 0.9rem;
  font-weight: lighter;
  color: #999999;
}

</style>
