<template>
  <v-container class="pa-0">
    <base-subheading>On Instagram</base-subheading>

    <v-row>
      <v-col
        v-for="(post, i) in posts"
        :key="i"
        cols="4"
      >
        <base-card
          :href="post.href"
          color="grey lighten-2"
          height="88"
          tag="a"
        >
          <v-img
            v-if="post.src"
            :src="require(`@/assets/instagram/${post.src}`)"
            height="100%"
          />
        </base-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'Instagram',

    data: () => ({
      posts: [
        {
          src: 'adventurealtitude.jpg',
          href: 'https://instagram.com/mahardikakdenie',
        },
        { src: 'garden.jpg', href: 'https://instagram.com/mahardikakdenie' },
        { src: 'pigduck.jpg', href: 'https://instagram.com/mahardikakdenie' },
        { src: 'rain.jpg', href: 'https://instagram.com/mahardikakdenie' },
        { src: 'spices.jpg', href: 'https://instagram.com/mahardikakdenie' },
        { src: 'sunset.jpg', href: 'https://instagram.com/mahardikakdenie' },
      ],
    }),
  }
</script>
