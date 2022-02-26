<template>
  <div>
    <!-- OK時の画像 -->
    <div
      v-if="childUrl"
    >
      <h2>OK!!!</h2>
      <img
        :src="childUrl"
        width=200
      >
    </div>
    <!-- NG時の画像 -->
    <div
      v-else
    >
      <h2>NG...</h2>
      <img
        src="../assets/no-image.png"
        width=200
      >
    </div>
  </div>
</template>

<script>
export default {
  props: {
    url: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      childUrl: '',
    }
  },
  beforeCreate() {
    console.log('beforeCreate: ', this.childUrl);
    // const newUrl = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg==';
    // this.childUrl = newUrl;
    // console.log('beforeCreate: ', this.childUrl);
  },
  created() {
    console.log('created: ', this.childUrl);
    // const newUrl = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg==';
    // this.childUrl = newUrl;
    // console.log('created: ', this.childUrl);
  },
  beforeMount() {
    console.log('beforeMount: ', this.childUrl);
    // const newUrl = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg==';
    // this.childUrl = newUrl;
    // console.log('beforeMount: ', this.childUrl);
  },
  mounted() {
    console.log('mounted: ', this.childUrl);
    // const newUrl = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg==';
    // this.childUrl = newUrl;
    // console.log('mounted: ', this.childUrl);
  },
  methods: {
    getUrl() {
      console.log('methods(getUrl): ', this.childUrl);
      // const newUrl = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg==';
      // this.childUrl = newUrl;
      // return this.childUrl;
    }
  }
}
</script>
