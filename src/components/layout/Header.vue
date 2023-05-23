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
          <ul class="nav" id="header-menu">
            <li class="nav-item">
              <a class="header-list-link" id="hotel-link" href="#">Hotel</a>
            </li>
            <li class="nav-item">
              <a class="header-list-link" id="vacation-package" href="#"
                >Vacation Package</a
              >
            </li>
            <li class="nav-item">
              <a class="header-list-link" href="#">Flight</a>
            </li>
            <li class="nav-item">
              <a class="header-list-link" aria-current="page" href="#"
                >My Account</a
              >
            </li>
            <li class="nav-item">
              <a class="header-list-link" href="#">English</a>
            </li>
            <li class="nav-item">
              <a class="header-list-link" href="#">$ USD</a>
            </li>
            <li class="nav-item">
              <a class="header-list-link" href="#">Help</a>
            </li>
          </ul>
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

<style>
#header-menu {
  float: right;
}
.header-list-link {
  display: block;
  padding: 20px;
  text-decoration: none;
}
#hotel-link {
  background-color: #f49100;
  color: white;
  margin-right: 10px;
}
#vacation-package {
  background-color: #1d9cc5;
  color: white;
}
</style>
