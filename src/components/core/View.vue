<template>
  <div>
    <welcome
      name="Kelina Shrestha"
      title="Ruby on Rails Engineer"
      intro="Self-motivated, dedicated and organized software engineer pursuing professional experience in technology with an aim to solve problems with technology. Collaborative team player uplifting performance of applications and team to achieve targeted goals accepting challenges."
    />
    <!-- <recent-projects /> -->
    <experience-timeline />
    <services />
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
    Services: () => import('@/components/Services'),
    Welcome: () => import('@/components/Welcome')
  }
}
</script>
