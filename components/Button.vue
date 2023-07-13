<template>
  <button
    @click="$emit('selected', icon)"
    class="css-nl00rp-ResponsiveButtonSection etitymn3 e3ku2yi0 css-pu5jf8-StyledButton-Section e1qpnu2f0"
  >
    <span class="flexer">
      <img
        v-if="icon"
        class="step-icon"
        :src="require(`~/assets/${icon}.png`)"
        width="25%"
      />
      <span class="css-1sqtaec-ButtonSpan e3ku2yi2">{{ text }}</span></span
    ><i
      width="20"
      height="15"
      size="64"
      color="#bcbcbc"
      fill="initial"
      class="e3ku2yi1 css-qjfwn2-IconWrapper-ButtonIcon ey9r1py0"
      name="IconFrontChevron"
      ><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 10 17">
        <path
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-width="2"
          d="M1.255 16.13l7.243-7.244M1 1.256L8.244 8.5"
        ></path>
      </svg>
    </i>
  </button>
</template>
<script>
export default {
  props: {
    icon: {
      type: String,
      default: "",
    },
    text: {
      type: String,
      default: "",
    },
  },
};
</script>
<style scoped lang="scss">
.step-icon {
  margin: 0 1rem;
}
/*! CSS Used from: Embedded */
* {
  text-decoration: none;
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: Lato, "Helvetica Neue", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
}
.flexer {
  display: flex;
  align-items: center;
}
/*! CSS Used from: Embedded */
@media (min-width: 576px) {
  .css-nl00rp-ResponsiveButtonSection {
    padding: 15px 20px;
    width: 100%;
  }
}
/*! CSS Used from: Embedded */
.css-pu5jf8-StyledButton-Section {
  min-width: 288px;
  font-size: 18px;
  padding: 15px;
  border: 1px solid rgb(222, 222, 222);
  color: rgb(68, 68, 68);
  background: rgb(255, 255, 255) !important;
  text-align: left;
  border-radius: 8px;
  font-family: Lato, "Helvetica Neue", Helvetica, Arial, sans-serif;
  box-sizing: border-box;
  min-height: 40px;
  vertical-align: middle;
  cursor: pointer;
  white-space: nowrap;
  line-height: 1.42857;
  will-change: transform;
  transform: scale(1);
  -webkit-font-smoothing: antialiased;
  transition: transform 300ms ease-out 0s, background 300ms ease-out 0s,
    -webkit-transform 300ms ease-out 0s;
  text-decoration: none;
  height: auto;
  margin: 16px auto;
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  -webkit-box-pack: justify;
  justify-content: space-between;
  max-width: 348px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 8px 0px;
}
.css-pu5jf8-StyledButton-Section:hover {
  background-color: rgb(255, 255, 255);
  border-color: rgb(68, 68, 68);
  box-shadow: rgb(68, 68, 68) 0px 0px 0px 1px;
}
.css-pu5jf8-StyledButton-Section:active,
.css-pu5jf8-StyledButton-Section:focus {
  border: 1px solid rgb(68, 68, 68);
  box-shadow: rgb(68, 68, 68) 0px 0px 0px 1px;
}
.css-pu5jf8-StyledButton-Section:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
.css-pu5jf8-StyledButton-Section:hover,
.css-pu5jf8-StyledButton-Section:focus {
  outline: 0px !important;
}
.css-pu5jf8-StyledButton-Section:active {
  transform: scale(0.9);
  transition-duration: 300ms;
}
.css-7un9f3-IconWrapper-ButtonIcon {
  display: inline-flex;
  box-sizing: border-box;
  width: 42px;
  height: 42px;
  color: rgb(188, 188, 188);
  fill: initial;
  vertical-align: middle;
}
.css-7un9f3-IconWrapper-ButtonIcon svg {
  display: inline-flex;
  box-sizing: border-box;
  width: 42px;
  height: 42px;
  color: rgb(188, 188, 188);
  fill: initial;
}
.e3ku2yi1 + .css-1sqtaec-ButtonSpan {
  margin-left: 15px;
  display: inline-flex;
  white-space: normal;
  word-break: break-word;
  max-width: 180px;
}
@media (max-width: 768px) {
  .e3ku2yi1 + .css-1sqtaec-ButtonSpan {
    max-width: 180px;
  }
}
.css-qjfwn2-IconWrapper-ButtonIcon {
  display: inline-flex;
  box-sizing: border-box;
  width: 20px;
  height: 15px;
  color: rgb(188, 188, 188);
  fill: initial;
  vertical-align: middle;
}
.css-qjfwn2-IconWrapper-ButtonIcon svg {
  display: inline-flex;
  box-sizing: border-box;
  width: 20px;
  height: 15px;
  color: rgb(188, 188, 188);
  fill: initial;
}
/*! CSS Used fontfaces */
@font-face {
  font-family: "Lato";
  font-style: italic;
  font-weight: 400;
  src: url("https://euwprd-cdn-w.care.com/assets/lato-italic-latin-ext-adad06528af4302d1612ab1b2a36ae7f.woff2")
    format("woff2");
}
@font-face {
  font-family: "Lato";
  font-style: italic;
  font-weight: 400;
  src: url("https://euwprd-cdn-w.care.com/assets/lato-italic-latin-8ebe320f3d03440cef5e87875e3f38a8.woff2")
    format("woff2");
}
@font-face {
  font-family: "Lato";
  font-style: normal;
  font-weight: 300;
  src: url("https://euwprd-cdn-w.care.com/assets/lato-thin-latin-ext-f0f8f93fabb6ff890ec4603e72d551f8.woff2")
    format("woff2");
}
@font-face {
  font-family: "Lato";
  font-style: normal;
  font-weight: 300;
  src: url("https://euwprd-cdn-w.care.com/assets/lato-thin-latin-5589842cc46587294240b2cc0c7a0f98.woff2")
    format("woff2");
}
@font-face {
  font-family: "Lato";
  font-style: normal;
  font-weight: 400;
  src: url("https://euwprd-cdn-w.care.com/assets/lato-latin-ext-a9c7c20a417a34a9d017176b563cfb64.woff2")
    format("woff2");
}
@font-face {
  font-family: "Lato";
  font-style: normal;
  font-weight: 400;
  src: url("https://euwprd-cdn-w.care.com/assets/lato-latin-e7e52c955aa33e618baf437a16539524.woff2")
    format("woff2");
}
@font-face {
  font-family: "Lato";
  font-style: normal;
  font-weight: 700;
  src: url("https://euwprd-cdn-w.care.com/assets/lato-bold-latin-ext-5bc5e06e2c36c36d2afbb4321dfc8697.woff2")
    format("woff2");
}
@font-face {
  font-family: "Lato";
  font-style: normal;
  font-weight: 700;
  src: url("https://euwprd-cdn-w.care.com/assets/lato-bold-latin-69b28056044be6438ce7e5214c66ba82.woff2")
    format("woff2");
}
</style>
