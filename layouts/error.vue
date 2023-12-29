<template>
  <div>
    <div class="text-center d-flex h-90">
      <div class="my-auto mx-auto">
        <slot name="header" />
        <div>
          <img
            src="https://ih1.redbubble.net/image.1849445085.4826/raf,360x360,075,t,fafafa:ca443f4786.jpg"
            alt=""
            class="error"
          />
        </div>
        <a href="/restaurants"> Go Back</a>
      </div>
    </div>
  </div>
</template>
<style>
img.error {
  max-width: 10rem;
}

.h-90 {
  height: 90vh;
}
</style>
