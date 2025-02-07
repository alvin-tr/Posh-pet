<template>
    <div class="w-full bg-[#F2F3F7] pb-[92px] px-[80px]">
        <BaseLayout>
            <div class="flex flex-col items-center justify-center">
                <p class="fontBebas text-[#DB2316] text-[120px] font-normal leading-[100px]">WHY CHOOSE US?</p>
                <div class="mt-[80px] grid grid-cols-3 gap-[40px]">
                    <div v-for="item in items" class="flex flex-col items-center justify-center">
                        <img :src="item.icon" alt="">
                        <p class="text-[20px] text-[#10131D] my-[24px] leading-[32px]">{{ item.title }}</p>
                        <p class="text-[#10131D80] text-[14px] leading-[20px] font-normal text-center">{{ item.des }}</p>
                    </div>
                </div>
            </div>
        </BaseLayout>
    </div>
</template>

<script setup>
import BaseLayout from '../BaseLayout.vue';

const items = [
    {
        icon: '/icon/earth.svg',
        title: 'GLOBAL DELIVERY',
        des: 'Experience Hassle-Free Shipping and Seamless Global Connectivity with Our Trustworthy and Efficient Delivery Service, Bringing the World to Your Fingertips!'
    },
    {
        icon: '/icon/box.svg',
        title: 'FREE SHIPPING',
        des: "Shop to Your Heart's Content Without Worrying About Shipping Costs: Our Free Shipping Service Delivers Your Purchases with a Smile, Straight to Your Doorstep!"
    },
    {
        icon: '/icon/phone.svg',
        title: '24/7 SUPPORTING',
        des: 'Shop with Confidence Anytime, Anywhere: Our Free Shipping Service Comes with 24/7 Support to Ensure Your Packages Arrive Safely and On Time!'
    },
    {
        icon: '/icon/email.svg',
        title: 'DAILY EMAIL',
        des: 'Stay Up-to-Date with Your Deliveries: Enjoy the Convenience of Daily Email Updates with Our Free Shipping Service, Making Your Online Shopping Experience Even More Enjoyable!'
    },
    {
        icon: '/icon/creditCard.svg',
        title: 'EASY PAYMENT',
        des: 'Shop and Pay with Ease: Our Free Shipping Service Not Only Delivers Your Packages for Free, but Also Offers Easy Payment Options, Making Your Shopping Experience a Breeze!'
    },
    {
        icon: '/icon/huyChuong.svg',
        title: 'MONTHLY  VOUCHER',
        des: 'More Than Just Free Shipping: Our Service Rewards Your Loyalty with Monthly Vouchers, Giving You More Reasons to Shop and Save on Your Favorite Products!'
    },
]

</script>

<style lang="scss" scoped>

</style>