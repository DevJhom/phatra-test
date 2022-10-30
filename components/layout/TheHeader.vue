<script>
import MainLogo from "../ui/MainLogo.vue";

export default {
  name: "TheHeader",
  components: {
    MainLogo,
  },
  data() {
    return {
      sideBar: false,
    };
  },
  methods: {
    openSideBar() {
      this.sideBar = true;
    },
    closeSideBar() {
      this.sideBar = false;
    },
  },
};
</script>

<template>
  <div>
    <nav class="navbar">
      <div class="container-fluid px-5 py-4">
        <div>
          <img
            class="hamburger"
            @click="openSideBar"
            src="@/assets/icons/hamburger.png"
            alt="hamburger"
          />
          <nuxt-link class="navbar-brand" to="/">
            <main-logo class="logo ms-4"></main-logo>
          </nuxt-link>
        </div>
        <div class="d-flex">
          <img
            src="@/assets/icons/search.svg"
            alt="search"
            class="search me-2"
          />
          <select class="form-select language" id="lang">
            <option value="th" selected>TH</option>
            <option value="en">EN</option>
          </select>
        </div>
      </div>
    </nav>
    <div class="sidebar" :class="sideBar ? 'open' : 'close'">
      <a class="closebtn" @click="closeSideBar">×</a>
      <nuxt-link to="/">Home</nuxt-link>
      <a href="#">About Us</a>
      <a href="#">Awards</a>
      <a href="#">Our Businesses</a>
      <a href="#">News & Activities</a>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  height: 100%;
  position: fixed;
  z-index: 1000;
  top: 0;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 80px;
}

.sidebar a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 1.15rem;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.sidebar a:hover {
  color: #f1f1f1;
}

.sidebar .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 40px;
  margin-left: 50px;
}

.open {
  width: 250px;
}

.close {
  width: 0;
}

nav {
  display: flex;
  width: 100vw;
  height: 6.25rem;
  color: #fff;
  z-index: 100;
}

select {
  color: #fff;
  border: none;
  background-color: transparent;
}

.hamburger {
  width: 2.5rem;
  height: 2.5rem;
}

.search:hover {
  cursor: pointer;
}

@media (max-width: 912px) {
  img.hamburger {
    width: 1.3rem;
    height: 1.3rem;
  }

  .search {
    margin-top: 10px;
    width: 13px;
    height: 13px;
  }

  select {
    font-size: 12px;
  }
}
</style>
