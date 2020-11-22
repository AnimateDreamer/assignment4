### Tiffany Liu

Fall 2020-MMC5277: Web Design Principles

# CSS Positioning
This assignment will demonstrate the student's ability to build a website by using html and CSS.

## Code
Here are the code for this website in order to function properly:

```html
<section>
    <h1 style="color:darkred;">Feed Ranga meat! <img src="image/meat.png" alt="cartoon meat" title="meat" width="100px" /></h1>
    <p style="color:#0a681d;">Ranga is hungry and needs to eat some juicy meat. Flip the cards to help him find the meat</p>
    <div class="flip-card box1">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <img src="image/block.png" alt="block" width="100px" />
            </div>
            <div class="flip-card-back">
                <h2><span class="foods">Bruh!</span> Gross!</h2>
                <img src="image/dubious.png" alt="dubious food" width="100px" />
            </div>
        </div>
    </div>
    <div class="flip-card box2">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <img src="image/block.png" alt="block" width="100px" />
            </div>
            <div class="flip-card-back">
                <h2>Yummy! <span class="foods">Meat!</span></h2>
                <img src="image/meat.png" alt="cartoon meat" width="100px" />
            </div>
        </div>
    </div>
    <div class="flip-card box3">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <img src="image/block.png" alt="block" width="100px" />
            </div>
            <div class="flip-card-back">
                <h2>Too <span class="foods">Sweet!</span></h2>
                <img src="image/cake.png" alt="strawberry shortcake" width="100px" />
            </div>
        </div>
    </div>
```

The ``<div>`` has 6 classes,  `flip-card box1-3`will show the mystery boxes. `flip-card-inner` will include the front and back side of the mystery box. The `flip-card-front` class will show the block image. Each `flip-card-back` will display a different food image.

### Flip animation
In order to do the flip animation for the mystery boxes and the food items, here are the required CSS:

```css
.flip-card {
    position: absolute;
    z-index: 1;
    width: 7%;
    display: inline-block;
    background: transparent;
    margin: 30px;
    bottom: 30vw;
}

.flip-card-inner {
    position: relative;
    width: 100%;
    transition: transform .6s;
    transform-style: preserve-3d;
}

.flip-card:hover .flip-card-inner {
    transform: rotateY(180deg);
}

.flip-card-back {
    position: relative;
    transform: rotateY(180deg);
}

.flip-card-front,
.flip-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
}
```

### Background images
The required background images and CSS are as follows:
```html
<img class="cloud-top" src="image/cloud.png" alt="cloud" title="Cloud" />
<img class="cloud-bottom" src="image/cloud.png" alt="cloud" title="Cloud" />
<img class="grass" src="image/grass.png" alt="grass" title="Grass" />
```
```CSS
.cloud-top,
.cloud-bottom {
    position: absolute;
}
.sky,
.ground {
    position: relative;
}
.sky {
    height: 100%;
    background: skyblue;
}
.grass {
    width: 100%;
    position: fixed;
    bottom: 0px;
```    

### Animation
Here are the CSS for the animation:
```css
.wolf {
    position: absolute;
    width: 20%;
    animation: move 4s forwards infinite linear, jump 1s infinite ease-out
}
.cloud-top {
    width: 200px;
    top: 120px;
    opacity: .5;
    animation: wind 40s forwards infinite linear reverse;
}
.cloud-bottom {
    width: 300px;
    top: 0;
    animation: wind 30s forwards infinite linear reverse;
}
@keyframes move {
    from {
        transform: translateX(-100px)
    }
    to {
        transform: translatex(1000px)
    }
}

@keyframes wind {
    from {
        left: -300px;
    }
    to {
        left: 2000px;
    }
}

@keyframes jump {
    0% {
        bottom: 0px;
    }
    50% {
        bottom: 40%;
    }
    100% {
        bottom: 0px;
    }
}
```
I, Tiffany Liu, have read the point deduction list and understand that I will lose points for missing items.

![flower](https://purepng.com/public/uploads/large/purepng.com-christmas-poinsettia-flowerchristmasxmaspartyflowernaturechristmas-poinsettia-flower-911524569065ivoyp.png)

## Resources

* [Floats](https://ufl.zoom.us/recording/play/rtBgWT35brdzOKkpkv4sB4oGEQsi5OxPFSsk0ztIMHrK7Yh_RMKsAgKEOKlclNvh?autoplay=true&startTime=1540053996000)

* [CSS Animation](https://ufl.zoom.us/recording/play/pFAh_A8oQ2fLWqWoLa0SNUoqDk10-_X-vQMVbrUHvjw1BsLK16Wi4KQYberm4SnB?autoplay=true&startTime=1540684427000)

* [Flip Animation](https://ufl.zoom.us/rec/play/P0sl7A6Kywrv1YjUJYYhUblmkS-Qly641wQLw_B8ijR9Fe-z95H0cEkBCP94amArvGYTdVOVEmnEYq9h.M88Tj91fcJeup2RT?autoplay=true&startTime=1604249108000)

* [Creating a README.md File](https://ufl.zoom.us/rec/play/EpVovFimouarWqq028eiUU6ORvZ_OJVDGMEhTyMnG5pUCO8K0Nc9U4Jlj7XX-fcqSdif64xHHCT-hkz9.0AnHpJbG78Zf4pEF?autoplay=true&startTime=1605458374000)
