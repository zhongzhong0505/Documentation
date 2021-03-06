---
PG_TITLE: How To Use the Default Rendering Pipeline
---

# Introduction

You can find a complete example of this pipeline in our playground : [https://www.babylonjs-playground.com/#5XB8YT#1](https://www.babylonjs-playground.com/#5XB8YT#1)

The default rendering pipeline provides visual improvements to enhance the output of your scene:
* Depth of field
* Antialiasing
* Bloom
* Image processing including:
 * Vignette effect
 * Contrast
 * Exposure
 * Color curves
 * Color grading
 * Tone mapping

# Creating the rendering pipeline

You just have to create an instance of BABYLON.DefaultRenderingPipeline
```
var pipeline = new BABYLON.DefaultRenderingPipeline(
    "default", // The name of the pipeline
    true, // Do you want HDR textures ?
    scene, // The scene instance
    [camera] // The list of cameras to be attached to
);
```

# Customizing

## Depth of field
You can turn the depth of field effect on and off with:

```
pipeline.depthOfFieldEnabled = true;
```

Set the strength of blur with (Higher may affect performance):

```
pipeline.depthOfFieldBlurLevel = BABYLON.DepthOfFieldEffectBlurLevel.Low;
```

Furthermore, you can control the settings of the effect with the following parameters:
```
pipeline.depthOfField.focusDistance  = 2000;
pipeline.depthOfField.focalLength  = 50;
pipeline.depthOfField.fStop  = 1.4;
pipeline.depthOfField.lensSize  = 50;
```
[Demo](https://www.babylonjs-playground.com/index.html#JA1ND3#56)

## Antialiasing
You can turn the antialiasing (fxaa) effect on and off with:

```
pipeline.fxaaEnabled = true;
```

## Bloom
You can turn the bloom effect on and off with:

```
pipeline.bloomEnabled = true;
```

Furthermore, you can control the impact of bloom in the final compositing with:
```
pipeline.bloomWeight = 0.3;
```


## Image processing effect
You can turn the image processing effect on and off with:

```
pipeline.imageProcessingEnabled = true;
```

You can also control individual image processing subeffects. To get more info about the ImageProcessing postprocess, please read the following [tutorial](/How_To/how_to_use_postprocesses#imageprocessing).


