<template>
<div>
     <v-navigation-drawer app fixed v-model="showMenu">
      <v-list dense>
        <v-list-item @click="">
          <v-list-item-action>
            <v-icon>settings</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item @click="">
          <v-list-item-action>
            <v-icon>help</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Help</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>


    <v-app-bar fixed app dark color="primary">
        <v-app-bar-nav-icon @click.stop="toggleMenu"></v-app-bar-nav-icon>
        <v-toolbar-title class="white--text">{{title}}</v-toolbar-title>
    </v-app-bar>
</div>
</template>
<script lang="ts">
import { Component, Vue} from 'vue-property-decorator';
import { Getter} from "vuex-class";

@Component
export default class TopToolbar extends Vue{
    @Getter("title", {namespace: "topToolbar"}) title!:string;
    showMenu: boolean = false;

    toggleMenu(): void {
        this.showMenu = !this.showMenu;
    }
}
</script>