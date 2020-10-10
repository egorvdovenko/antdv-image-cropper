<template>
  <div id="app">
    <a-image-cropper
      :auto-crop="true"
      :fixed="true"
      :fixed-number="[2, 1]"
      output-type="png"
      @crop="onCrop"
    >
      <template #upload="{ beforeUpload }">
        <a-upload
          list-type="picture-card"
          :before-upload="beforeUpload"
          :show-upload-list="false"
          accept="image/jpeg, image/png"
        >
          <img
            v-if="imageUrl"
            :src="imageUrl"
            alt="imageUrl"
          />
          <div v-else>
            <a-icon type="plus" />
            Upload
          </div>
        </a-upload>
      </template>
    </a-image-cropper>
    <p
      style="color: green"
      v-if="imageUrl"
    >
      Your image has been succesfully cropped!
    </p>
  </div>
</template>

<script>
import AImageCropper from './components/AImageCropper.vue'

export default {
  name: 'App',
  components: {
    AImageCropper
  },
  data () {
    return {
      imageUrl: null
    }
  },
  methods: {
    onCrop (image) {
      this.imageUrl = URL.createObjectURL(image)
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
