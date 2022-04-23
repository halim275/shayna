<script>
export default {
  name: "BreadcrumbShayna",
  props: {
    nameLink: String,
  },
};
</script>

<template>
  <div class="breacrumb-section">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <div class="breadcrumb-text product-more">
            <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
            <span>{{ nameLink }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
