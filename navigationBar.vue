<template>
  <div class="nav">
    <nav class="breadcrumb-container" aria-label="breadcrumbs">
      <div class="flex justify-between items-center">
        <!-- 로고를 왼쪽에 배치 -->
        <div class="flex items-center space-x-2">
          <img
            src="@/assets/img/Logo_orange.png"
            alt="STNI Logo"
            class="logo"
          />
          <div class="flex flex-col all-text">
            <!-- Flexbox를 사용하여 세로 정렬 -->
            <span class="font-bold text-lg">에스티앤아이</span>
            <span class="text-small">Smart Technology & Innovation</span>
          </div>
          <!-- 로고 옆에 텍스트 추가 -->
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavigationBar",
};
</script>

<style scoped>
.breadcrumb-container {
  background-color: rgba(212, 209, 209, 0.861);
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.nav {
  margin-top: 0px;
  width: 100%;
}
.text-small {
  font-size: 7.5px;
  font-weight: 900px;
}
.logo {
  height: 14;
  margin-left: 7px;
}
.all-text {
  margin-left: 0px; /* 텍스트와 로고 사이의 간격을 최소화 */
  line-height: 1; /* 텍스트 사이의 줄 간격을 줄임 */
}
</style>
