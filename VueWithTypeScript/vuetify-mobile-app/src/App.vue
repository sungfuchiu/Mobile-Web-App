<template>
  <v-app>
    <!--<v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Vuetify</span>
        <span class="font-weight-light">MATERIAL DESIGN</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <HelloWorld/>
    </v-content>-->
    <TopToolbar></TopToolbar>

    <v-content>
      <router-view></router-view>
    </v-content>
    
    <BottomNav></BottomNav>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue} from 'vue-property-decorator';
import TopToolbar from './components/TopToolbar.vue';
import BottomNav from './components/BottomNav.vue';

@Component({
  components:{
    TopToolbar,
    BottomNav
  }
})
export default class extends Vue{

}

// import Vue from 'vue';
// import HelloWorld from './components/HelloWorld.vue';

// export default Vue.extend({
//   name: 'App',
//   components: {
//     HelloWorld,
//   },
//   data: () => ({
//     //
//   }),
// });
</script>
