<template>
  <div>
    <welcome/>
    <!-- <recent-projects /> -->
    <experience-timeline />
    <skills />
    <about-me />
    <get-in-touch />
  </div>
</template>

<script>
export default {
  components: {
    AboutMe: () => import('@/components/AboutMe'),
    GetInTouch: () => import('@/components/GetInTouch'),
    ExperienceTimeline: () => import('@/components/ExperienceTimeline'),
    RecentProjects: () => import('@/components/RecentProjects'),
    Skills: () => import('@/components/Skills'),
    Welcome: () => import('@/components/Welcome')
  }
}
</script>
