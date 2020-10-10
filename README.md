# antdv-image-cropper

An image cropper component for Ant Design Vue [uploader](https://www.antdv.com/components/upload/). Based on [vue-cropper](https://github.com/xyxiao001/vue-cropper/blob/master/english.md) component.

[![npm](https://img.shields.io/npm/v/antdv-image-cropper.svg?style=flat-square)](https://www.npmjs.com/package/antdv-image-cropper)
[![npm bundle size](https://img.shields.io/bundlephobia/minzip/antdv-image-cropper?style=flat-square)](https://bundlephobia.com/result?p=antd-img-crop)

## Demo

[Live demo](https://codesandbox.io/s/antdv-image-cropper-mgs2h)

## Install

```sh
npm i antd-image-cropper
```

## Global registration

```
import Vue from 'vue'
import AImageCropper from 'antdv-image-cropper'

Vue.component('a-image-cropper', AImageCropper)
```

## Local registration

```
import AImageCropper from 'antdv-image-cropper'

export default {
    components: {
        AImageCropper
    },
    ...
```

## Props
You can use all props from **vue-cropper** component which are described [here](https://github.com/xyxiao001/vue-cropper/blob/master/english.md).
As well as properties small list of the component itself.

| Prop | Type | Default | Description |
| - | - | - | - |
| modalTitle | `String` | `Image editing` | Text that displayed into modal header |
| modalControl | `String` | `Save` | Text that displayed into crop button |
| modalWidth | `Number` | `610` | Width of modal window in pixels |
| containerWidth | `Number` | `520` | Width of cropper container in pixels |
| containerHeight | `Number` | `520` | Height of cropper container in pixels |

## License

[MIT License](https://github.com/nanxiaobei/antd-img-crop/blob/master/LICENSE) (c)