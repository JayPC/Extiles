# Extiles
2D Tilesheet Extruder

### Electron app
To use the electron app first run `npm i` to install npm dependencies and then `npm start` to start the electron app during development. To make a build run `npm run bundle` to build all platforms or `npm run bundle-x86_64-windows`, `npm run bundle-x86_64-mac` to build the respective platforms. 

### Instructions:
1. Put your image file somewhere in the local folder(like the img folder in the root)
2. Add **?img=** to the URL. For example **?img=GrassTiles.png**
3. The default is 16, if the tiles are larger than 16x16 add **&spriteSize=** and set the value. For example **&spriteSize=32** for 32x32
4. The default extrude is 1px, if larger is needed set the **&extrudeSize=** to the number of pixels to extrude. For example **&extrudeSize=3** will extrude 3 pixels in each direction

### Optional instructions:
* Add **?showAnimation=true** to the URL, To show an animation of how it draws the sprites(default is false)
* Add **?animationTime=** to the URL, To change the delay in milliseconds the animation uses(default is 60)

To save, right on the generated image and save it!

# About Extiles
This tool was originally created to fix a bug I had with Unity where tiles would bleed pixels into other tiles because they were right next to each other. This solves the issue by extruding the pixels so you can slice the tiles with offsets and padding.

This is what the problematic sheet looks like:

![Issue Tile](https://i.imgur.com/E3Y3zHH.png "Optional title")

Original vs Extiled Sprite:

![Original Sprite](https://i.imgur.com/R2aNmrY.png)
![Extiled Sprite](https://i.imgur.com/zhw4tCy.png)

Sliced in Unity:

![Original Sprite](https://i.imgur.com/w3emAou.png)
![Original Sprite](https://i.imgur.com/vWuh6ef.png)

Same Tile Before and After Extiles:

![In Game Appearance](https://i.imgur.com/zaeAYhs.png "Optional title")
