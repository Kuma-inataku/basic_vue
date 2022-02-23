<template>
  <div>
    <ImageChildComponent
      :url="url"
      @replace="replaceUrl"
    ></ImageChildComponent>
  </div>
</template>

<script>
import ImageChildComponent from './ImageChildComponent.vue'

export default {
  components: {
    ImageChildComponent
  },
  data() {
    return {
      url: '',
    }
  },
  methods: {
    replaceUrl(newUrl) {
      console.log(newUrl);
      this.url = newUrl;
    },
  }
}
</script>
