<script setup>
import { ref } from 'vue'

let qty = ref(2)

function addValue() {
  qty.value++
  console.log(qty)
}

function restValue() {
  if (qty.value > 0) {
    qty.value--
  }
  console.log(qty)
}
</script>

<template>
  <div class="wrapper">
    <div class="profile">
      <div class="ballon" v-show="qty > 0">{{ qty }}</div>
    </div>
    <div class="button-wrapper">
      <div class="button" @click="restValue">-</div>
      <div class="button" @click="addValue">+</div>
    </div>

    <div v-if="qty > 0">Me escribieron 😎</div>
    <div v-else>Nadie me escribe 😢</div>
  </div>
</template>

<style scoped>
.profile {
  background-image: url('https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/344e232b-060f-4bd2-a307-725eddf90c2b/d4u2u8z-c6172afd-c743-420b-a1a5-5607c182152a.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzM0NGUyMzJiLTA2MGYtNGJkMi1hMzA3LTcyNWVkZGY5MGMyYlwvZDR1MnU4ei1jNjE3MmFmZC1jNzQzLTQyMGItYTFhNS01NjA3YzE4MjE1MmEuanBnIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.uD44fJNfRtasD7b6BVyXYPBdD_OSR_YP_1QE9Xs4wZk');
  background-size: cover;
  position: relative;
  background-color: orange;
  width: 160px;
  height: 160px;
  margin: 0 auto;
  border-radius: 100%;
}
.wrapper {
  padding-top: 18px;
  background-color: #025e73;
  width: 60%;
  border-radius: 12px;
  margin: 0 auto;
  overflow: hidden;
}
.ballon {
  width: 32px;
  height: 32px;
  background-color: #8c1f28;
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  position: absolute;
  top: 0;
  right: 0;
}
.button-wrapper {
  text-align: center;
  margin-top: 18px;
  margin-bottom: 16px;
}
.button {
  background-color: #00939c;
  display: inline-block;
  padding: 4px 0;
  border-radius: 4px;
  width: 32px;
  margin: 0 8px;
}
.button:hover {
  cursor: pointer;
  background-color: #10abb4;
}
</style>
