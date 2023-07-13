<template>
  <section class="about">
    <section class="how-it-works">
      <h2 class="h1 how-it-works__title">Get started in 3 easy steps</h2>
      <div class="how-it-works__items">
        <div class="how-it-works__item">
          <div class="how-it-works__bullet">1</div>
          <h3 class="h3 how-it-works__item-title">Submit an enquiry</h3>
          <div class="body1 how-it-works__text">
            To get started, answer a few questions about your cleaning needs.
          </div>
        </div>

        <div class="how-it-works__item">
          <div class="how-it-works__bullet">2</div>
          <h3 class="h3 how-it-works__item-title">Connect</h3>
          <div class="body1 how-it-works__text">
            We'll find a trusted cleaner based on your needs and
            send you an offer.
          </div>
        </div>

        <div class="how-it-works__item">
          <div class="how-it-works__bullet">3</div>
          <h3 class="h3 how-it-works__item-title">Hire</h3>
          <div class="body1 how-it-works__text">
            If you're happy, the cleaner will visit you and leave things
            sparkling clean ✨
          </div>
        </div>
      </div>
      <div class="how-it-works__btn-wrapper">
        <a
          href="/join-now"
          class="btn btn--primary btn--medium"
        >
          Get started
        </a>
      </div>
    </section>
  </section>
</template>
<script>
export default {};
</script>
<style scoped lang="scss">
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP-0ca91e9aecd6c4a453d73b3570fa8318.css */
.h1,
.h3 {
  margin: 0;
  font-weight: 700;
  color: var(--color-neutral-900);
}
.h1 {
  font-size: 1.75rem;
  line-height: 1.215;
}
.h3 {
  font-size: 1.125rem;
  line-height: 1.333;
}
.body1 {
  font-size: 1.125rem;
  line-height: 1.333;
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
.btn.btn--medium {
  min-width: 9rem;
  padding: 0.5rem 1rem;
  font-size: 1.125rem;
  line-height: 1.34;
}
.btn.btn--primary {
  background-color: var(--brand-red-500) !important;
}
.btn.btn--primary:hover {
  background-color: var(--brand-red-400) !important;
}
.btn.btn--primary:active {
  background-color: var(--brand-red-800);
}
* {
  color: var(--color-neutral-900);
  font-family: "Proxima Nova", sans-serif;
}
.how-it-works {
  margin-bottom: 2.5rem;
  position: relative;
}
.how-it-works:before {
  position: absolute;
  content: "";
  width: var(--how-it-works-splitter-width);
  height: 0.1875rem;
  border-radius: 6.25rem;
  background: var(--color-neutral-200);
  top: 0;
  left: calc(50% - (var(--how-it-works-splitter-width) / 2));
}
.how-it-works__title {
  text-align: center;
  padding-bottom: 1.5rem;
  padding-top: 2rem;
}
.how-it-works__items {
  display: flex;
  justify-content: space-between;
  margin-bottom: 2rem;
}
.how-it-works__item {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  width: 33%;
  padding-right: 1.5rem;
}
.how-it-works__item:last-child {
  padding-right: 0;
}
.how-it-works__bullet {
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--color-neutral-white);
  background: var(--brand-blue-900);
  font-size: 1.125rem;
  border-radius: 50%;
  min-width: 2rem;
  height: 2rem;
}
.how-it-works__item-title {
  padding-top: 1rem;
  padding-bottom: 0.5rem;
}
.how-it-works__text {
  color: var(--brand-navy-800);
}
.how-it-works__btn-wrapper {
  text-align: center;
}
.how-it-works__btn-wrapper .btn {
  min-width: 18.5rem;
  text-decoration: none;
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.desktop-0f45632f9636b933c18e24187ad9ed36.css ; media=screen and (min-width: 1280px) */
@media screen and (min-width: 1280px) {
  .how-it-works__items {
    margin-bottom: 3.5rem;
  }
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.tablet-cb8becbb5bf5f82b52f37a44e6703808.css ; media=screen and (min-width: 960px) and (max-width: 1279px) */
@media screen and (min-width: 960px) and (max-width: 1279px) {
  .how-it-works:before {
    width: var(--how-it-works-splitter-width);
    left: calc(50% - (var(--how-it-works-splitter-width) / 2));
  }
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.mobile-2d658f069f2d1c58b51e91fe98e25cc0.css ; media=screen and (min-width: 320px) and (max-width: 956px) */
@media screen and (min-width: 320px) and (max-width: 956px) {
  .how-it-works__title {
    text-align: left;
  }
  .how-it-works__items {
    display: block;
  }
  .how-it-works__item {
    width: 100%;
    margin-bottom: 2rem;
    padding-right: 0;
  }
  .how-it-works__text {
    font-size: 1rem;
    line-height: 1.375;
  }
  .how-it-works:before {
    left: 0;
  }
  @media screen and (max-width: 599px) {
    .how-it-works__title {
      font-size: 1.3125rem;
      line-height: 1.238;
    }
    .how-it-works {
      margin: 0 1.5rem 2.5rem;
    }
  }
  @media screen and (min-width: 600px) {
    .how-it-works {
      margin: 0 2rem 2.5rem;
    }
    .how-it-works__btn-wrapper .btn {
      min-width: 25rem;
    }
  }
  @media screen and (max-width: 375px) {
    .how-it-works__btn-wrapper .btn {
      min-width: 0;
      width: 100%;
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
