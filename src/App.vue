<template>
  <div id="app" class="exercise-1 canvas">
    <div class="parkspot-info-wrapper">
      <display direction="⬆" place="0" name="P1" />
      <display direction="⮕" place="55" name="P2" />
      <display direction="⬅" place="101" name="P3" />
      <display direction="⬆" place="110" name="P4" />
    </div>
  </div>
</template>

<script>
import display from "./components/display";
export default {
  components: { display },
  name: "App",
};
</script>

<style scoped>
.exercise-1.canvas {
  font-family: Tahoma, Helvetica, sans-serif;
}

.parkspot-info-wrapper {
  background-color: #34495e;
  padding: 10px;
  display: inline-block;
}

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
