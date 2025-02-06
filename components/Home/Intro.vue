<template>
  <div class="mt-[88px] w-full flex flex-col items-center justify-center ">
    <div class="bg-[#FFF6DB] relative z-10 max-size-xl:px-[80px] max-size-2xl:px-[120px]">
      <p
        class="fontBebas text-[232px] leading-[200px] text-[#DB2316] text-center
        
        "
      >
        Pawfectly Yours
      </p>
      <!-- button -->
      <div class="flex flex-row items-end justify-end max-size-2xl:mt-[50px]">
        <UButton class="px-[20px] py-[15px] bg-white rounded-full">
          <p class="text-[#DB2316] text-[20px] leading-[32px] font-[510]">
            OUR PRODUCT
          </p>
        </UButton>
        <UButton
          class="px-[20px] py-[15px] bg-[#DB2316] rounded-full ml-[16px]"
        >
          <p class="text-white text-[20px] leading-[32px] font-[510]">
            BOOK SERVICE
          </p>
        </UButton>
      </div>
      <!-- dog and des-->
      <div
        class="w-full absolute left-0 flex flex-row
        max-size-xl:px-[80px] max-size-xl:top-[120px]
        max-size-2xl:px-[120px] max-size-2xl:top-[200px]
        "
      >
        <img
          src="/img/dogInSectionHome.svg"
          class="w-[75%] h-full object-cover"
        />
        <p
          class="uppercase text-[18px] text-[#10131D] font-[510] text-end w-[25%] mt-[572px]"
        >
          Where every paw finds<br />unconditional love and care.
        </p>
      </div>
    </div>
    <div class="z-50 relative w-full mt-[530px] max-size-2xl:mt-[700px]">
      <img src="/img/sectionHomeBehindDog.svg" class="w-full" />
    </div>
  </div>
</template>

<script setup></script>

<style scoped></style>
