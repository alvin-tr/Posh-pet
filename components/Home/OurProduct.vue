<template>
  <div class="bg-[#F2F3F7] pb-[180px]">
    <BaseLayout>
    <!-- title -->
    <div class="flex flex-row mt-[100px] items-center justify-between mb-[40px]">
      <p
        class="fontBebas uppercase text-[#DB2316] text-[120px] font-normal leading-[100px]"
      >
        our products
      </p>
      <div
        class="flex flex-row items-center py-[15px] px-[30px] rounded-[49px] bg-[#10131D1A]"
      >
        <p
          class="text-[14px] text-[#DB2316] font-[510] leading-[20px] mr-[2px]"
        >
          Discover
        </p>
        <UIcon
          name="mdi:arrow-top-right"
          class="text-[14px] text-[#DB2316] font-[510] leading-[20px]"
        />
      </div>
    </div>
    <!-- products -->
    <div class="grid grid-cols-3 gap-[50px]">
      <div
        v-for="items in products"
        class="bg-white px-[22px] pt-[20px] pb-[34px] max-w-[410px] w-[410px] rounded-[20px]"
      >
        <div
          :class="`flex items-center justify-center rounded-[9px] w-[366px] max-w-[366px] py-[79px] px-[56px]`"
          :style="{ backgroundColor: getBgColorOfProduct(index) }"
        >
          <img :src="items.img" alt="" />
        </div>
        <!-- title -->
        <div class="flex flex-row justify-between items-center mt-[30px]">
          <!-- des -->
          <div class="flex flex-col mr-[20px] w-[90%]">
            <p class="text-[#10131D] text-[26px] leading-[22px] font-[510]">
              {{ items.productsTitle }}
            </p>
            <p
              class="text-[#10131D80] text-[18px] leading-[28px] font-normal mt-[12px]"
            >
              {{ truncateText(items.productsDescription, 35) }}
            </p>
          </div>
          <!-- chat -->
          <div class="flex flex-col items-center w-[10%]">
            <div
              class="bg-[#10131D1A] p-[10px] flex items-center justify-center rounded-[20px]"
            >
              <UIcon
                name="solar:chat-round-line-outline"
                class="text-black text-[20px]"
              />
            </div>
            <p
              class="text-[#10131D80] text-[14px] leading-[20px] font-normal mt-[4px]"
            >
              15
            </p>
          </div>
        </div>
        <!-- price -->
        <div class="flex flex-row justify-between items-center mt-[26px]">
          <p class="text-[#DB2316] text-[26px] font-[510] leading-[22px]">
            ${{ formatPrice(items.price) }}
          </p>

          <div class="flex">
            <template
              v-for="(icon, index) in generateStars(items.star)"
              :key="index"
            >
              <UIcon
                v-if="icon === 'full'"
                name="ic:baseline-star"
                class="text-[#FFEAB6] text-[20px]"
              />
              <UIcon
                v-else-if="icon === 'half'"
                name="ic:baseline-star-half"
                class="text-[#FFEAB6] text-[20px]"
              />
            </template>
          </div>
        </div>
        <!-- Button buy now -->
        <div class="flex flex-row items-center justify-between mt-[32px]">
          <div
            class="w-[80%] bg-[#DB2316] py-[15px] flex items-center justify-center rounded-[10px]"
          >
            <p class="text-[20px] font-[510] leading-[32px]">BUY NOW</p>
          </div>
          <!-- bag -->
          <div
            class="bg-[#FFF6DB] rounded-[10px] p-[20px] flex items-center justify-center ml-[14px]"
          >
            <UIcon
              name="hugeicons:shopping-basket-02"
              class="text-[25px] text-[#DB2316]"
            />
          </div>
        </div>
      </div>
    </div>
  </BaseLayout>
  </div>
</template>

<script setup>
const products = [
  {
    img: '/img/products1.svg',
    productsTitle: 'PAWFECT CHEWS',
    productsDescription: 'Spoil your dog with our exciting new',
    price: '100000',
    star: '2',
  },
  {
    img: '/img/products2.svg',
    productsTitle: 'BARKY BITES',
    productsDescription: 'Discover the joy of our fresh dog treatments',
    price: '100000',
    star: '2.5',
  },
  {
    img: '/img/products3.svg',
    productsTitle: 'TAIL-WAGGERS TREATS',
    productsDescription: 'Introducing our latest canine delight',
    price: '100000',
    star: '3',
  },
  {
    img: '/img/products4.svg',
    productsTitle: 'FURRY FEAST SNACKS',
    productsDescription: 'Treat your pup to our new gourmet',
    price: '250000',
    star: '4.5',
  },
  {
    img: '/img/products5.svg',
    productsTitle: 'CANINE CRUNCHIES',
    productsDescription: 'Unleash happiness with our innovation',
    price: '100000',
    star: '5',
  },
  {
    img: '/img/products6.svg',
    productsTitle: 'WOOFERS DELIGHT',
    productsDescription: "Elevate your dog's snack time with flavor fullzilla",
    price: '100000',
    star: '2',
  },
]

function truncateText(text, maxLength) {
  return text.length > maxLength ? text.slice(0, maxLength) + '...' : text
}

// Hàm định dạng giá sản phẩm (USD)
function formatPrice(price) {
  const usdPrice = parseFloat(price) // Chuyển từ VND sang USD (giả định tỷ giá)
  return usdPrice.toFixed(2) // Làm tròn đến 2 số thập phân
}

// Hàm tạo danh sách icon sao
function generateStars(starCount) {
  const fullStars = Math.floor(starCount) // Số ngôi sao đầy
  const hasHalfStar = starCount % 1 !== 0 // Kiểm tra có nửa sao không

  const stars = Array(fullStars).fill('full') // Thêm các ngôi sao đầy
  if (hasHalfStar) {
    stars.push('half') // Thêm ngôi sao nửa
  }
  return stars
}

function getBgColorOfProduct(index) {
  const colors = [
    '#CFDFFF',
    '#FFEFBF',
    '#FFDED1',
    '#EDE2FE',
    '#CFDFFF',
    '#FFEAB6',
  ]
  return colors[index % colors.length]
}
</script>

<style scoped></style>
