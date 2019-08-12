<template>
  <div class="online-status">
    <div class="online" v-if="online">
      <span class="light"></span>
      <p>A staff is online and available</p>
    </div>

    <div class="offline" v-if="!online">
      <span class="light"></span>
      <p>A staff is not currently online</p>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      online: true
    }
  }
}
</script>

<style>
.online-status {
  background: #eee;
  border: 1px dashed #ddd;
  display: block;
  padding: 10px;
}
p{
  display: inline-block;
  margin: 0;
  color: #555;
}
.light{
  display: inline-block;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  margin-right: 10px;
}
.online .light{
  background: limegreen;
}
.offline .light{
  background: crimson;
}
</style>
