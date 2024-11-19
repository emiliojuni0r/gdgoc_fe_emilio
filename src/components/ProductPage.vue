<template>
  <div class="w-screen h-screen bg-[#FAFAFA] font-montserrat overflow-x-hidden">

    <!-- Content Container -->
    <div class="md:container md:px-36 mx-auto sm:mt-16 md:mt-28">
      <!-- Breadcrumb -->
      <div class="w-full h-24 bg-[#FAFAFA] flex flex-row items-center sm:justify-center md:justify-start gap-x-3">
        <p class="text-sm text-[#252B42] font-bold cursor-pointer">Home</p>
        <img src="@/assets/img/icon/breadcrumb_arrow.svg" alt="" />
        <p class="text-sm text-[#BDBDBD] font-bold cursor-pointer">Shop</p>
      </div>

      <!-- Main Product Container -->
      <div class="w-full h-fit flex sm:flex-col md:flex-row gap-x-3">
        <!--  -->
        <div class="sm:w-full md:w-[50%] h-full flex flex-col">
          <!-- main image container -->
          <div id="mainImage"
            class="relative sm:w-[348px] md:w-[490px] sm:h-[277px] md:h-[450px] sm:mx-auto bg-cover bg-no-repeat bg-center"
            :style="{ backgroundImage: `url(${currentImage})` }">
            <img src="@/assets/img/icon/arrow_display_product.svg" alt=""
              class="absolute right-8 bottom-28 cursor-pointer" @click="nextImage" />
            <img src="@/assets/img/icon/arrow_display_product.svg" alt=""
              class="absolute left-8 bottom-28 cursor-pointer rotate-180" @click="prevImage" />
          </div>

          <!-- thumbnail -->
          <div class="w-full h-fit flex flex-row gap-x-4 mt-5 sm:px-4 md:px-0">
            <img v-for="(image, index) in images" :key="index" :src="image" alt="thumbnail"
              class="thumbnail object-cover w-[100px] h-[75px] cursor-pointer" @click="setImage(image)" />
          </div>
        </div>

        <div class="sm:w-full md:w-[50%] h-full sm:px-6 md:pl-8 pt-4">

          <h1 class="text-[#252B42] font-medium text-xl">Floating Phone</h1>

          <!-- star n review container -->
          <div class="w-fit h-fit flex flex-row justify-between gap-x-1 items-center mt-3">
            <img src="@/assets/img/icon/icon_star_fill.svg" alt="" />
            <img src="@/assets/img/icon/icon_star_fill.svg" alt="" />
            <img src="@/assets/img/icon/icon_star_fill.svg" alt="" />
            <img src="@/assets/img/icon/icon_star_fill.svg" alt="" />
            <img src="@/assets/img/icon/icon_star_unfill.svg" alt="" />
            <p class="text-[#737373] text-sm font-bold ml-1.5">10 Reviews</p>
          </div>
          <h1 class="text-[#252B42] text-2xl font-bold mt-6">$1,139.33</h1>
          <h2 class="text-sm text-[#737373] font-bold mt-1.5">Availability : <span class="text-[#23A6F0]"> In
              Stock</span></h2>
          <p class="text-[#858585] text-sm font-medium mt-8 mb-4">Met minim Mollie non desert Alamo est sit cliquey
            dolor <br> do met sent. RELIT official consequent door ENIM RELIT Mollie. Excitation venial consequent sent
            nostrum met.</p>
          
            <!-- idk those line thing -->
          <hr class="border-b border-[#BDBDBD] mt-8">

          <!-- color container -->
          <div class="w-full h-fit flex flex-row justify-start gap-x-2.5 mt-8">
            <img src="@/assets/img/product/circle-blue.svg" alt="" />
            <img src="@/assets/img/product/circle-green.svg" alt="" />
            <img src="@/assets/img/product/circle-orange.svg" alt="" />
            <img src="@/assets/img/product/circle-dark-blue.svg" alt="" />
          </div>

          <!-- buttons container -->
          <div class="w-fit h-fit flex flex-row mt-14 gap-x-4">
            <!-- select options button -->
            <button
              class="w-36 h-11 text-white text-sm font-bold rounded-lg bg-[#23A6F0] hover:bg-[#2a81b3] focus:bg-[#2674a0]">select
              Options</button>
              <!-- fav button -->
            <button
              class="w-10 h-10 rounded-full border border-[#E8E8E8] bg-white hover:bg-slate-50 focus:bg-slate-100">
              <img src="@/assets/img/icon/icon_fav.png" alt="" class="m-auto" />
            </button>
            <!-- cart button -->
            <button
              class="w-10 h-10 rounded-full border border-[#E8E8E8] bg-white hover:bg-slate-50 focus:bg-slate-100">
              <img src="@/assets/img/icon/icon_cart_black.svg" alt="" class="m-auto" />
            </button>
            <!-- eye button -->
            <button
              class="w-10 h-10 rounded-full border border-[#E8E8E8] bg-white hover:bg-slate-50 focus:bg-slate-100">
              <img src="@/assets/img/icon/icon_eye.svg" alt="" class="m-auto" />
            </button>
          </div>
        </div>
      </div>
      <!-- end of main product container -->

      <!-- Best Sellers Products Container -->
      <div class="w-full h-full mt-14 flex flex-col sm:px-2 md:pl-10">

        <h1 class="text-[#252B42] font-bold sm:text-xl md:text-2xl sm:items-center sm:mx-auto md:mx-0">BESTSELLER
          PRODUCTS</h1>

        <hr class="sm:w-[80%] md:w-full mx-auto border-b-2 border-[#ECECEC] mt-4 mb-4" />

        <!-- products card container -->
        <div
          class="w-full h-auto grid sm:grid-cols-1 md:grid-cols-4 md:grid-rows-2 sm:gap-y-16 md:gap-x-3 md:gap-y-1 sm:pt-8 md:pt-0">

          <!-- cards product -->
          <div v-for="(product, index) in products" :key="index"
            class="w-[239px] h-[442px] sm:scale-110 md:scale-90 flex flex-col bg-white sm:mx-auto md:mx-0 hover:shadow-sm cursor-pointer">
            <img :src="product.image" alt="best seller img" class="w-full h-[280px] object-cover" />
            <div class="w-full h-full flex flex-col py-6 px-6 justify-start align-middle gap-y-3">
              <h5 class="text-[#252B42] text-base font-bold">{{ product.title }}</h5>
              <p class="text-[#737373] text-sm font-bold">{{ product.variant }}</p>
              <h5 class="text-[#BDBDBD] text-base font-bold ">{{ product.price }} <span class="text-[#23856D]">{{
                product.otherPrice }}</span></h5>
            </div>
          </div>
          <!-- cards product -->

        </div>
        <!-- end of products card container -->

      </div>

    </div>
    <!-- end of content container -->

  </div>
</template>

<script>
// import image for card products (best sellers sectionos)
import product1 from '@/assets/img/product/product1.png';
import product2 from '@/assets/img/product/product2.png';
import product3 from '@/assets/img/product/product3.png';
import product4 from '@/assets/img/product/product4.png';
import product5 from '@/assets/img/product/product5.png';
import product6 from '@/assets/img/product/product6.png';

// import image for main display and thumbnail
import img1 from '@/assets/img/product/carousel-item1.png'
import img2 from '@/assets/img/product/carousel-item2.jpg'
import img3 from '@/assets/img/product/carousel-item1.png'


export default {
  data() {
    return {
      currentImage: img1,
      images: [
        img2,
        img3,
      ],
      displayIndex: 0,
      // data for card products (best sellers section)
      products: [
        { title: 'Graphic Design', variant: 'English Department', price: '$16.48', otherPrice: '$6.48', image: product1 },
        { title: 'Graphic Design', variant: 'English Department', price: '$16.48', otherPrice: '$6.48', image: product2 },
        { title: 'Graphic Design', variant: 'English Department', price: '$16.48', otherPrice: '$6.48', image: product3 },
        { title: 'Graphic Design', variant: 'English Department', price: '$16.48', otherPrice: '$6.48', image: product4 },
        { title: 'Graphic Design', variant: 'English Department', price: '$16.48', otherPrice: '$6.48', image: product5 },
        { title: 'Graphic Design', variant: 'English Department', price: '$16.48', otherPrice: '$6.48', image: product6 },
        { title: 'Graphic Design', variant: 'English Department', price: '$16.48', otherPrice: '$6.48', image: product1 },
        { title: 'Graphic Design', variant: 'English Department', price: '$16.48', otherPrice: '$6.48', image: product2 },
      ],
    };
  },
  methods: {
    setImage(image) {
      this.currentImage = image;
    },
    nextImage() {
      this.displayIndex = (this.displayIndex + 1) % this.images.length;
      this.currentImage = this.images[this.displayIndex];
    },
    prevImage() {
      this.displayIndex = (this.displayIndex - 1 + this.images.length) % this.images.length;
      this.currentImage = this.images[this.displayIndex];
    },
  },
};
</script>

<style scoped>
.thumbnail {
  transition: opacity 0.3s;
}

.thumbnail:hover {
  opacity: 0.7;
}
</style>