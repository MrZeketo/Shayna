<template>
  <div class="product">
    <HeaderShayna />
        <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="breadcrumb-text product-more">
                        <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section End -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src="gambar_besar" alt="" />
                            </div>
                            <div class="product-thumbs">
                                <carousel class="product-thumbs-track ps-slider "  :auto-play="true">
                                    <div class="pt" @click="ubahGambar(thumbs[0])" 
                                    :class="thumbs[0] == gambar_besar ? 'active':'' ">
                                        <img src="img/product-single/product-1.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="ubahGambar(thumbs[1])"
                                    :class="thumbs[1] == gambar_besar ? 'active':'' ">
                                        <img src="img/product-single/product-2.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="ubahGambar(thumbs[2])"
                                    :class="thumbs[2] == gambar_besar ? 'active':'' ">
                                        <img src="img/product-single/product-3.jpg" alt="" />
                                    </div>
                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details">
                                <div class="pd-title">
                                    <span>oranges</span>
                                    <h3>Pure Pineapple</h3>
                                </div>
                                <div class="pd-desc">
                                    <p>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id accusantium! Autem.
                                    </p>
                                    <p>
                                        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur.
                                        Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
                                        Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                                        impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                                    </p>
                                    <h4>$495.00</h4>
                                </div>
                                <div class="quantity">
                                    <router-link to="ShopingCart" class="primary-btn pd-cart">Add To Cart</router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->

    
    <RelatedShayna />
    <PartnerShayna />
    <FooterShayna />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShayna from '@/components/HeaderShayna.vue'
import RelatedShayna from '@/components/RelatedShayna.vue'
import PartnerShayna from '@/components/PartnerShayna.vue'
import FooterShayna from '@/components/FooterShayna.vue'
import carousel from 'vue-owl-carousel'

export default {
  name: 'Product',
  components: {
    // HelloWorld
    HeaderShayna,
    RelatedShayna,
    PartnerShayna,
    FooterShayna,
    carousel
  },
    data() {
    return{
      gambar_besar:"img/products/product-3.jpg",
      thumbs:[
          "img/product-single/product-1.jpg",
          "img/product-single/product-2.jpg",
          "img/product-single/product-3.jpg"
      ]
    }
  },
  methods:{
      ubahGambar(berubah){
          this.gambar_besar=berubah;
      }
  }
};
</script>

<style scoped>
    .product-details{
    text-align: left;
    }
    .breacrumb-section{
    text-align: left;
    }
    .product-thumbs .pt{
        margin-right: 14px;
    }
</style>