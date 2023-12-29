<template>
  <div>
    <Html lang="en-US">
        <Head>
          <Title>Top 50 Restaurants in the world</Title>
          <Meta name="discription" content="This is a cool page"/>
          <Link rel="preload" href="https://ih1.redbubble.net/image.1849445085.4826/raf,360x360,075,t,fafafa:ca443f4786.jpg" as="script"/>
        </Head>
      </Html>
    <NuxtLayout name="custom">
      <div>
        <div class="container">
          <h1 class="text-center my-5">Restaurants</h1>
          <restaurantTable />
        </div>
      </div>
    </NuxtLayout>
  </div>
</template>
