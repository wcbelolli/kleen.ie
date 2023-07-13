<template>
  <section class="why-us">
    <h2 class="h1 why-us__title">Why choose Dublin Kleen?</h2>
    <div class="why-us__items">
      <div class="why-us__item">
        <div class="why-us__bullet">
          <img
            src="https://euwprd-cdn-w.care.com/assets/img/welcomePage/check-icon-3e820387c8b6fadf65713fed7513894a.svg"
            width="13"
            height="10"
            alt="Check mark"
          />
        </div>
        <div class="body1 why-us__text">
          We're a young Irish business who're eager to work hard and impress you.
        </div>
      </div>

      <div class="why-us__item">
        <div class="why-us__bullet">
          <img
            src="https://euwprd-cdn-w.care.com/assets/img/welcomePage/check-icon-3e820387c8b6fadf65713fed7513894a.svg"
            width="13"
            height="10"
            alt="Check mark"
          />
        </div>
        <div class="body1 why-us__text">
          We select, vet and train all our cleaners in Dublin area.
        </div>
      </div>

      <div class="why-us__item">
        <div class="why-us__bullet">
          <img
            src="https://euwprd-cdn-w.care.com/assets/img/welcomePage/check-icon-3e820387c8b6fadf65713fed7513894a.svg"
            width="13"
            height="10"
            alt="Check mark"
          />
        </div>
        <div class="body1 why-us__text">
          We're commited to your satisfaction to
          <span style="font-weight: bold; font-style: italic">earn</span> your 5
          star rating.
        </div>

        <!-- on our new (shiny) Google profile -->
      </div>
    </div>
  </section>
</template>
<script>
export default {};
</script>
<style scoped lang="scss">
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP-0ca91e9aecd6c4a453d73b3570fa8318.css */
.h1 {
  margin: 0;
  font-weight: 700;
  color: var(--color-neutral-900);
}
.h1 {
  font-size: 1.75rem;
  line-height: 1.215;
}
.body1 {
  font-size: 1.125rem;
  line-height: 1.333;
}
* {
  color: var(--color-neutral-900);
  font-family: "Proxima Nova", sans-serif;
}
.why-us {
  background: var(--brand-blue-100);
  border-radius: 1.25rem;
}
.why-us__title {
  text-align: center;
  padding-bottom: 1.5rem;
}
.why-us__items {
  display: flex;
  justify-content: space-between;
}
.why-us__item {
  display: flex;
  align-items: flex-start;
  width: 33%;
  padding-right: 1.5rem;
}
.why-us__item:last-child {
  padding-right: 0;
}
.why-us__bullet {
  display: flex;
  justify-content: center;
  align-items: center;
  background: var(--brand-green-700);
  border-radius: 50%;
  min-width: 1.375rem;
  height: 1.375rem;
  margin-right: 1rem;
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.desktop-0f45632f9636b933c18e24187ad9ed36.css ; media=screen and (min-width: 1280px) */
@media screen and (min-width: 1280px) {
  .why-us {
    margin: 3rem 0;
    padding: 3rem 0;
  }
  .why-us__items {
    padding: 0 3.5rem;
  }
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.tablet-cb8becbb5bf5f82b52f37a44e6703808.css ; media=screen and (min-width: 960px) and (max-width: 1279px) */
@media screen and (min-width: 960px) and (max-width: 1279px) {
  .why-us {
    margin: 2.5rem 0;
    padding: 2.5rem 0;
  }
  @media screen and (max-width: 1023px) {
    .why-us {
      margin: 2rem 0;
    }
    .why-us__items {
      padding: 0 1.5rem;
    }
  }
  @media screen and (min-width: 1024px) {
    .why-us__items {
      padding: 0 2rem;
    }
  }
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.mobile-2d658f069f2d1c58b51e91fe98e25cc0.css ; media=screen and (min-width: 320px) and (max-width: 956px) */
@media screen and (max-width: 956px) {
  .why-us {
    // padding: 0;
    // background: none;
    padding: 2rem 1.5rem;
    margin: 2rem 0rem;
  }
  .why-us__title {
    text-align: left;
  }
  .why-us__item {
    width: 100%;
    margin-bottom: 1rem;
    padding-right: 0;
  }
  .why-us__item:last-child {
    margin-bottom: 0;
  }
  .why-us__items {
    display: block;
  }
  @media screen and (max-width: 599px) {
    .why-us {
      padding: 2rem 1.5rem;
      margin: 2rem 0rem;
      border-radius: 0;
    }
    .why-us__title {
      font-size: 1.3125rem;
      line-height: 1.238;
    }
  }
  @media screen and (min-width: 600px) {
    .why-us {
      margin: 2rem;
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
