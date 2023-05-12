<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-md-3">
          <div class="logo">
            <a href="#"
              ><img src="src/assets/images/logo.png" width="229" height="47"
            /></a>
          </div>
        </div>

        <div class="col-md-9 col-xs-12 nav_top">
          <div class="fr top_btn_main">
            <ul class="top_link">
              <li>
                <a id="hotel_top_btn" href="#"
                  ><i class="fa fa-bed color_white" aria-hidden="true"></i
                  ><abbr>Hote</abbr></a
                >
              </li>
              <li>
                <a id="vp_top_btn" href="#"
                  ><i class="fa fa-briefcase color_white" aria-hidden="true"></i
                  ><abbr>Vacation Packages</abbr></a
                >
              </li>
              <li>
                <a id="flight_top_btn" href="#"
                  ><i class="fa fa-plane color_white" aria-hidden="true"></i
                  ><abbr>Flight</abbr></a
                >
              </li>
            </ul>

            <ul class="nav fr">
              <li
                class="dropdown user-menu fl"
                data-role="logout"
                data-dropdown="enabled"
              >
                <a class="dropdown-toggle" data-toggle="dropdown" href="#">
                  <i class="glyphicon glyphicon-user icon_color"></i>
                  <p>My Account</p>
                  <span class="caret icon_color"></span>
                </a>
                <ul class="dropdown-menu account_dropdown">
                  <div class="col-md-7 col-sm-12">
                    <div class="social_account">
                      <a class="facebook_btn" href="#">
                        <i class="fa fa-facebook" aria-hidden="true"></i>
                        <span>connect using Facebook</span>
                      </a>
                      <a class="google_btn" href="#">
                        <i class="fa fa-google-plus" aria-hidden="true"></i>
                        <span>connect using Google</span>
                      </a>
                    </div>
                    <div class="loging_part">
                      <div class="border_or"></div>
                      <p><abbr>OR</abbr></p>
                      <h4>TravelionBE</h4>
                      <div class="form-group">
                        <input
                          type="text"
                          class="form-control"
                          id="usr"
                          placeholder="Email Address"
                        />
                      </div>
                      <div class="form-group password_form_group">
                        <input
                          type="password"
                          class="form-control"
                          id="pwd"
                          placeholder="Password"
                        />
                      </div>
                      <div class="Remember">
                        <input type="checkbox" />
                        <abbr>Remember me</abbr>
                      </div>
                      <div class="form-group">
                        <button
                          class="btn btn-primary"
                          value="btn-primary"
                          type="button"
                          name="color"
                        >
                          Continue
                        </button>
                      </div>
                      <div class="Remember">
                        <a href="#">Forgot Password?</a>
                        <br />
                        New User?
                        <a href="#">Create Account</a>
                      </div>
                    </div>
                  </div>
                  <div class="col-md-5 col-sm-12">
                    <ul class="accont_menu fr">
                      <li>
                        <a href="#">My Account</a>
                      </li>
                      <li>
                        <a href="#">My Profile</a>
                      </li>
                      <li>
                        <a href="#">Manage Bookings</a>
                      </li>
                    </ul>
                    <ul class="accont_menu top_border right_acount">
                      <li>
                        <a href="#">View E-Tickett</a>
                      </li>
                      <li>
                        <a href="#">Cancel Bookings</a>
                      </li>
                      <li>
                        <a href="#">Check Refund Status</a>
                      </li>
                    </ul>
                  </div>
                </ul>
              </li>
              <li
                class="dropdown user-menu fl"
                data-role="logout"
                data-dropdown="enabled"
              >
                <a class="dropdown-toggle" data-toggle="dropdown" href="#">
                  <span
                    ><img
                      class="lang_icon"
                      src="images/usd.png"
                      alt=""
                      height="17"
                      width="25"
                  /></span>
                  <p>English</p>
                  <span class="caret icon_color"></span>
                </a>
                <ul class="dropdown-menu sab_menu">
                  <li>
                    <a href="#"
                      ><img
                        class="lang_icon"
                        src="images/usd.png"
                        alt=""
                        height="17"
                        width="25"
                      />English</a
                    >
                  </li>
                  <li>
                    <a href="#"
                      ><img
                        class="lang_icon"
                        src="images/usd.png"
                        alt=""
                        height="17"
                        width="25"
                      />English</a
                    >
                  </li>
                </ul>
              </li>
              <li
                class="dropdown user-menu fl"
                data-role="logout"
                data-dropdown="enabled"
              >
                <a class="dropdown-toggle" data-toggle="dropdown" href="#">
                  <p>$ USD</p>
                  <span class="caret icon_color"></span>
                </a>
                <div class="dropdown-menu usd_dropdown">
                  <lable>All Currency</lable>
                  <ul>
                    <li>
                      <a
                        onclick="fun_currencyChange('AUD');"
                        href="javascript:;"
                      >
                        <span>A$ </span>
                        <p>Australian Dollar</p></a
                      >
                    </li>
                    <li>
                      <a
                        onclick="fun_currencyChange('EUR');"
                        href="javascript:;"
                      >
                        <span>€ </span>
                        <p>Euro</p></a
                      >
                    </li>
                    <li>
                      <a
                        onclick="fun_currencyChange('GBP');"
                        href="javascript:;"
                      >
                        <span>£ </span>
                        <p>British Pound</p></a
                      >
                    </li>
                    <li>
                      <a
                        onclick="fun_currencyChange('INR');"
                        href="javascript:;"
                      >
                        <span>र </span>
                        <p>Indian Rupee</p></a
                      >
                    </li>
                    <li class="active_currency">
                      <a
                        onclick="fun_currencyChange('USD');"
                        href="javascript:;"
                      >
                        <span>$ </span>
                        <p>U.S. Dollar</p></a
                      >
                    </li>
                  </ul>
                </div>
              </li>
              <li
                class="fl dropdown"
                data-role="logout"
                data-dropdown="enabled"
              >
                <a class="dropdown-toggle" data-toggle="dropdown" href="#">
                  <i class="glyphicon glyphicon-earphone icon_color"></i>
                  <p>Help</p>
                  <span class="caret icon_color"></span>
                </a>
                <div class="dropdown-menu help_box">
                  <div class="support">
                    <a href="#"
                      ><i class="fa fa-user color_white" aria-hidden="true"></i
                      >Customer Support</a
                    >
                    <span
                      ><i class="fa fa-phone" aria-hidden="true"></i>US and
                      Canada: 1-800-780-5733</span
                    >
                    <span
                      ><i class="fa fa-phone" aria-hidden="true"></i>Europe :
                      00-800-11-20-11-40</span
                    >
                  </div>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  components: {},
  data() {},
};
</script>
