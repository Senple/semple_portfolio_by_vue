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
    <!-- <div id="outer" v-on:mouseenter="onmousein" v-on:mouseleave="onmouseout">
      外(outer)
      <p id="inner">内(inner)</p>
    </div>
    <div v-html="result"></div>-->
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
  // methods: {
  //   onmousein: function(e) {
  //     console.log(e);
  //     this.result += "Enter:" + e.target.id + "<br />";
  //   },
  //   onmouseout: function(e) {
  //     this.result += "Leave:" + e.target.id + "<br />";
  //   }
  // }
};
</script>

