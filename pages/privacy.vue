<template>
  <div>
    <div class="container">
      <Nav />
      <div style="padding: 5%">
        <h1>Our Privacy Policy</h1>
        <p>
          We will use your information only in respect of your enquiry, so we
          can respond to it fully, and tell you about our products and services.
          It will not be used for direct marketing purposes, unless you tick the
          box below.
        </p>
      </div>
      <Widget
        companyName="Dublin Kleen"
        companyLogo="logo.jpg"
        phoneNumber="+353838858622"
      />
    </div>
    <Footer />
  </div>
</template>

<style lang="scss">
body,
html {
  margin: 0;
  padding: 0;
}
.container {
  min-height: 95vh;
  display: flex;
  flex-direction: column;
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
</style>
