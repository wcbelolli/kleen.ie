<template>
  <section class="hero">
    <aside class="hero__postcode">
      <div class="postcode">
        <h1 class="h1 postcode__title">Find trusted cleaners in Dublin</h1>

        <div class="postcode__container">
          <div class="postcode__mobile-controls">
            <button id="cancel-button" class="btn btn--icon">
              <span class="icon icon--close"></span>
            </button>
            <button id="skip-button" class="btn btn--link">
              Skip and continue
            </button>
          </div>
          <div class="field field__full-width postcode__input">
            <div class="field__input">
              <input
                id="postcode-input"
                type="text"
                v-model="eircode"
                @keyup.enter="submit"
              />
              <label for="postcode-input">Enter Eircode</label>
              <span class="field__icon">
                <span
                  id="postcode-status-icon"
                  class="icon icon--magnifying-glass"
                  @click="submit"
                ></span>
              </span>
            </div>
            <ul id="postcode-options" class="field__options"></ul>
          </div>

          <label for="sign-up-button">Searching for jobs?</label>

          <button
            id="sign-up-button"
            class="btn btn--link link--primary"
            style="color: #015ac8"
            @click="apply"
          >
            Get started &gt;
          </button>
        </div>
      </div>
    </aside>

    <div class="hero__separator">
      <svg
        xmlns:svg="http://www.w3.org/2000/svg"
        xmlns="http://www.w3.org/2000/svg"
        preserveAspectRatio="none"
        version="1.0"
        viewBox="0 0 26 17"
      >
        <path d="M 0,0 L 17,0 L 0,17 L 0,0 z"></path>
      </svg>
    </div>
    <aside class="hero__image"></aside>
  </section>
</template>
<script>
export default {
  data() {
    return {
      eircode: null,
    };
  },
  methods: {
    submit: function () {
      if (!this.eircode) alert("Please enter eircode or area name");
      else {
        this.$router.push("/join-now?eircode=" + this.eircode);
      }
    },
    apply() {
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
        `&text=Hello Dublin Kleen 👋%0a%0a I'd like to find a cleaning job in Dublin.`;
      window.open(all, "_blank");
    },
  },
};
</script>
<style scoped lang="scss">
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP-0ca91e9aecd6c4a453d73b3570fa8318.css */
.h1 {
  margin: 0;
  font-weight: 700;
  // color: var(--color-neutral-900);
}
#sign-up-button {
  background-color: var(--hero-postcode-color) !important;
}
.h1 {
  font-size: 1.75rem;
  line-height: 1.215;
}
.btn {
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
.btn.btn--icon,
.btn.btn--link {
  padding: 0;
  min-width: auto;
  font-weight: 700;
  background: none;
}
.btn.btn--link:hover {
  text-decoration: underline;
}
.field {
  width: auto;
  position: relative;
}
.field.field__full-width {
  width: 100%;
}
.field .field__input {
  position: relative;
}
.field__input input {
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
  // color: var(--color-neutral-900);
  background: var(--color-neutral-white);
}
.field__input .field__icon {
  width: 1.5rem;
  height: 1.5rem;
  right: 1.25rem;
  top: calc(50% - 0.75rem);
  cursor: pointer;
  position: absolute;
}
.field__input > label {
  left: 1rem;
  position: absolute;
  top: calc(50% - 0.6em);
  font-size: 1em;
  color: var(--brand-grey-700);
  transition: top 0.2s ease-in-out, font-size 0.2s ease-in-out;
}
.field__input > input:focus ~ label {
  top: 0.3rem;
}
.field .field__options {
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
ul.field__options {
  list-style: none;
}
ul.field__options {
  border: none;
  outline: none;
}
.icon {
  display: block;
  height: 1.5rem;
  width: 1.5rem;
  background-position: center;
  background-repeat: no-repeat;
}
.icon--close {
  background-image: var(--close-icon-url);
}
.icon--magnifying-glass {
  background-image: var(--magnifying-glass-icon-url);
}
* {
  // color: var(--color-neutral-900);
  font-family: "Proxima Nova", sans-serif;
}
.hero {
  display: grid;
  margin-bottom: 2rem;
  grid-template-columns: 1fr var(--hero-splitter-width) 1fr;
  grid-template-areas: "hero__postcode hero__separator hero__image";
  height: 370px;
}
.hero .hero__separator {
  z-index: 1;
  grid-area: hero__separator;
}
.hero__separator > svg {
  height: 100%;
  width: var(--hero-splitter-width);
  fill: var(--hero-postcode-color);
}
.hero .hero__image {
  grid-area: hero__image;
  background-size: cover;
  background-repeat: no-repeat;
  //   @media screen and (min-width: 1775px) {
  // width: 800px;
  // background-position: center;
  //   }
  background-position: center;
  margin-left: calc(-1 * var(--hero-splitter-width));
  border-top-right-radius: var(--hero-border-radius);
  border-bottom-right-radius: var(--hero-border-radius);
}
.hero .hero__postcode {
  grid-area: hero__postcode;
  z-index: 1;
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  background-color: var(--hero-postcode-color);
  border-top-left-radius: var(--hero-border-radius);
  border-bottom-left-radius: var(--hero-border-radius);
}
.hero .hero__postcode,
.hero .hero__image {
  box-shadow: 0 0.125rem 0.5rem rgba(0, 0, 0, 0.15);
}
.hero__postcode .postcode__container {
  max-width: 19rem;
}
.hero__postcode .postcode {
  max-width: initial;
  margin: 0 2.5rem 0 4rem;
  box-sizing: border-box;
  padding: 5rem 0;
}
.postcode .postcode__title {
  word-break: break-word;
  margin-bottom: 1.5rem;
}
.postcode .postcode__input {
  font-size: 1.125rem;
  margin-bottom: 1.5rem;
}
.postcode__mobile-controls {
  display: none;
}
label[for="sign-up-button"] {
  font-weight: 700;
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.desktop-0f45632f9636b933c18e24187ad9ed36.css ; media=screen and (min-width: 1280px) */
@media screen and (min-width: 1280px) {
  .hero .hero__image {
    background-image: url("~static/hero.jpg");
  }
  .postcode .postcode__title {
    font-size: 2.25rem;
    line-height: 1.16;
  }
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.tablet-cb8becbb5bf5f82b52f37a44e6703808.css ; media=screen and (min-width: 960px) and (max-width: 1279px) */
@media screen and (min-width: 860px) and (max-width: 1279px) {
  .hero .hero__image {
    background-image: url("~static/hero.jpg");
  }
  @media screen and (max-width: 1023px) {
    .hero__postcode .postcode {
      padding: 5.5rem 0px 6.375rem 0px;
    }
  }
  @media screen and (min-width: 1024px) {
    .postcode .postcode__title {
      margin-bottom: 2rem;
    }
  }
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.mobile-2d658f069f2d1c58b51e91fe98e25cc0.css ; media=screen and (min-width: 320px) and (max-width: 956px) */
@media (max-width: 860px) {
  .hero {
    margin-bottom: 2rem;
    grid-template-columns: 1fr;
    grid-template-rows: calc(11.5rem + var(--hero-border-radius)) 1fr;
    grid-template-areas: "hero__image hero__image hero__image" "hero__postcode hero__postcode hero__postcode";
  }
  .hero .hero__separator {
    display: none;
  }
  .hero .hero__image,
  .hero .hero__postcode {
    border-radius: 0;
    box-shadow: none;
  }
  .hero .hero__image {
    margin-left: 0;
    background-position: top;
    background-image: url("~static/hero.jpg");
  }
  //   .hero .hero__postcode {
  //     margin-top: calc(-1 * var(--hero-border-radius));
  //     border-top-left-radius: var(--hero-border-radius);
  //     border-top-right-radius: var(--hero-border-radius);
  //   }
  .postcode .postcode__title {
    text-align: center;
    font-size: 1.5rem;
    line-height: 1.4;
  }
  .postcode .postcode__title,
  .postcode .postcode__input {
    margin-bottom: 1rem;
  }
  .hero__postcode .postcode {
    width: 100%;
    max-width: initial;
    margin: 0 auto;
    padding: 1.5rem;
  }
  .hero__postcode .postcode__container {
    max-width: initial;
  }
  .postcode__container > #sign-up-button,
  .postcode__container > label[for="sign-up-button"] {
    display: none;
  }
  .postcode__container .field__input input {
    padding: 1.875rem 2.8125rem 0.5rem 1rem;
  }
  .postcode__container .field__input > input:focus ~ label {
    top: 0.5rem;
  }
  @media screen and (min-width: 870px) {
    .hero {
      grid-template-rows: calc(16.375rem + var(--hero-border-radius)) 1fr;
    }
    .hero__postcode .postcode {
      padding: 3rem 6.375rem;
    }
    .postcode .postcode__title,
    .postcode .postcode__input {
      margin-bottom: 1.5rem;
    }
  }
}
/*! CSS Used fontfaces */
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url("https://euwprd-cdn-w.care.com/assets/proxima-nova-regular.woff2")
    format("woff2");
}
@font-face {
  font-family: "Proxima Nova";
  font-display: swap;
  src: url("https://euwprd-cdn-w.care.com/assets/proxima-nova-bold.woff2")
    format("woff2");
  font-weight: 700;
}
</style>
