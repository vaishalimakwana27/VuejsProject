<template>
  <div class="new_benner">
    <div id="container2"></div>
    <div class="tab_content_main">
      <div class="container">
        <ul class="nav nav-tabs home_tab">
          <li class="active">
            <a href="#Hotel" data-toggle="tab"
              ><span><i class="fa fa-bed color_white"></i></span
              ><label>Hotels</label></a
            >
          </li>
          <li class="">
            <a href="#vp" data-toggle="tab"
              ><span
                ><i class="glyphicon glyphicon-briefcase color_white"></i></span
              ><label>Vacation Packages</label></a
            >
          </li>
        </ul>
        <div id="myTabContent" class="tab-content">
          <div class="tab-pane active in" id="Hotel">
            <div class="search-form">
              <div class="search-content">
                <ul class="hotel_tab_home">
                  <li class="landmark">
                    <input
                      type="text"
                      name=""
                      value=""
                      placeholder="City, Hotels, Airport or Landmark"
                    />
                  </li>
                  <li class="date input-append" id="datetimepicker">
                    <input
                      id="check-in_date"
                      data-date-icon="icon-calendar"
                      class="add-on"
                      type="text"
                      name=""
                      value=""
                      placeholder="Check-in"
                    />
                  </li>
                  <li class="date input-append" id="datetimepicker2">
                    <input
                      id="check-in_date"
                      data-date-icon="icon-calendar"
                      class="add-on"
                      type="text"
                      name=""
                      value=""
                      placeholder="Check-out"
                    />
                  </li>
                  <li class="person_in">
                    <input
                      type="text"
                      name=""
                      value=""
                      placeholder="1 Person in 1 Room"
                    />
                    <div class="append" style="display: none">
                      <div class="room_add_main">
                        <h3>Room : 1</h3>
                        <ul class="append_room_add">
                          <li>
                            <label>Adults</label>
                            <p>Above 12 years</p>
                            <div class="divider_rooms">
                              <span
                                ><a
                                  class="minus_rooms"
                                  href="javascript:void(0)"
                                ></a
                              ></span>
                              <span class="room_nmbr"
                                ><a
                                  class="no_of_rooms"
                                  href="javascript:void(0)"
                                  >1</a
                                ></span
                              >
                              <span
                                ><a
                                  class="plus_rooms"
                                  href="javascript:void(0)"
                                ></a
                              ></span>
                            </div>
                          </li>
                          <li>
                            <label>Children </label>
                            <p>Below 12 years</p>
                            <div class="divider_rooms">
                              <span
                                ><a
                                  class="minus_rooms"
                                  href="javascript:void(0)"
                                ></a
                              ></span>
                              <span class="room_nmbr"
                                ><a
                                  class="no_of_rooms"
                                  href="javascript:void(0)"
                                  >1</a
                                ></span
                              >
                              <span
                                ><a
                                  class="plus_rooms"
                                  href="javascript:void(0)"
                                ></a
                              ></span>
                            </div>
                          </li>
                        </ul>
                      </div>
                      <ul class="append_room_add more_add_rooms">
                        <li>
                          <label>Age of Children </label>
                          <div class="divider_rooms">
                            <span
                              ><a
                                class="minus_rooms"
                                href="javascript:void(0)"
                              ></a
                            ></span>
                            <span class="room_nmbr"
                              ><a class="no_of_rooms" href="javascript:void(0)">
                                1</a
                              ></span
                            >
                            <span
                              ><a
                                class="plus_rooms"
                                href="javascript:void(0)"
                              ></a
                            ></span>
                          </div>
                          <div class="divider_rooms">
                            <span
                              ><a
                                class="minus_rooms"
                                href="javascript:void(0)"
                              ></a
                            ></span>
                            <span class="room_nmbr"
                              ><a class="no_of_rooms" href="javascript:void(0)"
                                >1</a
                              ></span
                            >
                            <span
                              ><a
                                class="plus_rooms"
                                href="javascript:void(0)"
                              ></a
                            ></span>
                          </div>
                          <div class="divider_rooms margin_right_none">
                            <span
                              ><a
                                class="minus_rooms"
                                href="javascript:void(0)"
                              ></a
                            ></span>
                            <span class="room_nmbr"
                              ><a class="no_of_rooms" href="javascript:void(0)"
                                >1</a
                              ></span
                            >
                            <span
                              ><a
                                class="plus_rooms"
                                href="javascript:void(0)"
                              ></a
                            ></span>
                          </div>
                        </li>
                      </ul>
                      <div class="add_remove_btn">
                        <a href="javascript:void(0)" class="add_room"
                          >Add Room</a
                        >
                        <a href="javascript:void(0)" class="remove_room"
                          >Remove This Room</a
                        >
                      </div>
                      <div class="social_account center-part">
                        <a
                          class="continus-btn hvr-shutter-out-vertical"
                          href="#"
                          >Done</a
                        >
                      </div>
                    </div>
                  </li>
                  <li class="search_btn">
                    <a class="hvr-shutter-out-vertical" href="#">Search</a>
                  </li>
                </ul>
                <ul class="sep_date">
                  <li class="landmark"></li>
                  <li class="specific_dates">
                    <input type="checkbox" name="" value="" />
                    <p>I don't have specific dates yet</p>
                  </li>
                  <li class="tip_main">
                    <p>Tip: Select fewer than 4 adults for the most results</p>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="tab-pane fade" id="vp">
            <div class="search-form">
              <div class="search-content Hotel_Destination">
                <ul class="vp_main_form">
                  <li class="landmark">
                    <label>Region</label>
                    <input
                      type="text"
                      name=""
                      value=""
                      placeholder="Search Your Holiday Destination"
                    />
                  </li>
                  <li class="monnth_part">
                    <label>Month</label>
                    <div class="selectborder">
                      <span
                        ><img
                          src="src/assets/images/date.png"
                          width="19"
                          height="22"
                          alt=""
                      /></span>
                      <span class="select_box">-- All --</span>
                      <select class="month_box">
                        <option>January</option>
                        <option>February</option>
                        <option>March</option>
                        <option>April</option>
                        <option>May</option>
                        <option>June</option>
                        <option>July</option>
                        <option>August</option>
                        <option>September</option>
                        <option>October</option>
                        <option>November</option>
                        <option>December</option>
                      </select>
                    </div>
                  </li>
                  <li class="monnth_part">
                    <label>Tour Theme</label>
                    <div class="selectborder">
                      <span class="tour_them_icon"
                        ><img
                          src="src/assets/images/icon_vp.png"
                          width="19"
                          height="17"
                          alt=""
                      /></span>
                      <span class="select_box">-- All --</span>
                      <select class="month_box">
                        <option>Nightlife</option>
                        <option>Adventure</option>
                        <option>Gastronomic delights</option>
                        <option>Shopping</option>
                        <option>Romance</option>
                        <option>Theme Parks</option>
                        <option>Natural Wonders</option>
                        <option>Beaches</option>
                        <option>Cultural Heritage</option>
                        <option>Entertainment</option>
                        <option>Winter Sports</option>
                        <option>Family</option>
                        <option>Weekend</option>
                      </select>
                    </div>
                  </li>
                  <li class="search_btn search_btn_vp">
                    <a class="hvr-shutter-out-vertical" href="#"
                      >Search Holidays</a
                    >
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainContent",
  components: {},
  data() {},
};
</script>
