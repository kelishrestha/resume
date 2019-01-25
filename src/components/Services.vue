<template>
  <section
    id="services"
    class="hide-overflow"
  >
    <v-layout accent>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/services.png')"
          height="100%"
        />
      </v-flex>
      <v-flex
        xs12
        md6
        text-xs-center
        pa-5
      >
        <v-layout
          align-center
          justify-center
          fill-height
          wrap
        >
          <v-flex xs12>
            <base-bubble-2
              style="transform: translateX(55%)"
            />
            <base-heading class="info--text">
              Services
            </base-heading>

            <base-text class="mb-5">
              Curabitur venenatis tortor erat, quis laoreet nis<br>
              lobortis eget. Fusce tempor aucto.
            </base-text>
          </v-flex>
          <v-flex
            v-for="(service, i) in services"
            :key="i"
            md6
            text-xs-center
            mb-3
          >
            <v-avatar
              class="elevation-6 mb-2"
              color="#69A1BB"
              size="64"
              tile
            >
              <v-icon
                dark
                size="52"
                v-text="service.icon"
              />
            </v-avatar>
            <base-text>
              <div
                class="mb-2"
                v-text="service.name"
              />
              <div v-html="service.blurb" />
            </base-text>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    services: [
      {
        name: 'Research',
        icon: 'mdi-clipboard-text-outline',
        blurb: 'Curabitur et nisi semper,<br> pellent e sque '
      },
      {
        name: 'Design',
        icon: 'mdi-pencil-outline',
        blurb: 'Curabitur et nisi semper, <br>pellent.'
      },
      {
        name: 'Development',
        icon: 'mdi-settings-outline',
        blurb: 'Curabitur et nisi semper, <br>pellent.'
      },
      {
        name: 'Support',
        icon: 'mdi-account',
        blurb: 'Curabitur et nisi semper, <br>pellent.'
      }
    ]
  })
}
</script>
