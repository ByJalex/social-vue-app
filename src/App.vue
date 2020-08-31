<template>
  <div id="app">
    <div class="nav">
      <div class="content-nav">
        <div class="item-nav">
          <router-link to="/">
            <i class="bx bx-home bx-sm icon-nav"></i>
          </router-link>
        </div>
        <div>
          <router-link to="/favorite">
            <i class="bx bx-star bx-sm icon-nav"></i>
          </router-link>
        </div>
        <div class="center-button">
          <router-link to="/add">
            <i class="bx bx-plus bx-sm"></i>
          </router-link>
        </div>
        <div>
          <router-link to="/messages">
            <i class="bx bx-message-square-detail bx-sm icon-nav"></i>
          </router-link>
        </div>
        <div>
          <router-link to="/profile">
            <i class="bx bx-slider-alt bx-sm icon-nav"></i>
          </router-link>
        </div>
      </div>
    </div>
    <router-view />
  </div>
</template>

<style>
* {
  font-family: 'Josefin Sans', sans-serif;
  margin: 0;
  padding: 0;
}

a{
  text-decoration: none;
  color: #499EF9;
}

.icon-nav {
  color: #808080;
}

.center-button {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 55px;
  width: 55px;
  background-color: #499ef9;
  margin-top: -35px;
  color: white;
  border-radius: 50%;
  border-style: solid;
  border-color: white;
}

.center-button a i {
  color: white;
}

.content-nav {
  display: flex;
  justify-content: space-between;
  padding: 15px;
}

.nav {
  bottom: 0;
  width: 100%;
  position: fixed;
  background-color: #fff;
}

.nav a.router-link-exact-active i {
  color: #353535;
}
</style>
