<template>
  <div id="about">
    <Loading v-show="loading"></Loading>
    <div class="about" v-show="!loading">
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
  </div>
</template>

<script>
import Loading from "../components/Loading.vue";

export default {
  data: function() {
    return {
      loading: true,
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
  },
  mounted() {
    console.log("mount start");
    setTimeout(() => {
      this.loading = false;
    }, 3000);
    console.log("mounted");
  },
  components: {
    Loading
    // HelloWorld
  }
};

// CSSで作るローディングページ。
// https://digipress.info/tech/css-spinner-animation-demo/
// Vue.component('v-loading', {
//     props: {
//         text: {
//             default: 'サーバ通信中...',
//             type: String
//         },
//         show: {
//             default: false,
//             type: Boolean
//         }
//     },
//     template: '<div v-if="show"><img src="https://estatesearch.s3-ap-northeast-1.amazonaws.com/img/ajax-loader.gif" >&nbsp;<span v-text="text"></span></div>'
// });
</script>
