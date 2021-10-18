<template>
  <div class="footer-widgets-wrap clearfix">
    <div class="row clearfix">
      <div class="col-md-6">
        <div class="widget clearfix">
          <div class="row">
            <div class="col-xs-4 widget_links">
              <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">FAQs</a></li>
                <li><a href="#">Support</a></li>
                <li><a href="#">Contact</a></li>
              </ul>
            </div>

            <div class="col-xs-4 widget_links">
              <ul>
                <li><a href="#">Shop</a></li>
                <li><a href="#">Portfolio</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">Events</a></li>
                <li><a href="#">Forums</a></li>
              </ul>
            </div>

            <div class="col-xs-4 widget_links">
              <ul>
                <li><a href="#">Corporate</a></li>
                <li><a href="#">Agency</a></li>
                <li><a href="#">eCommerce</a></li>
                <li><a href="#">Personal</a></li>
                <li><a href="#">OnePage</a></li>
              </ul>
            </div>
          </div>
        </div>
        <div class="visible-sm bottommargin-sm"></div>
      </div>

      <div class="visible-sm visible-xs line"></div>

      <div class="col-md-6">
        <div class="widget subscribe-widget clearfix">
          <h4>Subscribe to Our Newsletter</h4>
          <p>
            Get Important Offers and Deals directly to your Email Inbox.
            <em>We never send spam!</em>
          </p>
          <div class="widget-subscribe-form-result"></div>
          <form
            id="widget-subscribe-form"
            action="include/subscribe.php"
            role="form"
            method="post"
            class="nobottommargin"
          >
            <div style="margin-bottom: -10px">
              <div class="row">
                <div class="col-sm-9" style="margin-bottom: 10px">
                  <input
                    type="email"
                    id="widget-subscribe-form-email"
                    name="widget-subscribe-form-email"
                    class="form-control not-dark required email"
                    placeholder="Enter your Email"
                  />
                </div>
                <div class="col-sm-3" style="margin-bottom: 10px">
                  <button class="btn btn-block btn-success" type="submit">
                    Subscribe
                  </button>
                </div>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
    <div class="line"></div>
    <div class="row clearfix">
      <div class="col-md-7 col-sm-6">
        <div class="widget clearfix">
          <div class="clear-bottommargin-sm">
            <div class="row clearfix">
              <div class="col-md-6">
                <div class="footer-big-contacts">
                  <span>Call Us:</span>
                  <a href="#">01880089100</a>, <a href="#">01880089101</a>,
                  <a href="#">01880089102</a>
                </div>
                <div class="visible-sm visible-xs bottommargin-sm"></div>
              </div>
              <div class="col-md-6">
                <div class="footer-big-contacts">
                  <span>Email Us:</span>
                  <a href="#">travelforing@gmail.com</a>
                </div>
                <div class="visible-xs bottommargin-sm"></div>
              </div>
            </div>
          </div>
        </div>
        <div class="visible-sm visible-xs bottommargin-sm"></div>
      </div>
      <div class="col-md-5 col-sm-6">
        <div
          class="clearfix"
          data-class-lg="fright"
          data-class-md="fright"
          data-class-sm="fright"
          data-class-xs=""
          data-class-xxs=""
        >
          <a
            href="https://www.facebook.com/travelforing/"
            target="_blank"
            class="social-icon si-rounded si-small si-colored si-facebook"
          >
            <i class="icon-facebook"></i>
            <i class="icon-facebook"></i>
          </a>
          <a
            href="https://instagram.com/foringer_dol?utm_medium=copy_link"
            target="_blank"
            class="social-icon si-rounded si-small si-colored si-gplus"
          >
            <i class="icon-instagram"></i>
            <i class="icon-instagram"></i>
          </a>
          <a
            href="https://youtube.com/channel/UC-CGAoKw4Cf4xJt8kT8B-ZQ"
            target="_blank"
            class="social-icon si-rounded si-small si-colored si-pinterest"
          >
            <i class="icon-youtube"></i>
            <i class="icon-youtube"></i>
          </a>
        </div>
      </div>
    </div>
    <div id="copyrights">
      <div class="container center uppercase clearfix">
        &copy; 2021 Developed by
        <a href="https://www.facebook.com/catchbitflex" target="_blank"
          >BitFlex </a
        >|
        <a href="https://www.facebook.com/catchbangladesh" target="_blank"
          >Catch Bangladesh</a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
