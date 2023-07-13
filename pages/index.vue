<template>
  <div>
    <div class="container">
      <Nav />
      <Hero />
      <HowItWorks />
      <WhyUs />
      <Widget
        companyName="Dublin Kleen"
        companyLogo="logo.jpg"
        phoneNumber="+353838858622"
      />
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style lang="scss">
body,
html {
  margin: 0;
  padding: 0;
}
.container {
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
