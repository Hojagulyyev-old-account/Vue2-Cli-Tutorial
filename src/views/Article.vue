<template>
  <div class="about">
    <h1>This is an <span>article</span> page</h1>
    <div class="spiner">
      <breeding-rhombus-spinner
      :animation-duration="2000"
      :size="100"
      color="#3cac8a"
      />
    </div>
  </div>
</template>

<script>

import {BreedingRhombusSpinner} from 'epic-spinners';

export default {
  components: {
    BreedingRhombusSpinner
  }
}
</script>

<style lang="css" scoped>
h1 {
  font-size:45px;
}
span {
  color: #3cac8a
}
.about {
  text-align: center;
}
.spiner {
  position: absolute;
  margin: auto;
  left: 50%;
  top: 40%;
  transform: translate(-50%, -50%);
}
</style>
