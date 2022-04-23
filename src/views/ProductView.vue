<style scoped>
.product-thumbs .pt {
  margin-right: 14px;
}
</style>

<script>
import HeaderShayna from "@/components/HeaderShayna.vue";
import FooterShayna from "@/components/FooterShayna.vue";
import RelatedShayna from "@/components/RelatedShayna.vue";
import BreadcrumbShayna from "@/components/BreadcrumbShayna.vue";

import carousel from "vue-owl-carousel-cg";

export default {
  name: "ProductView",
  components: {
    HeaderShayna,
    FooterShayna,
    RelatedShayna,
    carousel,
    BreadcrumbShayna,
  },
  data() {
    return {
      activePhoto: 0,
      thumbs: [
        {
          id: 1,
          img: "img/mickey1.jpg",
        },
        {
          id: 2,
          img: "img/mickey2.jpg",
        },
        {
          id: 3,
          img: "img/mickey3.jpg",
        },
        {
          id: 4,
          img: "img/mickey4.jpg",
        },
      ],
    };
  },
  methods: {
    changeImage(x) {
      this.activePhoto = x;
    },
  },
};
</script>

<template>
  <div class="product">
    <HeaderShayna />

    <!-- Breadcrumb Section Begin -->
    <BreadcrumbShayna nameLink="Detail" />
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img :src="thumbs[activePhoto].img" :key="thumbs[activePhoto].id" alt="" class="product-big-img" />
                </div>
                <div class="product-thumbs">
                  <carousel :dots="false" :nav="false" class="product-thumbs-track ps-slider">
                    <div v-for="(thumb, index) in thumbs" :key="thumb.id">
                      <div class="pt" :class="{ active: index == activePhoto }" @click="changeImage(index)">
                        <img :src="thumb.img" alt="" />
                      </div>
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
                      Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi,
                      id accusantium! Autem.
                    </p>
                    <p>
                      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti
                      cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur. Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus
                      voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores. Commodi ratione distinctio harum voluptatum velit
                      facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? a exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam impedit
                      praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                    </p>
                    <h4>$495.00</h4>
                  </div>
                  <div class="quantity">
                    <router-link to="/cart" class="primary-btn pd-cart">Add To Cart</router-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Product Shop Section End -->

    <!-- Related Products Section End -->
    <RelatedShayna />
    <!-- Related Products Section End -->

    <FooterShayna />
  </div>
</template>
