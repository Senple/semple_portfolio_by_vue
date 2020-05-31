<template>
  <div class="skill">
    <p>
      {{ year }}年から、
      <span class="pythonColor">Python</span>を書いています。
      <br />スタートアップへ就職してからは、
      <span class="vueColor">vue.js</span>と
      <span class="awsColor">AWS</span>など
      <span class="pythonColor">Python</span>以外もさわり始めています。
    </p>
  </div>
</template>


<style scoped>
.pythonColor:hover {
  background-color: rgba(62, 124, 173, 1);
}
.vueColor:hover {
  background-color: rgba(78, 192, 141, 1);
}
.awsColor:hover {
  background-color: rgba(248, 153, 29, 1);
}
</style>


 <script>
export default {
  data: function() {
    return {
      year: 2018,
      result: ""
    };
  }
};
</script>

