<template>
  <div class="overflow-hidden bg-white rounded-lg">
    <div class="relative bg-red-400 pb-2/3">
      <img
        class="absolute object-top w-full h-full"
        :src="propss.imageUrl"
        :alt="propss.title"
      />
    </div>
    <div class="p-4">
      <div class="flex items-baseline">
        <span
          class="inline-block px-2 py-0 text-xs font-semibold tracking-wide text-blue-600 uppercase bg-blue-200 rounded-full"
        >
          New
        </span>
        <div
          class="ml-2 text-xs font-semibold tracking-wide text-gray-600 uppercase"
        >
          {{ propss.beds }} beds &bull; {{ propss.baths }} baths
        </div>
      </div>
      <h1 class="mt-1 text-lg font-semibold truncate">{{ propss.title }}</h1>
      <div class="mt-1">
        {{ propss.price }} <span class="text-sm text-gray-600">/ wk</span>
      </div>
      <div class="flex items-center mt-2">
        <svg
          v-for="i in 5"
          :key="i"
          :class="i <= propss.rating ? ' text-blue-500' : 'text-gray-400'"
          class="w-5 h-5 fill-current"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
          fill="currentColor"
        >
          <path
            d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"
          />
        </svg>
        <span class="ml-2 text-sm text-gray-600">
          {{ propss.reviewCount }} reviews
        </span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["propss"],
};
</script>
