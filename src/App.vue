<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from '@/components/HelloWorld.vue'
import LogoutView from './views/LogoutView.vue'
import HomeView from './views/HomeView.vue';
import DashboardSkeleton from './views/DashboardSkeletonView.vue'

</script>

<template>
  <RouterView /> 
</template>