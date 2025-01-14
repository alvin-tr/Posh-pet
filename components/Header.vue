<template>
  <div class="w-full bg-[#F4E8C3] flex justify-center">
    <div
      class="max-w-[1440px] w-full bg-[#F4E8C3] px-[80px] h-[72px] flex flex-row justify-between
      max-size-lg:px-[50px]
      max-size-lg1:px-[30px]
      "
    >
      <!-- section 1 -->
      <div class=" h-full flex flex-row items-center">
        <img src="/img/logoRemoveBg.png" class="h-[100px] w-[100px]" />
        <p
          class="text-[30px] text-[#DB2316] font-medium ml-[-10px] 
          max-size-xl05:text-[25px]
          max-size-lg:hidden
          ">
          Posh pet
        </p>
        <div class="ml-[60px] h-full flex items-center max-size-lg:ml-[20px] max-size-md:hidden">
          <p class="text-[14px] leading-[20px] font-[510] text-[#10131D]">
            Services
          </p>
        </div>
        <div class="ml-[72px] h-full flex items-center max-size-lg:ml-[20px] max-size-md:hidden">
          <p class="text-[14px] leading-[20px] font-[510] text-[#10131D]">
            Product
          </p>
        </div>
      </div>
      <!-- section 2 -->
      <div class=" h-full flex flex-row items-center max-size-md:hidden">
        <!-- search -->
        <div class="w-[60%] min-w-[150px] flex flex-row border-b-[2px] border-[#E8DCBA]
        max-size-lg:w-[50%] 
        ">
          <UIcon name="mdi-light:magnify" class="text-[#DB2316] text-[30px]" />
          <UInput
            variant="none"
            placeholder="Search products"
            class="text-[#10131D80] w-full"
            maxLength="50"
          />
        </div>
        <!-- cart -->
        <div
          class="flex items-center justify-center border-[2px] w-[40px] h-[40px] border-[#E8DCBA] bg-white rounded-full ml-[20px] p-[10px]"
        >
          <UIcon name="mdi-light:cart" class="text-[20px] text-[#DB2316]" />
        </div>
        <!-- Sign in -->
        <div class="w-[60%] bg-[#DB2316] ml-[12px] px-[30px] py-[10px] rounded-full flex items-center justify-center
        max-size-xl1:w-[30%]
        max-size-lg:w-[40%]
        ">
          <p class="font-[510] text-white">Sign In</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const inputValue = ref('')
</script>

<style scoped></style>
