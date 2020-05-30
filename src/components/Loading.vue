<template>
  <div class="box">
    <!-- type1 〜 type8 はお好みで -->
    <div class="spinner type1">
      <span>Loading...</span>
    </div>
  </div>
</template>



<style scoped>
/* ローディングアニメーション */
.spinner {
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  -webkit-transform-origin: center;
  transform-origin: center;
  width: 120px;
  height: 120px;
}

/* Loading テキスト */
.spinner span {
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  font-size: 12px;
}

/* Spinner 2 */
.type2 {
  border-radius: 50%;
  border-width: 4px;
  border-style: solid;
  border-color: #fff transparent;
  animation: spinner1_1 2.2s infinite linear forwards;
}

.spinner.type2 {
  border-radius: 50%;
  border-width: 4px;
  border-style: solid;
  border-color: #fff transparent;
  -webkit-animation: spinner1_1 2.2s infinite linear forwards;
  animation: spinner1_1 2.2s infinite linear forwards;
}
.spinner.type2::before {
  content: "";
  position: absolute;
  top: 4px;
  left: 4px;
  right: 4px;
  bottom: 4px;
  border-radius: 50%;
  border-width: 4px;
  border-style: solid;
  border-color: #fff transparent;
  animation: spinner1_2 0.8s infinite linear forwards reverse;
}
.spinner.type2 span {
  animation: spinner_loading_text 2.2s infinite linear forwards reverse;
}

span {
  animation: spinner_loading_text 2.2s infinite linear forwards reverse;
}
@-webkit-keyframes spinner_loading_text {
  0% {
    opacity: 1;
    -webkit-transform: translate(-50%, -50%) rotate(0deg);
    transform: translate(-50%, -50%) rotate(0deg);
  }
  50% {
    opacity: 0;
    -webkit-transform: translate(-50%, -50%) rotate(180deg);
    transform: translate(-50%, -50%) rotate(180deg);
  }
  100% {
    opacity: 1;
    -webkit-transform: translate(-50%, -50%) rotate(360deg);
    transform: translate(-50%, -50%) rotate(360deg);
  }
}
@keyframes spinner_loading_text {
  0% {
    opacity: 1;
    -webkit-transform: translate(-50%, -50%) rotate(0deg);
    transform: translate(-50%, -50%) rotate(0deg);
  }
  50% {
    opacity: 0;
    -webkit-transform: translate(-50%, -50%) rotate(180deg);
    transform: translate(-50%, -50%) rotate(180deg);
  }
  100% {
    opacity: 1;
    -webkit-transform: translate(-50%, -50%) rotate(360deg);
    transform: translate(-50%, -50%) rotate(360deg);
  }
}
</style>