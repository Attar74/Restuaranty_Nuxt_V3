<template>
  <NuxtLayout name="custom">
    <div>
      <Html lang="en-US">
        <Head>
          <Title>Restaurntly</Title>
          <Meta name="discription" content="This is a cool page"/>
          <Link rel="preload" href="https://ih1.redbubble.net/image.1849445085.4826/raf,360x360,075,t,fafafa:ca443f4786.jpg" as="script"/>
        </Head>
      </Html>
      <div class="text-center">
        <h1 class="mt-5">Welcom to Restaurantly</h1>
        <NuxtLink to="/restaurants"> Go to restaurants</NuxtLink>
      </div>
    </div>
  </NuxtLayout>
</template>
