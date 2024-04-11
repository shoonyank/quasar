<template>
  <q-layout>
    <div class="home-banner">
      <q-navbar class="bg-transparent viewport-container navbar">
        <q-toolbar class="flex justify-between">
          <img src="../assets/logo-white.png" class="navbar-logo">

          <div class="q-pa-md mobile-d-none">
            <q-btn-dropdown class="q-mr-xl" flat color="white" label="채용">
              <q-list>
                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>채용</q-item-label>
                  </q-item-section>
                </q-item>

                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>해외 개발자 원격 채용</q-item-label>
                  </q-item-section>
                </q-item>

                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>외국인 원격 채용 (비개발 직군)</q-item-label>
                  </q-item-section>
                </q-item>

                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>한국어 가능 외국인 채용</q-item-label>
                  </q-item-section>
                </q-item>
              </q-list>
            </q-btn-dropdown>
            <q-btn flat color="white" label="해외 개발자 활용 서비스" />
          </div>

          <q-btn color="white" class="mobile-d-none q-mb-md" text-color="primary" label="문의하기" />
        </q-toolbar>
      </q-navbar>

      <q-item class="banner-text viewport-container">
        <div class="col-sm-7 col-12">
          <div class="tooltip" v-if="showToolTip">
            풀타임, 파트타임!
          </div>
          <h3 class="banner-heading">최고의 실력을 가진 <br />외국인 인재를 찾고 계신가요?</h3>
          <h5 class="banner-caption">법률 및 인사관리 부담없이 <br />1주일 이내에 원격으로 채용해보세요.</h5>
          <q-btn flat color="white" class="banner-action-button mobile-d-none" label="개발자가 필요하신가요?" />

          <q-item class="banner-grid-view row q-pl-none justify-between mobile-d-none">
            <div class="col-3 grid-view-item">
              <h5 class="q-ma-none">평균 월 120만원</h5>
              <p>임금을 해당 국가를 기준으로 계산합니다.</p>
            </div>
            <div class="col-3 grid-view-item">
              <h5 class="q-ma-none">최대 3회 인력교체</h5>
              <p>막상 채용해보니 맞지 않아도 걱정하지 마세요.</p>
            </div>
            <div class="col-3 grid-view-item">
              <h5 class="q-ma-none">평균 3일, 최대 10일</h5>
              <p>급하게 사람이 필요한 경우에도 빠른 채용이 가능합니다.</p>
            </div>
          </q-item>
        </div>

        <div class="col-sm-5 col-12 hero-slider">
          <div class="tooltip-slider" v-if="showToolTip">
            풀타임, 파트타임!
          </div>
          <carousel :itemsToShow="3" :wrapAround="true">
            <slide :key="1">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
            <slide :key="2">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
            <slide :key="3">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
            <slide :key="4">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
            <slide :key="5">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
          </carousel>
        </div>
      </q-item>

      <div class="hero-bottom-slider viewport-container mobile-d-none">
        <carousel :items-to-show="2.5" :autoplay="5000" :wrap-around="true">
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>해외 마케팅</span>
          </slide>
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>퍼블리셔</span>
          </slide>
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>캐드원(제도사)</span>
          </slide>
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>해외 세일즈</span>
          </slide>
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>해외 CS</span>
          </slide>
        </carousel>
      </div>
    </div>

    <q-item class="footer-section">
      <q-item class="viewport-container justify-center row footer-section-head">
        <div class="col-sm-3 col-12">
          <img class="q-mb-sm" src="../assets/hyperhire-logo.png">
          <p class="extra-bold text-dark q-mb-md">우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.</p>
          <p class="extra-bold text-grey q-mb-md">010-0000-0000</p>
          <p class="extra-bold text-grey q-mb-md">aaaaa@naver.com</p>
        </div>
        <div class="col-sm-9 col-12 cards-row">
          <q-card class="footer-cards">
            <q-item>
              <q-item-section avatar>
                <img src="../assets/icons/code.png">
              </q-item-section>
            </q-item>

            <q-item class="no-min-height">
              <p class="extra-bold text-dark">해외 개발자 원격 채용</p>
            </q-item>

            <q-item class="no-min-height">
              <p class="extra-bold text-grey">바로가기</p>
              <img src="../assets/icons/arrow-right.png" class="card-right-arrow" />
            </q-item>
          </q-card>

          <q-card class="footer-cards">
            <q-item>
              <q-item-section avatar>
                <img src="../assets/icons/code.png">
              </q-item-section>
            </q-item>

            <q-item class="no-min-height">
              <p class="extra-bold text-dark">해외 개발자 원격 채용</p>
            </q-item>

            <q-item class="no-min-height">
              <p class="extra-bold text-grey">바로가기</p>
              <img src="../assets/icons/arrow-right.png" class="card-right-arrow" />
            </q-item>
          </q-card>

          <q-card class="footer-cards">
            <q-item>
              <q-item-section avatar>
                <img src="../assets/icons/code.png">
              </q-item-section>
            </q-item>

            <q-item class="no-min-height">
              <p class="extra-bold text-dark">해외 개발자 원격 채용</p>
            </q-item>

            <q-item class="no-min-height">
              <p class="extra-bold text-grey">바로가기</p>
              <img src="../assets/icons/arrow-right.png" class="card-right-arrow" />
            </q-item>
          </q-card>

          <q-card class="footer-cards">
            <q-item>
              <q-item-section avatar>
                <img src="../assets/icons/code.png">
              </q-item-section>
            </q-item>

            <q-item class="no-min-height">
              <p class="extra-bold text-dark">해외 개발자 원격 채용</p>
            </q-item>

            <q-item class="no-min-height">
              <p class="extra-bold text-grey">바로가기</p>
              <img src="../assets/icons/arrow-right.png" class="card-right-arrow" />
            </q-item>
          </q-card>
        </div>
      </q-item>

      <q-item class="viewport-container justify-center row footer-section-bottom">
        <div class="col-sm-3 col-12">
          <div class="flex justify-between">
            <p class="extra-bold text-dark">상호명</p>
            <p class="extra-bold text-dark">대표 CEO</p>
          </div>
          <div class="flex justify-between">
            <p class="extra-bold text-grey">하이퍼하이어</p>
            <p class="extra-bold text-grey">김주현</p>
          </div>
          <div class="flex justify-between">
            <p class="extra-bold text-grey">Hyperhire India Pvt Ltd</p>
            <p class="extra-bold text-grey">Juhyun Kim</p>
          </div>
        </div>
        <div class="col-sm-9 col-12 cards-row">
          <div class="footer-address">
            <p class="extra-bold text-dark">사업자등록번호 CIN</p>
            <p class="extra-bold text-grey">427-86-01187</p>
            <p class="extra-bold text-grey">U74110DL2016PTC290812 </p>
          </div>
          <div>
            <p class="extra-bold text-dark">주소 ADDRESS</p>
            <p class="extra-bold text-grey">서울특별시 강남대로 479, 지하 1층 238호 </p>
            <p class="extra-bold text-grey">D-138, Street number 11, Jagjeet Nagar, North East Delhi, New Delhi,
              110053 India </p>
          </div>
        </div>
      </q-item>
    </q-item>
  </q-layout>
</template>

<style>
@import 'animate.css';

* {
  font-family: "Poppins", sans-serif;
}

p {
  margin: 0px;
}

.viewport-container {
  padding-right: 20px;
  padding-left: 20px;
  margin-right: auto;
  margin-left: auto;
  width: 100%;
}

@media (min-width: 576px) {
  .viewport-container {
    max-width: 540px;
  }
}

@media (min-width: 768px) {
  .viewport-container {
    max-width: 720px;
  }
}

@media (min-width: 992px) {
  .viewport-container {
    max-width: 960px;
  }
}

@media (min-width: 1200px) {
  .viewport-container {
    max-width: 1140px;
  }
}

@media (min-width: 1400px) {
  .viewport-container {
    max-width: 1320px;
  }
}


.tooltip,
.tooltip-slider {
  position: relative;
  background-color: #ffffff;
  color: #40E2E8;
  text-align: center;
  padding: 10px 20px;
  border-radius: 8px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
  font-weight: bold;
  width: fit-content;
  animation: fadeIn;
  animation-duration: 300ms;
}

.tooltip-slider {
  background-color: #E9F7EF;
  color: #00C696;
  margin: auto;
}

.tooltip::after,
.tooltip-slider::after {
  content: '';
  position: absolute;
  bottom: -18px;
  left: 20px;
  transform: translateX(-50%);
  border-width: 10px;
  border-style: solid;
  border-color: #ffffff transparent transparent transparent;
  filter: drop-shadow(0 2px 2px rgba(0, 0, 0, 0.1));
}

.tooltip-slider::after {
  left: 60px;
}

.trigger:hover .tooltip {
  visibility: visible;
  opacity: 1;
}

.banner-text {
  display: flex;
  margin-top: 100px;
  color: #fff;
}

.banner-bottom-slider {
  width: 100%;
  height: 60px;
  top: 500px;
}

.banner-text .banner-heading {
  font-weight: 700;
  animation: fadeInUp;
  animation-duration: 500ms;
  margin-top: 20px;
  margin-bottom: 10px;
}

.banner-text .banner-caption {
  font-weight: 600;
  animation: fadeInUp;
  animation-duration: 500ms;
  margin-top: 20px;
  margin-bottom: 10px;
}

.banner-action-button {
  border-bottom: 1px solid #fff;
  border-radius: unset;
  padding: 0px;
}

.home-banner {
  background-image: url("../assets/banner-bg.png");
  min-height: 700px;
  background-size: cover;
  position: relative;
  display: flex;
  flex-direction: column;
}

.hero-bottom-slider {
  padding: 0;
  width: 100%;
  animation: fadeIn;
  animation-duration: 500ms;
}

.bottom-slider-slide {
  background-color: #FFFFFF20;
  border-radius: 8px;
  margin: 0px 15px;
  height: 48px;
  padding-left: 10px;
  width: 250px !important;
  justify-content: flex-start;
  color: #fff;
  font-weight: 700;
  font-size: 16px;
}

.bottom-slider-slide:first-child {
  margin-left: 0px;
}

.bottom-slider-slide img {
  width: 30px;
  margin-right: 10px;
}

.navbar-logo {
  width: 114px;
}

.banner-grid-view {
  margin-top: 50px;
  animation: fadeIn;
  animation-duration: 500ms;
}

.grid-view-item {
  border-top: 1px solid #fff;
}

.grid-view-item h5 {
  font-size: 18px;
}

.grid-view-item p {
  font-size: 16px;
}

.banner-bottom-slider {
  height: 68px;
  width: 80%;
  margin: auto;
}

.footer-section {
  display: block;
  padding: 100px 0px;
  background-color: #fbfbfb;
}

.cards-row {
  display: flex;
}

.footer-cards {
  box-shadow: unset;
  margin: 0px 20px;
  border-radius: 12px;
  width: 187px;
}

.card-right-arrow {
  width: 20px;
  height: 20px;
}

.card-title {
  font-weight: 600;
}

.no-min-height {
  min-height: unset;
}

.carousel__slide {
  padding: 5px;
}

.carousel__viewport {
  perspective: 2000px;
}

.carousel__track {
  transform-style: preserve-3d;
}

.carousel__slide--sliding {
  transition: 0.5s;
}

.carousel__slide {
  opacity: 0.9;
  transform: rotateY(-20deg) scale(0.9);
}

.carousel__slide--active~.carousel__slide {
  transform: rotateY(0deg) scale(0.85);
  z-index: -1;
}

.carousel__slide--prev {
  opacity: 1;
  transform: rotateY(0deg) scale(0.85);
}

.carousel__slide--next {
  opacity: 1;
  transform: rotateY(10deg) scale(0.85);
}

.carousel__slide--active {
  opacity: 1;
  transform: rotateY(0) scale(1);
}

.carousel__item img {
  width: 240px;
  height: 350px;
}

.extra-bold {
  font-weight: 900;
}

.text-grey {
  color: #5E626F !important;
}

.text-dark {
  color: #343741 !important;
}

.footer-address {
  margin: 0px 20px;
}

.hero-slider {
  animation: fadeIn;
  animation-duration: 500ms;
}

@media (max-width: 576px) {
  .mobile-d-none {
    display: none;
  }

  .banner-text {
    display: block;
  }

  .footer-section-head {
    display: block !important;
  }

  .cards-row {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: space-between;
  }

  .footer-cards {
    margin: 10px 0px;
    border-radius: 12px;
    width: 47%;
    font-size: 10px;
  }

  .footer-section-bottom {
    display: block;
  }

  .footer-address {
    margin-left: 0px;
    margin-bottom: 20px;
    margin-top: 20px;
  }

  .tooltip-slider {
    margin-top: 30px;
  }
}
</style>

<script setup>
import { ref, onMounted } from 'vue';
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

const showToolTip = ref(false);
onMounted(() => {
  setTimeout(() => {
    showToolTip.value = true;
  }, 500);

});

defineOptions({
  name: 'IndexPage',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
});
</script>
