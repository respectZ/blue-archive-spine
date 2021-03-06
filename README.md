# blue-archive-spine
For viewing Blue Archive Spines.

Have a look at [this branch](https://github.com/respectZ/blue-archive-spine/tree/resourceless) for resourceless.

# Requirements
- [decrunch](https://github.com/HearthSim/decrunch/)
- [fsb5](https://github.com/HearthSim/python-fsb5)
- [lz4](https://github.com/python-lz4/python-lz4)
- [Pillow](https://python-pillow.org/)
- [astc_decomp](https://github.com/K0lb3/astc_decomp/)
- MSVC++ 14.0 Build Tools with Windows 10 SDK

# Setup
## Building UnityPack
```
setup.py build
```
## Installing UnityPack
```
setup.py install
```
or
```
setup.py install --user
```

# Downloading Models
```
py/getModels.py
```
Downloaded Models located at ./downloaded_resource

Assets (Spine and Audio) located at ./assets

# Generating JSON Data
## data/audio.json
```
py/generateAudioJson.py
```
This will download VOC_JP audio instead of playing it directly (cors issue ?)

To play audio directly from BA's server, change py/generateModelsJson.py
```python
_type = 1
```
to
```python
_type = 0
```
## data/models.json
```
py/generateModelsJson.py
```
## And you're done!
Just launch index.html

## Used Libraries
- [pixi.js](https://pixijs.com/)
- [pixi-spine](https://github.com/pixijs/spine)
- [howler.js](https://howlerjs.com/)
- [UIKit](https://getuikit.com/)

Big Kudos for awesome [UnityPack](https://github.com/HearthSim/UnityPack)