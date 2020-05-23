
<template>
  <div id="contact" class="wrapper">
    <section id="header">
      <h2>Dear Semple</h2>
    </section>

    <section id="main" class="paper-format">
      <div
        id="change-font"
        v-bind:class="{wf_hannari:isActive01,
        wf_nikukyu:isActive02,
        wf_nicomoji:isActive03}"
      >こんにちは、Sempleです。abcdefghijklmnopqrsfndjhaiofhaeAFJCOAED`VJREFHDZCAS</div>
    </section>

    <section id="footer" class="sender">
      Best regardly
      <br />
      <span v-text="name" id="yourname"></span>
      <br />
      <input type="text" max-font="8" placeholder="あなたのお名前" v-model="name" />
    </section>
    <section id="option">
      <div class="font">
        <!-- <div
          id="hoge"
          v-bind:class="{wf_hannari:isActive01,
          wf_nikukyu:isActive02,
          wf_nicomoji:isActive03}"
        >hoge テキスト hoge</div>-->
        <div class="button-row">
          <button type="button" class="wf_hannari" @click="switchFont(1)" value="1">しっかり</button>
          <button type="button" class="wf_nikukyu" @click="switchFont(2)" value="2">にゃーん</button>
          <button type="button" class="wf_nicomoji" @click="switchFont(3)" value="3">やわらかい</button>
          <button type="button" @click="switchFont(0)" value="0">解除</button>
        </div>
      </div>
    </section>
    <!-- <h1>This is contact page</h1> -->
  </div>
</template>

<style scoped>
@import url(//fonts.googleapis.com/earlyaccess/hannari.css);
@import url(//fonts.googleapis.com/earlyaccess/nikukyu.css);
@import url(//fonts.googleapis.com/earlyaccess/nicomoji.css);

.wrapper {
  background: #fff;
  padding: 1em 2em;
  width: 80%;
  height: 40em;
  margin: 30px auto;
  box-shadow: 5px 5px 20px 5px rgba(0, 0, 0, 0.7);
  text-align: left;
}
#header {
  height: 10%;
  width: 100%;
}

#main {
  height: 60%;
  width: 100%;
  /* background-color: red; */
}
.paper-format {
  background-image: linear-gradient(
    180deg,
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 0) 97%,
    #ddd 97%,
    #ddd 100%
  );
  background-size: 100% 2em;
  line-height: 2;
  margin-bottom: 2em;
}

#footer {
  height: 20%;
  width: 100%;
}

.sender {
  text-align: right;
}

#option {
  width: 100%;
  height: 10%;
}
.wf_hannari {
  font-family: "Hannari";
}
.wf_nikukyu {
  font-family: "Nikukyu";
}
.wf_nicomoji {
  font-family: "Nico Moji";
}

@media screen and (max-width: 480px) {
  .button-row {
    display: block;
    width: 100%;
  }
}
</style>


<script>
export default {
  data: function() {
    return {
      name: "",
      isActive01: false,
      isActive02: false,
      isActive03: false
    };
  },
  methods: {
    switchFont: function(changenum) {
      this.isActive01 = false;
      this.isActive02 = false;
      this.isActive03 = false;

      if (changenum === 1) {
        this.isActive01 = true;
      } else if (changenum === 2) {
        this.isActive02 = true;
      } else if (changenum === 3) {
        this.isActive03 = true;
      } else if (changenum === 0) {
        return;
      }
    }
  }
};
</script>

