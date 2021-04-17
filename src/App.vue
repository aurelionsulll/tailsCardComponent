<template>
  <div class="antialiased text-gray-900">
    <div class="flex items-center justify-center min-h-screen p-8 bg-gray-200">
      <card-component :propss="propss" />
    </div>
  </div>
</template>
<script>
import CardComponent from "./components/CardComponent.vue";
export default {
  name: "app",
  components: {
    CardComponent,
  },
  data() {
    return {
      title: String,
      propss: {
        imageUrl: "stephan.jpg",
        title:
          "Modern executive home in the heart of historic London in the great br",
        beds: 3,
        baths: 2,
        price: "$1,900.00",
        rating: 4,
        reviewCount: 32,
      },
    };
  },
};
</script>
