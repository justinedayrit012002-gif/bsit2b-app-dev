<template>
  <v-app>
    
     <v-navigation-drawer v-model="drawer" :rail="rail" permanent >
        <template v-slot:prepend>
          <v-list-item
            lines="two"
            prepend-avatar="https://static.wikia.nocookie.net/ageofempires/images/1/14/AoMRT_Greek_Zeus.webp/revision/latest/scale-to-width/360?cb=20250701110532"
            subtitle="Logged in"
            title="justine dayrit"
          ></v-list-item>
        </template>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-home-city" title="Home" value="home"></v-list-item>
          <v-list-item prepend-icon="mdi-account" title="My Account" value="account"></v-list-item>
          <v-list-item prepend-icon="mdi-account-group-outline" title="Users" value="users"></v-list-item>
        </v-list>
        
      </v-navigation-drawer>
      
      <v-app-bar :elevation="2" color="blue">
  <template v-slot:prepend>
    <v-app-bar-nav-icon @click="rail = !rail"></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Application Bar</v-app-bar-title>
</v-app-bar>
       <v-main>
        <v-container fluid>
    <slot />
      </v-container >
      </v-main>
  </v-app>
</template>

<script setup>
const drawer = ref(true)
const rail = ref(true)
</script>

<style>

</style>