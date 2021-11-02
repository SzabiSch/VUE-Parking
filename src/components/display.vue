<template>
  <div class="parkspot-info" :class="checkPalceStyle">
    <div class="parkspot-info__arrow">{{ direction }}</div>
    <div class="parkspot-info__free-spaces">
      <span class="parkspot-info__count">{{ place }}</span>
      <span class="parkspot-info__count-label">Freie Plätze</span>
    </div>
    <div class="parkspot-info__name">{{ name }}</div>
  </div>
</template>

<script>
export default {
  name: "display",
  props: {
    place: { type: Number, default: 0 },
    direction: { type: String },
    name: { type: String },
  },
  computed: {
    checkPalceStyle() {
      if (this.place == 0) {
        return "parkspot-info--out";
      } else if (this.place < 10) {
        return "parkspot-info--few";
      } else {
        return false;
      }
    },
  },
};
</script>

<style scoped>
.parkspot-info {
  background-color: #3498db;
  color: #fff;
  width: 600px;
  display: flex;
  width: 380px;
  justify-content: center;
  align-items: center;
  padding: 0 40px;
  border: 2px solid #fff;
}

.parkspot-info--few {
  background-color: #f9ca24;
}

.parkspot-info--out {
  background-color: #eb4d4b;
}

.parkspot-info__arrow {
  font-size: 5rem;
}

.parkspot-info__free-spaces {
  margin: 0 40px;
}

.parkspot-info__count {
  font-family: Tahoma, Helvetica, sans-serif;
  display: block;
  font-size: 2.9rem;
  background-color: #34495e;
  color: #fff200;
  padding: 0px 0px 0px 5px;
  text-align: center;
  letter-spacing: 0.5rem;
}

.parkspot-info__count-label {
  display: block;
  text-align: center;
}

.parkspot-info__name {
  font-weight: bold;
  font-size: 7rem;
}
</style>
