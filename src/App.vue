<template>
  <div id="app">
    <v-app-bar
      absolute
      color="#1976D2"
      height="80px"
    >
      <v-app-bar-nav-icon style="color:white"></v-app-bar-nav-icon>
      <v-toolbar-title style="color:white">清澜山信息技术交流实践俱乐部 官方网站</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon style="color:white">
        <v-icon color="white">mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon style="color:white">
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon style="color:white">
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    <v-carousel
      cycle
      height="400"
      hide-delimiter-background
      show-arrows-on-hover
    >
      <v-carousel-item
        v-for="(slide, i) in slides"
        :key="i"
      >
        <v-sheet
          :color="colors[i]"
          height="100%"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <div class="display-3">{{ slide }} Slide</div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <router-view/>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
        ],
        slides: [
          'First',
          'Second',
          'Third',
          'Fourth',
          'Fifth',
        ],
      }
    },
  }
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
//  src="https://picsum.photos/1920/50?random"
//src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fbpic.588ku.com%2Fback_origin_min_pic%2F19%2F04%2F16%2F23f24c93f2d422fb10bb8984c8d6dc43.jpg&refer=http%3A%2F%2Fbpic.588ku.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1635598571&t=ff944a564803f1d871b2c4cd946bc661"

