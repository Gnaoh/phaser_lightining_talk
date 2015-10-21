<img src="http://phaser.io/images/img.png">

<img src="http://phaser.io/images/github/jump.jpg" align="right">

##What is Phaser?

Phaser is an open source HTML5 game framework created by Photon Storm. It's designed to create games that will run on desktop and mobile web browsers. A lot of focus was given to performance inside of mobile web browsers, a growing and important area of web gaming. If the device is capable then it uses WebGL for rendering, but otherwise it seamlessly reverts to Canvas. 

####What is canvas you ask? 
The HTML <canvas> element is used to draw graphics, on the fly, via scripting (usually JavaScript). The <canvas> element is only a container for graphics.



##What Platforms Can I Target With Phaser?

###Desktop Browsers
Phaser is a JavaScript library designed to run on all major desktop browsers. This includes Internet Explorer 9 and above, Firefox, Chrome, and Safari. Prior to IE9 it didn't support canvas, so if you absolutely need a framework that can handle DOM rendering then Phaser won't be suitable. However, demand for these types of games are becoming next to minimal; if anything, it's shifting the other direction (towards WebGL).

###Mobile Browsers
On mobile, Phaser runs on iOS5 and above inside of Mobile Safari. On Android, it runs in 2.2 and above in both the stock browser and in Chrome. Chrome is now the standard Android browser, with recent versions even supporting WebGL, but you still can't ignore the millions of legacy Android devices that remain in use.


##Key Features

###It's Just Plain JavaScript
This may sound like a strange 'feature', but it should actually be quite a compelling one. Phaser doesn't use any faux OO-style practises internally. There's no massive inheritance chain or component system, and you don't have to force your objects into any fixed class structure, either. It's a simple straight-forward prototype chain, the way JavaScript was meant to be used.

This doesn't mean you can't build your game in a structured way; far from it. All it means is that we don't enforce it. It also means that Phaser is internally very easy to hack around with.


###Easy Asset Loading
Phaser has a built-in asset Loader that can handle:

*Images

*Sprite Sheets (fixed sized frames)

*Texture Atlases (including Texture Packer, JSON Hash, JSON Array, Flash CS6/CC, and Starling XML formats)

*Audio files

*Data Files (XML, JSON, plain text)

*JavaScript files (so you can part-load your games or JS based resources)

*Tilemaps (CSV and Tiled map formats)

*Bitmap Fonts

We routinely export texture atlas files from Flash directly to our Phaser games, and it supports fully trimmed atlases. Assets can be part-loaded, cached, and pulled from different URLs (for CDN support), and you can even turn any sprite into a progress bar with a single line of code.

###Rendering: WebGL and Canvas

Internally, Phaser uses Pixi.js for rendering. Pixi is a great, fast rendering library that focuses on Canvas and WebGL. It's a library we continue to contribute towards to help push things forward.

For your games, this means that if the browser supports WebGL then the player will more often than not get a smoother experience. WebGL is common on desktop but still emerging on mobile; even so, it is where HTML5 games are headed in the future, so supporting it is vital. The latest release of Phaser introduced WebGL shader and filter support, and forthcoming ones will implement normal maps so you can benefit from new tools like Sprite Lamp.

###Audio: Web Audio and Legacy Audio
Audio has been one of the weakest points of HTML games for a long time. Only a couple of years ago, we were faced with the choice of having one single channel of high-latency audio that would cripple the device during playback or having no audio at all. But times have changed, and the Web Audio API came to our salvation. It allows for proper node-based audio support, with multiple channels, node routing and all kinds of effects. So Phaser fully supports Web Audio.

However, on Android especially, lots of devices still don't support thi—so we also support legacy Audio and the use of Audio Sprites: the method of packing a bunch of samples together into a single file and using playback markers to jump to different effects. Phaser will swap between the two depending on the device capabilities and also includes unlocking the audio sub-system automatically for you, something that catches out a lot of first-time mobile devs!

###Input: Multi-Touch, Keyboard, Pointer, Mouse
When supporting desktop and mobile there are an increasingly varied number of potential input options. Phaser supports keyboard, mouse, touch, MSPointer (now Pointer under IE11), and combinations thereof. For example, on Windows Surface devices you could swap between using a mouse and touch, or indeed use both together.

For touch input, Phaser copes with both single-touch and multi-touch environments. You can define up to 10 touch points and track them all independently, using their events to handle Sprite interactions such as dragging, tapping, and collision.

###Physics, Tweens, and Particles
Bundled into the core library are the ArcadePhysics and ArcadeParticles systems. These are simple AABB light-weight libraries that allow you to apply gravity and motion to any Sprite, then test for collision and separation. Using a world-based quadtree to help minimise collision tests, you can achieve decent results quickly with little processing time required.

###Plugins
It is our aim that the core of Phaser will eventually settle down and hit a nice stable equilibrium, where we're not likely to touch it much beyond fixes and browser updates. However, we want Phaser to carry on growing, providing features for all kinds of games but without causing the core library to explode in growth. To this end, we've built in a plugin system.

Phaser plugins can register themselves with the core framework, be updated in line with the core game loop, and perform all kinds of useful additional tasks. A great example of this is the recently released EasyStar path finding plugin. We will be releasing plugins ourselves and expect to see more coming from the community in the future.



However, we understand that this won't suit all types of games, so the physics system is easy to replace and none of the physics properties are bound to actual sprites (but rather to a body component), so can be swapped out for the likes of Box2D or p2.js. A tweening system is also built-in, allowing you to tween objects or properties easily. And should the game pause, then all of your tweens will pause automatically and resume as needed.


## Integrating Phaser

* Clone the git repository via https://github.com/photonstorm/phaser

### Bower / npm

Install via [bower](http://bower.io)

`bower install phaser`

Install via [npm](https://www.npmjs.com)

`npm install phaser`

### CDN

[jsDelivr](http://www.jsdelivr.com/#!phaser) is a "super-fast CDN for developers". Include the following in your html:

`<script src="//cdn.jsdelivr.net/phaser/2.4.4/phaser.js"></script>`

or the minified version:

`<script src="//cdn.jsdelivr.net/phaser/2.4.4/phaser.min.js"></script>`

[cdnjs.com](https://cdnjs.com/libraries/phaser) also offers a free CDN service. They have all versions of Phaser and even the custom builds:

`<script src="https://cdnjs.cloudflare.com/ajax/libs/phaser/2.4.4/phaser.js"></script>`

##How do you use it? Is there a "cheatsheet" you made others can reference?
Yes, please refer for the "cheatsheet.html" file.


