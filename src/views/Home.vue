<template>
  <div class="home">
    <div class="header-home">
      <div class="header-home-content">
        <div>
          <i class="bx bx-notification bx-sm"></i>
        </div>
        <div>josue_ayala27</div>
        <div>
          <i class="bx bx-circle bx-sm"></i>
        </div>
      </div>
    </div>
    <div class="stories-container">
      <div class="stories-content">
        <div class="stories-header">
          <div>
            <h1>Stories</h1>
          </div>
          <div>
            <router-link to="/stories">See all</router-link>
          </div>
        </div>
        <div>
          <span class="text-gray">Explore the stories shared by your circles.</span>
        </div>
        <div class="stories-image-content">
          <div class="scroll-stories">
            <div :key="item.id" v-for="item in $store.state.profileStories" class="storie">
              <img class="img-bg" :src="item.imageBack" alt />
              <div class="storie-profile-photo">
                <img class="img-center-storie" :src="item.imgProfile" alt />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
};
</script>

<style>
.scroll-stories {
  text-align: center;
  display: inline-flex;
  text-align: center;
}
.storie-profile-photo {
  position: absolute;
  width: 50px;
  height: 50px;
  background: #000;
  border-radius: 50px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.25s ease;
  border: 1px solid #499ef9;
}
.storie-profile-photo img {
  display: flex;
  align-items: center;
  justify-content: center;
  transform: scale(1.3);
  width: 100%;
  transition: all 0.25s ease;
}
.storie {
  margin-left: 2px;
  margin-right: 2px;
  width: 120px;
  height: 170px;
  border-radius: 10px;
  overflow: hidden;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.25s ease;
  backface-visibility: hidden;
}

.storie .img-bg {
  height: 100%;
  transform: scale(1.29);
  transition: all 0.25s ease;
}

.storie:hover .img-bg {
  height: 100%;
  transform: scale(1.2);
}

.storie:hover .storie-profile-photo img {
  width: 100%;
  transform: scale(1.4);
}
.stories-image-content {
  /*background-color: red;*/
  margin-top: 15px;
  overflow-x: scroll;
}

.stories-image-content::-webkit-scrollbar {
  width: 8px; /* Tamaño del scroll en vertical */
  height: 8px; /* Tamaño del scroll en horizontal */
  display: none; /* Ocultar scroll */
}

.text-gray {
  color: #75747a;
}
.stories-content {
  padding: 15px;
}
.stories-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.stories-container {
  margin-top: 10px;
}
.header-home {
  width: 100%;
  background-color: #f4f4f4;
}
.header-home-content {
  padding: 15px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
