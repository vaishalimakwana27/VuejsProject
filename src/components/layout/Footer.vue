<template>
  <div class="featured_part">
    <div class="container">
      <div class="row">
        <div class="col-md-8">
          <div class="center_head left_head">
            <h2>FEATURED HOTELS</h2>
            <div class="main_border">
              <hr class="head_border_top" />
            </div>
            <div class="main_border_bottom">
              <hr class="read_border_bottom" />
            </div>
          </div>
          <ul class="featured_manu">
            <li><a href="#">New York City</a></li>
            <li><a href="#">San Francisco</a></li>
            <li><a href="#">Las Vegas</a></li>
            <li><a href="#">Miami</a></li>
            <li><a href="#">USA</a></li>
            <li><a href="#">Paris</a></li>
            <li><a href="#">Washington DC</a></li>
            <li><a href="#">Rome</a></li>
            <li><a href="#">Chicago</a></li>
            <li><a href="#">Australia</a></li>
            <li><a href="#">London</a></li>
            <li><a href="#">Orlando</a></li>
            <li><a href="#">Sydney</a></li>
            <li><a href="#">Cairns</a></li>
            <li><a href="#">New Zealand</a></li>
            <li><a href="#">Melbourne</a></li>
            <li><a href="#">Hawaii</a></li>
            <li><a href="#">Tokyo</a></li>
            <li><a href="#">Los Angeles</a></li>
            <li><a href="#">France</a></li>
            <li><a href="#">Madrid</a></li>
            <li><a href="#">Venice</a></li>
            <li><a href="#">Milan</a></li>
            <li><a href="#">Amsterdam</a></li>
            <li><a href="#">Italy</a></li>
          </ul>
        </div>
        <div class="col-md-4">
          <div class="center_head left_head">
            <h2>DEALS IN YOUR INBOX</h2>
            <div class="main_border">
              <hr class="head_border_top" />
            </div>
            <div class="main_border_bottom">
              <hr class="read_border_bottom" />
            </div>
          </div>
          <div class="connect_us">
            <p>
              Subscribe to our newsletter to receive the latest news and
              Exclusive deals
            </p>
            <div align="center" class="connect_part">
              <span class="paper_icon icon_box"></span>
              <input
                id="email"
                type="text"
                placeholder="Email address"
                data-bvalidator="email,required"
                name="data[Subscriber][email]"
              />
              <input
                align="middle"
                type="submit"
                name="SUBSCRIBE"
                value="SUBSCRIBE"
              />
            </div>
            <div class="center_head left_head connect_head margin_none">
              <h2>CONNECT WITH US</h2>
              <div class="main_border">
                <hr class="head_border_top" />
              </div>
              <div class="main_border_bottom">
                <hr class="read_border_bottom" />
              </div>
            </div>
            <ul class="contact_box margin_none">
              <li><a class="fb icon_box" href="#"></a></li>
              <li><a class="tw icon_box" href="#"></a></li>
              <li><a class="gplus icon_box" href="#"></a></li>
              <li><a class="in icon_box" href="#"></a></li>
              <li><a class="rss icon_box" href="#"></a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="footer">
    <div class="footer_menu">
      <ul class="f_menu">
        <li><a href="#">Home</a></li>
        <li><a href="#">About Us</a></li>
        <li><a href="#">All destinations</a></li>
        <li><a href="#">support</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
    </div>
    <div class="footer_social">
      <ul>
        <li>
          <label>Verisign Secure</label><br />
          <span class="secure"></span>
        </li>
        <li>
          <label>We Accept(more)</label><br />
          <span class="accept"></span>
        </li>
        <li>
          <label>Hotels Reviews By</label><br />
          <span class="review"></span>
        </li>
      </ul>
    </div>
    <div class="footer_menu">
      <div class="container">
        <p>
          Copyright © 2016Travelonwards.com - All rights reserved.
          <a href="#">Privacy Policy</a> | <a href="#">Terms & Conditions</a>
        </p>
        <span>Powered By - <a href="#">TravelOTAS.com</a></span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Footer",
  components: {},
};
</script>
