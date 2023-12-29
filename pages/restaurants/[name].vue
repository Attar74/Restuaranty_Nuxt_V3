<template>
  <div>
    <div v-if="restaurant" class="restaurant-container">
      <div class="image-container">
        <img :src="restaurant?.imageUrl" alt="" />
      </div>
      <div class="info-container">
        <h1>{{ restaurant?.name }}</h1>
        <div class="stats-container">
          <h5>Revenue (in billions)</h5>
          <p>${{ restaurant?.revenue }}</p>
        </div>
        <div class="stats-container">
          <h5>Number of Stores</h5>
          <p>{{ restaurant?.numberOfStores }}</p>
        </div>
        <p class="content">{{ restaurant?.content }}</p>
      </div>
    </div>
    <div class="text-center d-flex h-90" v-else>
      <div class="my-auto mx-auto">
        <NuxtLayout name="error">
          <template #header>
            <h1 class="mb-4">Page Not Found!!</h1>
          </template>
          <div>
            <img
              class="error"
              src="https://ih1.redbubble.net/image.1849445085.4826/raf,360x360,075,t,fafafa:ca443f4786.jpg"
              alt=""
            />
          </div>
          <a href="/restaurants"> Go Back</a>
        </NuxtLayout>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import restaurants from "@/data.json";


const route = useRoute();
const name = route.params.name;

const restaurant = restaurants.find((r) => r.name === name);

useHead({
  title: restaurant ? restaurant?.name : '404 - Restaurant Not Found',
  meta: [{ name: 'description', content: 'My amazing site.' }]
})

</script>

<style scoped>
.h-90 {
  height: 90vh;
}
.restaurant-container {
  display: flex;
}
.image-container {
  width: 100%;
  height: 95vh;
}
.image-container img {
  width: 100%;
  height: 100%;
}
.restaurant-not-found {
  height: 75vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.info-container {
  padding: 3rem;
  width: 50%;
}
.info-container h1 {
  text-transform: uppercase;
  font-size: 6rem;
  margin-bottom: 3rem;
}
.stats-container {
  display: flex;
  align-items: flex-end;
  margin-bottom: 1rem;
}
.stats-container h5 {
  width: 20rem;
  font-size: 2rem;
  margin: 0;
  margin-right: 5rem;
}
.stats-container p {
  font-size: 2rem;
  margin: 0;
}
.content {
  font-size: 1.5rem;
  margin-top: 4rem;
}

img.error {
  max-width: 10rem;
}
</style>
