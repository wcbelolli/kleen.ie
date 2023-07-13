<template>
  <nav>
    <section class="header">
      <div class="header__content header__content_desktop">
        <a
          class="header__logo btn btn--icon"
          href="/"
          aria-label="Find Childcare, Housekeepers &amp; Pet Sitters - Care.com IE"
        >
          Dublin Kleen
        </a>

        <span class="header__links">
          <!-- <a
            href="#about"
            rel="nofollow"
            class="header__link btn btn--link no-mobile"
          >
            Why us?
          </a> -->

          <a
            href="mailto:cleaners@kleen.ie"
            rel="nofollow"
            class="header__link btn btn--link"
          >
            Email
          </a>

          <a
            @click="send"
            rel="nofollow"
            class="header__link btn btn--primary"
            style="width: 8.5rem"
          >
            <img
              src="https://cdn-icons-png.flaticon.com/512/124/124034.png"
              alt=""
            />
            WhatsApp
          </a>
        </span>
      </div>
    </section>
  </nav>
</template>
<script>
export default {
  name: "IndexPage",
  methods: {
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
        `&text=Hello Dublin Kleen 👋%0a%0a We'd like to take the first step to a sparkling clean home 🫧`;
      window.open(all, "_blank");
    },
  },
};
</script>
<style scoped lang="scss">
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP-0ca91e9aecd6c4a453d73b3570fa8318.css */
.btn {
  //   width: 17%;
  border: none;
  outline: none;
  cursor: pointer;
  background-color: white !important;
  //   min-width: 8.5rem;
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
  transition: background-color 100ms ease-out;
  justify-content: start;
}
.btn.btn--icon,
.btn.btn--link {
  padding: 0;
  min-width: auto;
  font-weight: 700;
  background: none;
}

// .btn.btn--link:hover {
//   text-decoration: underline;
// }
.btn.btn--primary {
  background-color: var(--whatsapp) !important;
  img {
    width: 30%;
  }
}
// .btn.btn--primary:hover {
//   /* background-color: var(--brand-red-400); */
//   background-color: rgba(241, 32, 0, 0.8);
// // }
// .btn.btn--primary:active {
//   background-color: var(--brand-red-800);
// }
// .btn.btn--secondary {
//   background-color: var(--brand-navy-800);
// }
// .btn.btn--secondary:hover {
//   background-color: var(--brand-navy-700);
// }
// .btn.btn--secondary:active {
//   background-color: var(--brand-navy-900);
// }
* {
  /* color: var(--color-neutral-900); */
  font-family: "Proxima Nova", sans-serif;
}
.header {
  padding: 1rem 0;
}
.header .header__content {
  display: flex;
  align-items: center;
}
.header .header__content:not(.header__content_desktop) {
  display: none;
}
.header .header__logo {
  margin-right: auto;
  color: black;
}
@media (max-width: 650px) {
  .no-mobile {
    display: none;
  }
}

@media (max-width: 500px) {
  nav {
    padding: 0 5%;
  }
}
.header .header__links {
  display: inline-flex;
  align-items: center;
  justify-content: end;
}
.header__links .header__link:not(:last-child) {
  margin-right: 2rem;
}
.header__links .header__link.btn.btn--link {
  font-weight: normal;
  color: inherit;
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.desktop-0f45632f9636b933c18e24187ad9ed36.css ; media=screen and (min-width: 1280px) */
@media screen and (min-width: 1280px) {
  .header {
    padding: 1.25rem 0;
  }
}
/*! CSS Used from: https://euwprd-cdn-w.care.com/assets/welcomeVHP.mobile-2d658f069f2d1c58b51e91fe98e25cc0.css ; media=screen and (min-width: 320px) and (max-width: 956px) */
/* @media screen and (min-width: 320px) and (max-width: 956px) {
  .header {
    margin: 0;
    top: -4rem;
    transition: top 0.1s ease-out;
  }
  .header .header__content.header__content_mobile {
    display: flex;
  }
  .header .header__content:not(.header__content_mobile) {
    display: none;
  }
  @media screen and (max-width: 599px) {
    .header {
      padding-left: 1.5rem;
      padding-right: 1.5rem;
    }
  }
  @media screen and (min-width: 600px) {
    .header {
      padding-left: 2rem;
      padding-right: 2rem;
    }
  }
} */
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
