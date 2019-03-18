<template>
  <section id="welcome" class="hide-overflow">
    <v-layout>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/profile.jpg')"
          height="100vh"
        />
      </v-flex>

      <v-flex
        xs12
        md6
        align-content-space-between
        layout
        :pa-5="$vuetify.breakpoint.smAndDown"
        wrap
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateY(25%)"
        />

        <v-layout
          align-center
          justify-center
        >
          <v-flex
            xs10
            md8
          >
            <base-heading>{{ name }}</base-heading>
            <base-subheading>{{ title }}</base-subheading>
            <base-text class="pb-5 mb-5">
              {{ intro }}
            </base-text>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  props: {
    name: String,
    title: String,
    intro: String
  }
}
</script>
