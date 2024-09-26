<template>
  <div class="grid-container">
    <span col>
      <span low>
        <span col>
          <div class="grid">
            <card-rect
              :image="require('@/assets/img/MainCardImage/image1.png')"
              title="First Card"
              content="This is the first card."
              @click.native="goToDigitalTwin('First Card')"
            />
            <card-rect
              :image="require('@/assets/img/MainCardImage/image2.png')"
              title="Second Card"
              content="This is the second card."
              @click.native="handleCardClick('Second Card')"
            />
          </div>
        </span>
      </span>
      <span low>
        <div class="grid">
          <card-rect
            :image="require('@/assets/img/MainCardImage/image3.png')"
            title="Third Card"
            content="This is the third card."
            @click.native="handleCardClick('Third Card')"
          />
          <card-rect
            :image="require('@/assets/img/MainCardImage/image4.png')"
            title="Fourth Card"
            content="This is the fourth card."
            @click.native="handleCardClick('Fourth Card')"
          />
        </div>
      </span>
    </span>
  </div>
</template>

<script>
import CardRect from "@/components/CardRect.vue";

export default {
  name: "RectGrid",
  components: {
    CardRect,
  },
  methods: {
    goToDigitalTwin(title) {
      const targetRoute = { name: "DigitalTwin", params: { title } };

      // 현재 경로와 이동할 경로 비교
      if (
        this.$route.name !== targetRoute.name ||
        this.$route.params.title !== title
      ) {
        this.$router.push(targetRoute).catch((err) => {
          if (!err.message.includes("NavigationDuplicated")) {
            console.error(err);
          }
        });
      }
    },
  },
};
</script>

<style scoped>
.grid-container {
  position: absolute;
  display: grid;
  justify-items: center;
  align-items: center;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
  padding: 20px;
}
</style>
