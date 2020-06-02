<template>
  <div id="about">
    <Loading v-show="loading"></Loading>
    <div id="container" class="about" v-show="!loading">
      <h5 id="header" class="header">今までの軌跡</h5>
      <div id="card1" class="scout card">
        <span class="icon">icon</span>
        <p class="card-left card-text">
          2016
          <br />3rdCJK-Bangladesh Project
          <br />Bangladesh
          <br />初めての海外ボランティア
        </p>
      </div>
      <p>人生は喜劇だ。</p>
      <div id="card2" class="scout card">
        <!-- <p class="card-left">2018</p> -->
        <span class="icon">icon</span>
        <p class="card-left card-text">
          2018
          <br />9thAPR Scout Youth Forum
          <br />Philippine
          <br />初めての国際会議
        </p>
      </div>

      <div id="card3" class="card">
        <span class="icon">icon</span>
        <p class="card-left card-text">
          2019
          <br />SPIN2019
          <br />India
          <br />初めての国際学会
        </p>
      </div>

      <div id="card4"></div>

      <!-- <div v-for="topic in history" :key="topic.index">
        <p></p>
        {{ topic.title }}
        <br />
        Date: {{ topic.date }}
        <br />
        Type: {{ topic.type }}
        <br />
        Note:{{ topic.remarks }}
      </div>
      <hr />-->
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
          // title: "第3回CJKプロジェクト・バングラデシュ派遣",
          title: "3rdCJK-Bangladesh Project",
          date: "2016",
          type: "scout",
          remarks: "初めての海外ボランティア",
          index: "A0001"
        },
        {
          // title: "第9回アジア太平洋地域スカウトユースフォーラム",
          title: "9thAPR Scout Youth Forum",
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
      console.log("Loading...");
    }, 3000);
    console.log("mounted");
    // this.loading = false;
  },

  components: {
    Loading
  }
};

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

<style scoped>
#container {
  display: grid;
  grid-template-columns: 50vw 50vw;
  grid-template-rows: 10vh 22.5vh 22.5vh 22.5vh 22.5vh;
  width: 100vw;
  height: 100vh;
  /* grid-template-areas:
    "header header"
    "card1 word1"
    "word2 card2"
    "card3 word3"
    "word4 card4"; */
}

#header {
  grid-row: 1/2;
  grid-column: 1/3;
  background: #8f8;
}
#card1 {
  grid-row: 2/3;
  grid-column: 1/2;
  background: #8f8;
}
#card2 {
  grid-row: 3/4;
  grid-column: 2/3;
  background: #8f8;
}
#card3 {
  grid-row: 4/5;
  grid-column: 1/2;
  background: #8f8;
}
p {
  font-size: 20px;
}

.header {
  padding: 1%;
  margin: 1em 8em;
}

.card {
  padding: 2%;
  margin: 0.5em 8em;
}

.card-left {
  text-align: left;
  /* vertical-align: bottom; */
}
/* .card-text {
  padding-top: 5%;
} */

/* スマホ版のCSSを設定 */
@media only screen and (max-width: 480px) {
  p {
    font-size: 5px;
  }
  .header {
    padding: 4%;
    margin: 1.2em 1.5em;
  }
  .card {
    padding: 5%;
    margin: 3em 1em;
  }
  /* .card-text {
    padding-top: 10%;
  } */
}
</style>
