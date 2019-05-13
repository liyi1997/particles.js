## particles.js

### A lightweight JavaScript library for creating particles.

------------------------------
### `Demo / Generator`

<a href="http://vincentgarreau.com/particles.js/" target="_blank"><img src="http://vincentgarreau.com/particles.js/assets/img/github-screen.jpg" alt="particles.js generator" /></a>

Configure, export, and share your particles.js configuration on CodePen: <br />
http://vincentgarreau.com/particles.js/

CodePen demo: <br />
http://codepen.io/VincentGarreau/pen/pnlso

-------------------------------
### `Usage`

Load particles.js and configure the particles:

**index.html**
```html
<div id="particles-js"></div>

<script src="particles.js"></script>
```

**app.js**
```javascript
/* particlesJS.load(@dom-id, @path-json, @callback (optional)); */
particlesJS.load('particles-js', 'assets/particles.json', function() {
  console.log('callback - particles.js config loaded');
});
```

**particles.json**
```javascript
particlesJS("particles-js", {

    "particles": {
        "number": {                   
            "value": 100,                 // 固定粒子数量
            "density": {
                "enable": true,           // 启用粒子密度
                "value_area": 800         // 固定粒子数量的区域大小
            }
        },
        "color": {
            "value": "#ffffff"            // 粒子颜色
        },
        "shape": {
            "type": "circle",             // 粒子形状
            "stroke": {
                "width": 0,               // 粒子边框宽度
                "color": "#FF13FE"        // 粒子边框颜色
            },
            "polygon": {
                "nb_sides": 5             // 多边形粒子的边数
            },
            "image": {
                "src": "image/par.svg",  // 自定义粒子(svg/png/gif/jpg)
                "width": 100,             // 自定义粒子图片宽度
                "height": 100             // 自定义粒子图片高度
            }
        },
        "opacity": {
            "value": 0.5,                 // 不透明度 0 ~ 1
            "random": false,              // 随机不透明度
            "anim": {
                "enable": false,          // 开启过渡、渐变
                "speed": 1,               // 渐变动画速度
                "opacity_min": 0.1,       // 渐变动画不透明度
                "sync": false
            }
        },
        "size": {
            "value": 3,                   // 粒子大小
            "random": true,               // 粒子大小随机
            "anim": {
                "enable": true,           // 开启粒子缩放动画
                "speed": 20,              // 动画速度
                "size_min": .5,           // 最小收缩粒子大小 0 ~ 1
                "sync": false
            }
        },
        "line_linked": {
            "enable": true,               // 开启连接线
            "distance": 150,              // 连接线有效距离
            "color": "#ffffff",           // 连接线颜色
            "opacity": 0.4,               // 连接线不透明度 0 ~ 1
            "width": 1                    // 连接线的宽度
        },
        "move": {
            "enable": true,               // 开启粒子移动
            "speed": 1,                   // 移动速度
            "direction": "none",          // 移动方向
            "random": false,              // 移动方向随机
            "straight": false,            // 直接移动
            "out_mode": "out",            // 边缘移出 out、反弹 bounce
            "bounce": false,              // 是否跳动移动
            "attract": {
                "enable": false,          // 粒子之间吸引
                "rotateX": 600,           // X 水平距离
                "rotateY": 1200           // Y 水平距离
            }
        }
    },

    "interactivity": {
        "detect_on": "canvas",            // 粒子之间互动检测
        "events": {
            "onhover": {
                "enable": true,           // 开启鼠标悬停
                "mode": "grab"            // 悬停模式
            },
            "onclick": {
                "enable": true,           // 开启鼠标单击
                "mode": "push"            // 单击模式
            },
            "resize": true                // 互动事件调整
        },
        "modes": {
            "grab": {
                "distance": 140,          // 粒子互动抓取距离
                "line_linked": {
                    "opacity": 1          // 粒子互动抓取距离连线不透明度
                }
            },
            "bubble": {
                "distance": 400,          // 粒子抓取泡沫效果之间的距离
                "size": 40,               // 粒子抓取泡沫效果之间的大小
                "duration": 2,            // 粒子抓取泡沫效果之间的持续时间
                "opacity": 8,             // 不透明度
                "speed": 3                // 速度
            },
            "repulse": {
                "distance": 200,          // 击退效果距离
                "duration": 0.4           // 击退效果持续时间
            },
            "push": {
                "particles_nb": 4         // 粒子推出的数量
            },
            "remove": {
                "particles_nb": 2         // 粒子移除的数量
            }
        }
    },
    "retina_detect": true                 // 视网膜检测，即无闪烁
});
```

-------------------------------

### `Options`

key | option type / notes | example
----|---------|------
`particles.number.value` | number | `40`
`particles.number.density.enable` | boolean | `true` / `false` 
`particles.number.density.value_area` | number | `800`
`particles.color.value` | HEX (string) <br /> RGB (object) <br /> HSL (object) <br /> array selection (HEX) <br /> random (string) | `"#b61924"` <br /> `{r:182, g:25, b:36}` <br />  `{h:356, s:76, l:41}` <br /> `["#b61924", "#333333", "999999"]` <br /> `"random"`
`particles.shape.type` | string <br /> array selection | `"circle"` <br /> `"edge"` <br /> `"triangle"` <br /> `"polygon"` <br /> `"star"` <br /> `"image"` <br /> `["circle", "triangle", "image"]`
`particles.shape.stroke.width` | number | `2`
`particles.shape.stroke.color` | HEX (string) | `"#222222"`
`particles.shape.polygon.nb_slides` | number | `5`
`particles.shape.image.src` | path link <br /> svg / png / gif / jpg | `"assets/img/yop.svg"` <br /> `"http://mywebsite.com/assets/img/yop.png"`
`particles.shape.image.width` | number <br />(for aspect ratio) | `100`
`particles.shape.image.height` | number <br />(for aspect ratio) | `100`
`particles.opacity.value` | number (0 to 1) | `0.75`
`particles.opacity.random` | boolean | `true` / `false` 
`particles.opacity.anim.enable` | boolean | `true` / `false` 
`particles.opacity.anim.speed` | number | `3`
`particles.opacity.anim.opacity_min` | number (0 to 1) | `0.25`
`particles.opacity.anim.sync` | boolean | `true` / `false`
`particles.size.value` | number | `20`
`particles.size.random` | boolean | `true` / `false` 
`particles.size.anim.enable` | boolean | `true` / `false` 
`particles.size.anim.speed` | number | `3`
`particles.size.anim.size_min` | number | `0.25`
`particles.size.anim.sync` | boolean | `true` / `false`
`particles.line_linked.enable` | boolean | `true` / `false`
`particles.line_linked.distance` | number | `150`
`particles.line_linked.color` | HEX (string) | `#ffffff`
`particles.line_linked.opacity` | number (0 to 1) | `0.5`
`particles.line_linked.width` | number | `1.5`
`particles.move.enable` | boolean | `true` / `false`
`particles.move.speed` | number | `4`
`particles.move.direction` | string | `"none"` <br /> `"top"` <br /> `"top-right"` <br /> `"right"` <br /> `"bottom-right"` <br /> `"bottom"` <br /> `"bottom-left"` <br /> `"left"` <br /> `"top-left"`
`particles.move.random` | boolean | `true` / `false`
`particles.move.straight` | boolean | `true` / `false`
`particles.move.out_mode` | string <br /> (out of canvas) | `"out"` <br /> `"bounce"`
`particles.move.bounce` | boolean <br /> (between particles) | `true` / `false`
`particles.move.attract.enable` | boolean | `true` / `false`
`particles.move.attract.rotateX` | number | `3000`
`particles.move.attract.rotateY` | number | `1500`
`interactivity.detect_on` | string | `"canvas", "window"`
`interactivity.events.onhover.enable` | boolean | `true` / `false`
`interactivity.events.onhover.mode` | string <br /> array selection | `"grab"` <br /> `"bubble"` <br /> `"repulse"` <br /> `["grab", "bubble"]`
`interactivity.events.onclick.enable` | boolean | `true` / `false`
`interactivity.events.onclick.mode` | string <br /> array selection | `"push"` <br /> `"remove"` <br /> `"bubble"` <br /> `"repulse"` <br /> `["push", "repulse"]`
`interactivity.events.resize` | boolean | `true` / `false`
`interactivity.events.modes.grab.distance` | number | `100`
`interactivity.events.modes.grab.line_linked.opacity` | number (0 to 1) | `0.75`
`interactivity.events.modes.bubble.distance` | number | `100`
`interactivity.events.modes.bubble.size` | number | `40`
`interactivity.events.modes.bubble.duration` | number <br /> (second) | `0.4`
`interactivity.events.modes.repulse.distance` | number | `200`
`interactivity.events.modes.repulse.duration` | number <br /> (second) | `1.2`
`interactivity.events.modes.push.particles_nb` | number | `4`
`interactivity.events.modes.push.particles_nb` | number | `4`
`retina_detect` | boolean | `true` / `false`

-------------------------------

### `Packages install`

##### ***npm***
https://www.npmjs.com/package/particles.js
```
npm install particles.js
```

##### ***Bower***
```
bower install particles.js --save
```

##### ***Rails Assets***
```
gem 'rails-assets-particles.js'
```

##### ***Meteor***
https://atmospherejs.com/newswim/particles
```
meteor add newswim:particles
```

-------------------------------

### `Hosting / CDN`

***Please use this host or your own to load particles.js on your projects***

http://www.jsdelivr.com/#!particles.js
