<template>
  <div>
    <div class="nav-wrapper">
      <div class="container">
        <Nav />
      </div>
    </div>
    <div class="main-container">
      <Steps />
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
.header {
  padding: 1rem 0 !important;
}
.nav-wrapper {
  border-bottom: 1px solid rgb(188, 188, 188);
}
.main-container {
  min-height: 90vh;
  display: flex;
  flex-direction: column;
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
