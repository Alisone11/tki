<template>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />
  <div class="row menu-mobile d-flex justify-content-around w-100 m-0 ">
    <link-wrapper :location="'/'" class="col-3 link-color border-end">
      <div class=" d-flex flex-column mobile-menu-item align-items-center  ">
        <svg xmlns="http://www.w3.org/2000/svg" class="fa-2x p-2 " height="1em" viewBox="0 0 576 512">
            <path d="M575.8 255.5c0 18-15 32.1-32 32.1h-32l.7 160.2c0 2.7-.2 5.4-.5 8.1V472c0 22.1-17.9 40-40 40H456c-1.1 0-2.2 0-3.3-.1c-1.4 .1-2.8 .1-4.2 .1H416 392c-22.1 0-40-17.9-40-40V448 384c0-17.7-14.3-32-32-32H256c-17.7 0-32 14.3-32 32v64 24c0 22.1-17.9 40-40 40H160 128.1c-1.5 0-3-.1-4.5-.2c-1.2 .1-2.4 .2-3.6 .2H104c-22.1 0-40-17.9-40-40V360c0-.9 0-1.9 .1-2.8V287.6H32c-18 0-32-14-32-32.1c0-9 3-17 10-24L266.4 8c7-7 15-8 22-8s15 2 21 7L564.8 231.5c8 7 12 15 11 24z"/>
          </svg>
        <span>首頁</span>
      </div>
    </link-wrapper>

    <link-wrapper :location="'/'" class="col-3 link-color border-end">
      <div class="d-flex flex-column mobile-menu-item align-items-center">
        <span class="material-symbols-outlined p-2">book_online</span>
        <span>我的票券</span>
      </div>
    </link-wrapper>

    <link-wrapper :location="'/cart'" class="col-3 link-color border-end">
      <div class=" d-flex flex-column mobile-menu-item align-items-center ">
        <span class="material-symbols-outlined p-2">payments</span>
        <span>購票清單</span>
      </div>
    </link-wrapper>

    <link-wrapper :location="'/my-account'" class="col-3 link-color ">
      <div class="d-flex flex-column mobile-menu-item align-items-center">
        <font-awesome-icon class="fa-2x p-2 " :icon="['far', 'user-circle']" />
        <span>會員中心</span>
      </div>
    </link-wrapper>
  </div>
</template>
<script>

import LinkWrapper from "../../atoms/LinkWrapper/LinkWrapper.vue";
export default {
  components: { LinkWrapper },
};
</script>

<style scoped="scoped">
.material-symbols-outlined{
  font-size: 2em;
}
a.col-3.link-color{
  display: flex;
  justify-content: center;
  align-items: end;
}
a:hover path {
  fill: var(--primary-color);
}

.menu-mobile {
  background-color: #ffffff;
  overflow: hidden;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 9999;
}
.link-color {
  color:initial;
  text-decoration: none;
}
.p-2 {
  padding: 0.3rem !important;
}
.col-3 span:not(.material-symbols-outlined) {
  font-size: 12px !important;
  font-weight: 300 !important;
}
@media (max-width: 767.98px) {
.mobile-menu-item{
  padding:5px 0!important;
}
.mobile-menu-item span{
  font-weight:300;
}
}
@media screen and (min-width: 1024px) {
  .menu-mobile {
    display: none !important;
  }
}
@media screen and (min-width: 1600px) {
  .menu-mobile {
    display: none !important;
  }
}
@media screen and (min-width: 1900px) {
  .menu-mobile {
    display: none !important;
  }
}
</style>
