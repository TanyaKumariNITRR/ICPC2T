<template>
  <div>
    <div class="object">
      <div class="object-rope"></div>
      <div class="object-shape">Coming <span class="soon">Soon</span></div>
    </div>

    <div class="content">


      <slot />
    </div>
  </div>
</template>
<script>
export default {
  name: "SUC",
  components: {},
};
</script>

<style scoped>
@keyframes sway {
  0% {
    transform: rotate(8deg);
  }
  50% {
    transform: rotate(-8deg);
  }
  100% {
    transform: rotate(8deg);
  }
}

.object {
  position: absolute;
  animation: sway 2.4s infinite;
  animation-timing-function: ease-in-out;
  -webkit-transform-origin: top;
  -moz-transform-origin: top;
  transform-origin: top;
  left: 0;
  right: 0;
  height: 5%;
  z-index: 999;
  text-transform: uppercase;
}

.object-shape {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  display: block;
  background-color: #2187c7;
  margin: 0 auto;
  position: relative;
  color: #fff;
  text-align: center;
  padding-top: 25px;
  font-weight: 800;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

.object-shape span {
  font-size: 22px;
  color: white;
}

.object-rope {
  height: 100%;
  width: 5px;
  background-color: #2187c7;
  content: "";
  display: block;
  margin-left: 50%;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 auto;
  max-width: 500px;
  padding: 35vh 20px 20px 20px;
}

.logo {
  max-width: 300px;
}

p {
  font-family: sans-serif;
  text-align: center;
}

.message {
  margin-top: 40px;
}
</style>
