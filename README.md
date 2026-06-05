# AR setup for posters 
- AR asstets
  - videos hovering above the poster
  - 3D models
    - Molecular structures
    - Experimental setup
  - 3D animations
- QR-code with link to AR website serves as AR marker
- Touch controls (zoom and rotate)
- optimized to be used with mobile devices

## Asset structure
- Each AR asset is located in a seoarate subfolder
- Files
  - index.html: contains all controls and data
  - targets.mind: compiled AR marker (QR-code) using https://hiukim.github.io/mind-ar-js-doc/tools/compile/
  - AR content file
    - Video: mp4 file 
    - 3D model: glb format

## QR code marker
- create QR code URL link using https://5qr.net/
- add border (quiet zone) with a width of at least 4 small QR code squares
- save as png file
- compiled AR marker from QU code using https://hiukim.github.io/mind-ar-js-doc/tools/compile/
- save compiled marker as targets.mind

## AR asset
### Video
- Video has to be added as mp4 in github folder as video.mp4
- Video has to be loaded completely before replay, and kept in cache. Keep file size reasonable (< 100 MB) to minimize bload times
- embedding video streams from YouTube, Vimeo, etc. is not possible

## 3D model
- 3D models have to be converted to glb files with y-axis pointig upward

### Chemical structures from cif files
- clean structure and save as pdb or obj file
- import structure to Blender (extetions needed for importig pdb files)
- reduce number of objects/vertices
- export as glb file (keep file size reasonable, few MB)

## 3D Animation
to be added

## Main control file index.html
- Each asset folder contains one index.html
- can be modified using LLMs

## To do
- smart