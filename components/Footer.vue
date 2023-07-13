<template>
  <!-- Site footer -->
  <footer class="site-footer" style="padding: 5% 5% 2% 5%">
    <div class="footer-container">
      <div class="row">
        <!-- <div class="col-sm-12 col-md-6">
          <h6>Address</h6>
          <p class="text-justify">Dublin, Ireland</p>
        </div> -->

        <div class="col-xs-6 col-md-3">
          <h6>Contact</h6>
          <ul class="footer-links">
            <!-- <li><a href="http://scanfcode.com/about/">About Us</a></li> -->
            <li><a href="tel:+353838858622">Phone: 0838858622</a></li>
            <li>
              <a href="mailto:cleaners@kleen.ie">Email: cleaners@kleen.ie</a>
            </li>
            <!-- <li>
              <a href="http://scanfcode.com/contribute-at-scanfcode/"
                >Contribute</a
              >
            </li> -->
            <li>
              <a href="/privacy">Privacy Policy</a>
            </li>
            <!-- <li><a href="http://scanfcode.com/sitemap/">Sitemap</a></li> -->
          </ul>
        </div>
      </div>
      <hr />
    </div>
    <div class="footer-container">
      <div class="row">
        <div class="col-md-8 col-sm-6 col-xs-12">
          <p class="copyright-text">
            Copyright &copy; 2023 All Rights Reserved by
            <a href="/">Dublin Kleen</a>.
          </p>
        </div>

        <div class="col-md-4 col-sm-6 col-xs-12">
          <ul class="social-icons">
            <li>
              <a
                class="facebook"
                target="_blank"
                href="https://www.facebook.com/profile.php?id=100087290063669"
                ><img
                  width="100%"
                  src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/05/Facebook_Logo_%282019%29.png/1024px-Facebook_Logo_%282019%29.png"
                  alt=""
                  srcset=""
              /></a>
            </li>
            <!-- <li>
              <a class="twitter" href="#"><i class="fa fa-twitter"></i></a>
            </li>
            <li>
              <a class="dribbble" href="#"><i class="fa fa-dribbble"></i></a>
            </li>
            <li>
              <a class="linkedin" href="#"><i class="fa fa-linkedin"></i></a>
            </li> -->
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
footer {
  margin-top: auto;
  font-family: "Proxima Nova", sans-serif;
}
.site-footer {
  background-color: #f6f7f8;
  padding: 45px 0 20px;
  font-size: 15px;
  line-height: 24px;
  color: #505d6d;
}
.site-footer hr {
  border-top-color: #bbb;
  opacity: 0.5;
}
.site-footer hr.small {
  margin: 20px 0;
}
.site-footer h6 {
  color: #172c42;
  font-size: 16px;
  text-transform: uppercase;
  margin: 0px;
  letter-spacing: 2px;
}
.site-footer a {
  color: #172c42;
  text-decoration: none;
}
.site-footer a:hover {
  color: #3366cc;
  text-decoration: none;
}
.footer-links {
  padding-left: 0;
  list-style: none;
}
.footer-links li {
  display: block;
}
.footer-links a {
  color: #172c42;
  text-decoration: none;
}
.footer-links a:active,
.footer-links a:focus,
.footer-links a:hover {
  color: #3366cc;
  text-decoration: none;
}
.footer-links.inline li {
  display: inline-block;
}
.site-footer .social-icons {
  text-align: right;
}
.site-footer .social-icons a {
  width: 40px;
  height: 40px;
  line-height: 40px;
  margin-left: 6px;
  margin-right: 0;
  border-radius: 100%;
  background-color: #33353d;
}
.copyright-text {
  margin: 0;
}
@media (max-width: 991px) {
  .site-footer [class^="col-"] {
    margin-bottom: 30px;
  }
}
@media (max-width: 767px) {
  .site-footer {
    padding-bottom: 0;
  }
  .site-footer .copyright-text,
  .site-footer .social-icons {
    text-align: center;
  }
}
.social-icons {
  padding-left: 0;
  margin-bottom: 0;
  list-style: none;
}
.social-icons li {
  display: inline-block;
  margin-bottom: 4px;
}
.social-icons li.title {
  margin-right: 15px;
  text-transform: uppercase;
  color: #96a2b2;
  font-weight: 700;
  font-size: 13px;
}
.social-icons a {
  background-color: #eceeef;
  color: #818a91;
  font-size: 16px;
  display: inline-block;
  line-height: 44px;
  width: 44px;
  height: 44px;
  text-align: center;
  margin-right: 8px;
  border-radius: 100%;
  -webkit-transition: all 0.2s linear;
  -o-transition: all 0.2s linear;
  transition: all 0.2s linear;
}
.social-icons a:active,
.social-icons a:focus,
.social-icons a:hover {
  color: #fff;
  background-color: #29aafe;
}
.social-icons.size-sm a {
  line-height: 34px;
  height: 34px;
  width: 34px;
  font-size: 14px;
}
.social-icons a.facebook:hover {
  background-color: #3b5998;
}
.social-icons a.twitter:hover {
  background-color: #00aced;
}
.social-icons a.linkedin:hover {
  background-color: #007bb6;
}
.social-icons a.dribbble:hover {
  background-color: #ea4c89;
}
@media (max-width: 767px) {
  .social-icons li.title {
    display: block;
    margin-right: 0;
    font-weight: 600;
  }
}
</style>
