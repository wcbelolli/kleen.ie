<template>
  <main class="steps-container">
    <div class="w3-border">
      <div class="w3-grey" :style="`height: 5px; width: ${progress}`"></div>
    </div>
    <div style="text-align: center">
      <h3
        class="css-1pd8dxv-ResponsiveH3 etitymn2 css-12iu88i-Elem-BaseTypography e1sl5nsj1"
        color="#444444"
        display="block"
        font-size="18"
        letter-spacing="normal"
        font-weight="normal"
      >
        <span v-if="eircode"
          >Hi there! Why don't you tell us about yourself?</span
        >
        <span v-else>Hi there! Where in Dublin are you located?</span>
      </h3>
    </div>
    <div v-if="requestEircode" class="eircode" style="margin: 0 1rem">
      <div class="field field__full-width postcode__input" data-v-5f57e4d5="">
        <div class="field__input" data-v-5f57e4d5="">
          <input
            id="postcode-input"
            type="text"
            v-model="eircode"
            data-v-5f57e4d5=""
            @keyup.enter="submit"
          />
          <label for="postcode-input" data-v-5f57e4d5="">Enter Eircode</label>
          <span class="field__icon" data-v-5f57e4d5=""
            ><span
              id="postcode-status-icon"
              class="icon icon--magnifying-glass"
              data-v-5f57e4d5=""
              @click="submit"
            ></span
          ></span>
        </div>
        <div class="submit-eircode" style="margin-top: 1rem">
          <div class="how-it-works__btn-wrapper" data-v-95337e7c="">
            <button
              @click="submit"
              class="btn btn--primary btn--medium"
              data-v-95337e7c=""
            >
              Continue
            </button>
          </div>
        </div>
      </div>
    </div>
    <div v-else class="buttons">
      <Button icon="household" text="I'm a household" @selected="step" />
      <Button icon="business" text="I'm a business" @selected="step" />
    </div>
  </main>
</template>
<script>
export default {
  data() {
    return {
      eircode: "",
      requestEircode: true,
      cleaningFor: "",
      progress: "50%",
    };
  },
  methods: {
    step(value) {
      this.cleaningFor = value;
      //   if (this.cleaningFor === "household") {
      this.send();
      //   }
    },
    send() {
      let url = "https://web.whatsapp.com/send";
      if (
        /Android|webOS|iPhone|iPad|Mac|Macintosh|iPod|BlackBerry|IEMobile|Opera Mini/i.test(
          navigator.userAgent
        )
      ) {
        url = "whatsapp://send";
      }
      const all =
        url +
        "?phone=+353838858622" +
        `&text=Hello Dublin Kleen 👋%0a%0a We'd like to take the first step to a sparkling clean ${
          this.cleaningFor === "household" ? "home" : "business"
        } 🫧 ${this.eircode || ""}`;
      window.open(all, "_blank");
    },
    submit: function (v) {
      if (!v) alert("Please enter eircode or area name");
      else {
        this.requestEircode = false;
        this.progress = "75%";
      }
    },
  },
  mounted() {
    if (this.$route.query.eircode) {
      this.eircode = this.$route.query.eircode;
      this.requestEircode = false;
    }
  },
};
</script>
<style scoped lang="scss">
.field__input {
  @media screen and (min-width: 840px) {
    max-width: 490px;
    margin: auto;
  }
}
/*! CSS Used from: Embedded */
.field[data-v-5f57e4d5] {
  width: auto;
  position: relative;
}
.field.field__full-width[data-v-5f57e4d5] {
  width: 100%;
}
.field .field__input[data-v-5f57e4d5] {
  position: relative;
}
.field__input input[data-v-5f57e4d5] {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  width: 100%;
  outline: none;
  box-sizing: border-box;
  border-radius: 0.75rem;
  border: 1px solid var(--color-neutral-300);
  padding: 1.5rem 2.8125rem 0.1rem 1rem;
  font-size: 1em;
  font-weight: 700;
  line-height: 1.34;
  background: var(--color-neutral-white);
}
.field__input .field__icon[data-v-5f57e4d5] {
  width: 1.5rem;
  height: 1.5rem;
  right: 1.25rem;
  top: calc(50% - 0.75rem);
  cursor: pointer;
  position: absolute;
}
.field__input > label[data-v-5f57e4d5] {
  left: 1rem;
  position: absolute;
  top: calc(50% - 0.6em);
  font-size: 1em;
  color: var(--brand-grey-700);
  transition: top 0.2s ease-in-out, font-size 0.2s ease-in-out;
}
.field__input > input:focus ~ label[data-v-5f57e4d5] {
  top: 0.3rem;
}
.field .field__options[data-v-5f57e4d5] {
  display: none;
  width: 100%;
  position: absolute;
  box-sizing: border-box;
  margin: 0.5rem 0 0;
  border-radius: 0.75rem;
  padding: 0.75rem 0;
  background-color: var(--color-neutral-white);
  box-shadow: 0px 0.25rem 1rem rgba(0, 0, 0, 0.15);
}
ul.field__options[data-v-5f57e4d5] {
  list-style: none;
}
ul.field__options[data-v-5f57e4d5] {
  border: none;
  outline: none;
}
.icon[data-v-5f57e4d5] {
  display: block;
  height: 1.5rem;
  width: 1.5rem;
  background-position: center;
  background-repeat: no-repeat;
}
.icon--magnifying-glass[data-v-5f57e4d5] {
  background-image: var(--magnifying-glass-icon-url);
}
*[data-v-5f57e4d5] {
  font-family: "Proxima Nova", sans-serif;
}
.postcode .postcode__input[data-v-5f57e4d5] {
  font-size: 1.125rem;
  margin-bottom: 1.5rem;
}
@media (max-width: 860px) {
  .postcode .postcode__input[data-v-5f57e4d5] {
    margin-bottom: 1rem;
  }
  .postcode__container .field__input input[data-v-5f57e4d5] {
    padding: 1.875rem 2.8125rem 0.5rem 1rem;
  }
  .postcode__container .field__input > input:focus ~ label[data-v-5f57e4d5] {
    top: 0.5rem;
  }
}
@media screen and (max-width: 860px) and (min-width: 600px) {
  .postcode .postcode__input[data-v-5f57e4d5] {
    margin-bottom: 1.5rem;
  }
}
/*! CSS Used fontfaces */
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
.w3-border {
  max-width: 384px;
  margin: 25px auto 0px;
  background-color: lightgray;
}
.w3-grey {
  color: #000 !important;
  background-color: rgb(68, 68, 68) !important;
  border-radius: 5px;

  .steps-container {
    // max-width: 67.5%;
    // @media screen and (min-width: 500px) and (max-width: 1650px) {
    @media screen and (min-width: 1775px) {
      width: 67.5%;
    }
    @media screen and (max-width: 1775px) {
      width: 80.5%;
    }
    @media screen and (max-width: 482px) {
      width: 100%;
    }
    margin: auto;
  }
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
/*! CSS Used from: Embedded */
.css-1pd8dxv-ResponsiveH3 {
  margin: 50px 0px !important;
}
@media (min-width: 576px) {
  .css-1pd8dxv-ResponsiveH3 {
    font-size: 28px !important;
    line-height: 38px !important;
  }
}
/*! CSS Used from: Embedded */
.css-12iu88i-Elem-BaseTypography {
  font-style: unset;
  text-transform: none;
  color: rgb(68, 68, 68);
  font-size: 18px;
  font-weight: normal;
  letter-spacing: normal;
  line-height: 26px;
  display: block;
  text-align: inherit;
  margin: 10px 0px;
  box-sizing: border-box;
  font-family: Lato, "Helvetica Neue", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
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
/*! CSS Used from: Embedded */
.btn[data-v-95337e7c] {
  width: auto;
  border: none;
  outline: none;
  cursor: pointer;
  min-width: 6.5rem;
  padding: 0.25rem 1rem;
  border-radius: 1.75rem;
  display: inline-flex;
  box-sizing: border-box;
  justify-content: center;
  align-items: center;
  font-size: 1rem;
  line-height: 1.5;
  font-weight: 400;
  text-decoration: none;
  color: var(--color-neutral-white);
  transition: background-color 300ms ease-out;
}
.btn.btn--medium[data-v-95337e7c] {
  min-width: 9rem;
  padding: 0.5rem 1rem;
  font-size: 1.125rem;
  line-height: 1.34;
}
.btn.btn--primary[data-v-95337e7c] {
  background-color: var(--brand-red-500) !important;
}
.btn.btn--primary[data-v-95337e7c]:hover {
  background-color: var(--brand-red-400) !important;
}
.btn.btn--primary[data-v-95337e7c]:active {
  background-color: var(--brand-red-800);
}
*[data-v-95337e7c] {
  color: var(--color-neutral-900);
  font-family: "Proxima Nova", sans-serif;
}
.how-it-works__btn-wrapper[data-v-95337e7c] {
  text-align: center;
}
.how-it-works__btn-wrapper .btn[data-v-95337e7c] {
  //   min-width: 18.5rem;
  text-decoration: none;
}
// @media screen and (min-width: 320px) and (max-width: 956px) and (min-width: 600px) {
//   .how-it-works__btn-wrapper .btn[data-v-95337e7c] {
//     min-width: 25rem;
//   }
// }
@media screen and (max-width: 750px) {
  .how-it-works__btn-wrapper .btn[data-v-95337e7c] {
    // min-width: 0;
    width: 100%;
  }
}
/*! CSS Used fontfaces */
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2)
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url(https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2)
    format("woff2");
  font-weight: 700;
}
</style>
