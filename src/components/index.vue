<template>
    <div>
        <div class="jumbotron">
            <h1 class="display-3">Color Palettes</h1>
            <p class="lead">This is a sample demo page that displays the color palettes from the npm plugin <a href="https://github.com/Jam3/nice-color-palettes">nice-color-palettes</a>
            </p>
            <p>Please head over to their documentation for the usage and more information! <a href="https://github.com/Jam3/nice-color-palettes">https://github.com/Jam3/nice-color-palettes</a></p>
        </div>
        <div id="colors-container">
            <div class="row">
                <div v-for="(palette, index) in colorPalettes" :key="index" class="color-row col-sm-3 mb-4">
                    <div v-for="(color, index2) in palette" :key="index2" class="p-2" :style="{'background-color': color}">{{color}}</div>
                </div>
            </div>
            
        </div>
    </div>
</template>

<script>
import ColorPalettes from 'nice-color-palettes'

export default {
  created () {
  },
  data () {
    return {
      colorPalettes: ColorPalettes
    }
  }
}
</script>

<style>
#colors-container
{
    margin-top: 20px;
}

#colors-container > .color-row:not(:last-child) {
    margin-bottom: 20px;
}

#colors-container > .color-row:not(:last-child) > .row > div {
    padding: 5px 20px;
}
</style>
