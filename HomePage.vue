<template>
  <div class="container">
    <img
      class="image-size slide-in"
      alt="Sliding Image"
      src="@/assets/img/GstarCad.jpg"
      :class="{ 'slide-active': isScrolled }"
    />
  </div>
</template>

<script>
export default {
  name: "HomePage",
};
</script>

<style scoped>
.container {
  overflow-x: hidden;
}
.image-size {
  width: 1000px;
  height: auto;
  margin-left: 0px;
}

/* 이미지가 우측에서 슬라이드로 들어오는 효과 */
.slide-in {
  transform: translateX(100%);
  transition: transform 1s ease-in-out;
  opacity: 0;
}

.slide-active {
  transform: translateX(0);
  opacity: 1;
}
</style>
