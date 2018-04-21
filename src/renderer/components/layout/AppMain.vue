<!--
  @TAG:APPLAYOUT:APPMAIN
  This component implements router-view
-->

<template>
  <section class="eva-shell-appmain-container Vue-AppMain">
    <router-view :key="$route.fullPath"></router-view>
  </section>
</template>