<template>
  <v-carousel hide-controls hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
</template>
<script>
  export default {
    data () {
      return {
        items : [
          {
            src: require('@/assets/first/BlueFilterTitleImage3.jpg')
          },
          {
            src: require('@/assets/first/Parallax_notext.jpg')
          },
          {
            src: require('@/assets/first/installation_31_medical_museum.jpg')
          }
        ]
      }  
    }
  }
</script>

