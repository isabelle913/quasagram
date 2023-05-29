<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar class="constrain">
        <q-btn size="18px" icon="eva-camera-outline" class="large-screen-only q-mr-sm" to="/camera" dense flat round/>
        <q-separator class="large-screen-only" inset vertical spaced />
        <q-toolbar-title class="text-grand-hotel text-bold">
          Quasagram
        </q-toolbar-title>
        <q-btn size="18px" icon="eva-home-outline" class="large-screen-only q-ml-sm" to="/" dense flat round/>

      </q-toolbar>
    </q-header>

    <q-footer class="bg-white small-screen-only" bordered>
      <q-tabs class="text-grey-10" active-color="primary" indicator-color="transparent">
        <q-route-tab to="/" icon="eva-home-outline" />
        <q-route-tab to="/camera" icon="eva-camera-outline"/>
      </q-tabs>
    </q-footer>


    <q-page-container class="bg-grey-1">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>


</script>

<style lang="scss" >

.q-toolbar{
  @media (min-width: $breakpoint-sm-min){
    height: 77px;
  }
}

.q-toolbar__title{
  font-size: 30px;

  @media (max-width: $breakpoint-xs-max){
    text-align: center;
  }

}

.q-footer{
  .q-tab__icon{
    font-size: 30px;
  }
}

</style>
