<template>
  <div>
    <v-btn
      v-for="(item, i) in items.slice(0, large ? items.length : 3)"
      :key="i"
      fab
      class="ma-2"
      :large="large"
      color="deep-orange darken-4"
      :href="item.href"
      target="blank"
    >
      <v-icon
        color="white"
        v-text="item.icon"
      />
    </v-btn>
  </div>
</template>

<script>
export default {
  props: {
    large: {
      type: Boolean,
      default: false
    }
  },

  data: () => ({
    items: [
      {
        name: 'Twitter',
        icon: 'mdi-twitter',
        href: 'https://twitter.com/kelishrestha'
      },
      {
        name: 'Instagram',
        icon: 'mdi-instagram',
        href: 'https://www.instagram.com/kelishrestha/'
      },
      {
        name: 'Facebook',
        icon: 'mdi-facebook',
        href: 'https://facebook.com/keli.shrestha'
      },
      {
        name: 'Email',
        icon: 'mdi-email',
      },
      {
        name: 'Phone',
        icon: 'mdi-phone'
      }
    ]
  })
}
</script>
