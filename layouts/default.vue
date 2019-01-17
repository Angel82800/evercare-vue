<template>
  <v-app>
    <v-toolbar
      color="#114B34"
      height="100"
      class="nav"      
      app
    >
      <v-toolbar-title>
        <v-layout align-center column class="logo">
          <h2>EVERCARE</h2>
          <span>FAMILY FIRST</span>
        </v-layout>
      </v-toolbar-title>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-layout class="botton-group">
          <v-btn color="#00AF7C" class="nav-btn" disabled>Managed Care</v-btn>
          <v-btn color="#00AF7C" class="nav-btn" >Become a Carer</v-btn>
          <v-btn color="#00AF7C" class="nav-btn" disabled >Sign In</v-btn>
          <v-btn color="#00AF7C" class="nav-btn" disabled >Sign Up</v-btn>
        </v-layout>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      <v-menu class="hidden-md-and-up" flat>
        <v-toolbar-side-icon slot="activator" color="white"></v-toolbar-side-icon>
        <v-list>
          <v-list-tile>
            <v-list-tile-content>
              <v-list-tile-title>Managed Care</v-list-tile-title>
             </v-list-tile-content>
          </v-list-tile>
          <v-list-tile>
            <v-list-tile-content>
              <v-list-tile-title>Become a Carer</v-list-tile-title>
             </v-list-tile-content>
          </v-list-tile>
          <v-list-tile>
            <v-list-tile-content>
              <v-list-tile-title>Sign In</v-list-tile-title>
             </v-list-tile-content>
          </v-list-tile>
          <v-list-tile>
            <v-list-tile-content>
              <v-list-tile-title>Sign Up</v-list-tile-title>
             </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-menu>
      <v-menu offset-y flat>
        <v-btn slot="activator" class="menu-button" flat>
          <v-avatar
            color="grey lighten-4 avatar"
          >
            <img src="https://vuetifyjs.com/apple-touch-icon-180x180.png" alt="avatar">
          </v-avatar>
          <p class="hidden-sm-and-down">Lorem Ipsum</p>
          <i class="material-icons">
            expand_more
          </i>
        </v-btn>
        <v-list>
          <v-list-tile>
            <v-list-tile-title>Profile</v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-menu>
    </v-toolbar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer
      app
    >
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>
<style lang="scss" scoped>
.nav {
  color: white;
  font-family: sans-serif;
  .v-btn {
    text-transform: initial;
  }
  .logo {
    letter-spacing: 2px;
    h2 {
      font-size: 20px;
    }
    span {
      font-size: 10px;
    }
  }

  .botton-group {
    button {
      margin: 6px 8px!important;
      height: 36px!important;
      color: white!important;
    }
    margin-left: 10%;
  }
  
  .nav-btn {
    color: white;
  }
  .avatar {
    height: 100%;
  }
  p {
    margin: 0px 10px 0 10px;
    color: white;
  }
  i {
    color: white;
  }
  .menu-button {
      &.has-icon .btn__content {
        padding: 6px;
      }
      &.has-text .btn__content {
        padding: 16px;
      }
      height: fit-content;
  }
}

</style>

<script>
export default {
  data() {
    return {
      dropdown_font: ['Arial', 'Calibri', 'Courier', 'Verdana']
    }
  }
}
</script>
