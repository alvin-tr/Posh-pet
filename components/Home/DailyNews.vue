<template>
    <div class="w-full z-50 relative ">
        <img src="/img/shapeInDailyNews.svg" class="mt-[-500px] object-cover w-full">
        <div class="flex items-center justify-between bg-[#FFF6DB] px-[80px] pt-[120px]">
            <p class="fontBebas text-[#DB2316] text-[120px] leading-[100px]">Daily news</p>
            <div class="bg-[#10131D1A] flex flex-row items-center px-[40px] py-[16px] rounded-full">
                <p class="text-[#DB2316] text-[14px] mr-[2px]">Discover</p>
                <UIcon name="mdi:arrow-top-right" class="text-[#DB2316] text-[14px]"/>
            </div>
        </div>
        <!-- swiper -->
        <div class="mt-[48px] pb-[50px]">
            <SwiperDailyNews/>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>