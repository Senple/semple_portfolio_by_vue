<template>
  <div class="about">
    <p>人生は喜劇だ。</p>
    <h3>今までの軌跡</h3>
    <div v-for="topic in history" :key="topic.index">
      <hr />
      {{ topic.title }}
      <br />
      Date: {{ topic.date }}
      <br />
      Type: {{ topic.type }}
      <br />
      Note:{{ topic.remarks }}
    </div>
    <hr />
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      history: [
        {
          title: "第3回CJKプロジェクト・バングラデシュ派遣",
          date: "2016",
          type: "scout",
          remarks: "初めての海外ボランティア",
          index: "A0001"
        },
        {
          title: "第9回アジア太平洋地域スカウトユースフォーラム",
          date: "2018",
          type: "scout",
          remarks: "初めての国際会議",
          index: "A0002"
        },
        {
          title: "SPIN2019",
          date: "2019",
          type: "Academic",
          remarks: "初めての国際学会",
          index: "A0003"
        }
      ]
    };
  }
};
</script>
