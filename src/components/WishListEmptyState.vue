<template>
  <div
    class="w-full h-screen flex flex-col items-center justify-center gap-6"
    v-if="WishlistStore.favouritesCount === 0"
  >
    <h2
      class="font-[avenir-bold] text-3xl lg:text-4xl flex items-center text-center"
    >
      You have nothing on your wishlist :|
    </h2>
    <router-link to="/catalog">
      <p class="link font-[avenir-medium] text-base lg:text-lg">
        Catalog &rarr;
      </p>
    </router-link>

    <img
      src="../assets/images/favoritesEmpty.svg"
      class="h-[12rem] lg:h-[20rem]"
      alt="empty cart"
    />
  </div>
</template>

<script setup lang="ts">
import useWishlistStore from "@/stores/WishlistStore";
const WishlistStore = useWishlistStore();
</script>

<style scoped></style>
