<template>
      <div class="marquee-wrapper overflow-hidden relative bg-[#F2F3F7] py-[40px] z-50">
    <div class="marquee flex items-center space-x-[50px] relative ">
      <img
        v-for="(item, index) in logos"
        :key="index"
        :src="item.url"
        class="logo-item"
      />

      <img
        v-for="(item, index) in logos"
        :key="'repeat-' + index"
        :src="item.src"
        class="logo-item"
      />
    </div>
  </div>
</template>

<script setup>
    const logos = [
        {
            src: '/img/logoBrand/aspenLogo.svg'
        },
        {
            src: '/img/logoBrand/cropLogo.svg'
        },
        {
            src: '/img/logoBrand/nLogo.svg'
        },
        {
            src: '/img/logoBrand/missyLogo.svg'
        },
        {
            src: '/img/logoBrand/peppermintLogo.svg'
        },
        {
            src: '/img/logoBrand/pixieLogo.svg'
        }
    ]
</script>

<style scoped>
.marquee-wrapper {
  width: 100%;
  overflow: hidden;
  position: relative;
}

.marquee {
  display: flex;
  align-items: center;
  gap: 50px;
  animation: marquee-animation 10s linear infinite;
}

@keyframes marquee-animation {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-50%);
  }
}

.logo-item {
  width: 500px;
  height: auto;
  margin-block: 20px;
}

@media (max-width: 425px) {
  .marquee-wrapper {
    margin-block: 20px;
  }
  .marquee {
    gap: 5px;
  }
  .logo-item {
    width: 100px;
  }
}

@media (max-width: 641px) {
  .marquee-wrapper {
    margin-block: 20px;
  }
  .marquee {
    gap: 5px;
  }
  .logo-item {
    width: 100px;
  }
}
</style>