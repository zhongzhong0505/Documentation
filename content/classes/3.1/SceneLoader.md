---
ID_PAGE: 25211
PG_TITLE: SceneLoader
PG_VERSION: 2.1
TAGS:
    - Scene
---
## Description

class [SceneLoader](/classes/3.1/SceneLoader)



## Members

### static NO_LOGGING : number


### static MINIMAL_LOGGING : number


### static SUMMARY_LOGGING : number


### static DETAILED_LOGGING : number


### static ForceFullSceneLoadingForIncremental : boolean


### static ShowLoadingScreen : boolean


### static loggingLevel : number


### static CleanBoneMatrixWeights : boolean


### static OnPluginActivatedObservable : [Observable](/classes/3.1/Observable)&lt;ISceneLoaderPlugin&gt;


### ISceneLoaderPluginAsync : undefined


### ISceneLoaderPluginAsync : undefined


### ISceneLoaderPluginFactory : undefined


### ISceneLoaderPluginAsync : undefined


### ISceneLoaderPluginAsync : undefined


### ISceneLoaderPluginAsync : undefined


## Methods

### static GetPluginForExtension(extension) &rarr; ISceneLoaderPlugin



#### Parameters
 | Name | Type | Description
---|---|---|---
 | extension | string | 

### static RegisterPlugin(plugin, ISceneLoaderPluginAsync) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | plugin | ISceneLoaderPlugin or ISceneLoaderPluginAsync | 
### static ImportMesh(meshNames, rootUrl, sceneFilename, scene, onSuccess, onProgress, onError, pluginExtension) &rarr; Nullable&lt;ISceneLoaderPlugin&gt;

Import meshes into a scene

#### Parameters
 | Name | Type | Description
---|---|---|---
 | meshNames | any |  an array of mesh names, a single mesh name, or empty string for all meshes that filter what meshes are imported
 | rootUrl | string |  a string that defines the root url for scene and resources
 | sceneFilename | string |  a string that defines the name of the scene file. can start with "data:" following by the stringified version of the scene
 | scene | [Scene](/classes/3.1/Scene) |  the instance of BABYLON.[Scene](/classes/3.1/Scene) to append to
optional | onSuccess | Nullable&lt;(meshes: [AbstractMesh](/classes/3.1/AbstractMesh)[], particleSystems: [ParticleSystem](/classes/3.1/ParticleSystem)[], skeletons: [Skeleton](/classes/3.1/Skeleton)[]) =&gt; void&gt; |  a callback with a list of imported meshes, particleSystems, and skeletons when import succeeds
optional | onProgress | Nullable&lt;(event: ProgressEvent) =&gt; void&gt; |  a callback with a progress event for each file being loaded
optional | onError | Nullable&lt;(scene: [Scene](/classes/3.1/Scene), message: string, exception: any) =&gt; void&gt; |  a callback with the scene, a message, and possibly an exception when import fails
### static Load(rootUrl, sceneFilename, engine, onSuccess, onProgress, onError, pluginExtension) &rarr; Nullable&lt;ISceneLoaderPlugin&gt;

Load a scene

#### Parameters
 | Name | Type | Description
---|---|---|---
 | rootUrl | string |  a string that defines the root url for scene and resources
 | sceneFilename | any |  a string that defines the name of the scene file. can start with "data:" following by the stringified version of the scene
 | engine | [Engine](/classes/3.1/Engine) |  is the instance of BABYLON.[Engine](/classes/3.1/Engine) to use to create the scene
optional | onSuccess |  | scene | [Scene](/classes/3.1/Scene) | 

 |  a callback with the scene, a message, and possibly an exception when import fails
optional | onProgress |  | event | ProgressEvent | 
optional | onError |  | scene | [Scene](/classes/3.1/Scene) | 
 | message | string | 
optional | exception | any | 
### static Append(rootUrl, sceneFilename, scene, onSuccess, onProgress, onError, pluginExtension) &rarr; Nullable&lt;ISceneLoaderPlugin&gt;

Append a scene

#### Parameters
 | Name | Type | Description
---|---|---|---
 | rootUrl | string |  a string that defines the root url for scene and resources
 | sceneFilename | any |  a string that defines the name of the scene file. can start with "data:" following by the stringified version of the scene
 | scene | [Scene](/classes/3.1/Scene) |  is the instance of BABYLON.[Scene](/classes/3.1/Scene) to append to
optional | onSuccess |  | scene | [Scene](/classes/3.1/Scene) | 

 |  a callback with the scene, a message, and possibly an exception when import fails
optional | onProgress |  | event | ProgressEvent | 
optional | onError |  | scene | [Scene](/classes/3.1/Scene) | 
 | message | string | 
optional | exception | any | 
