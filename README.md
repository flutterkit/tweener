# Tweener

Tweener is a simple and lightweight flutter animation tool. Anyone can easily learn to use it.

## Features

* Does one thing and one thing only: tween properties
* Very simple to use, but it can achieve a lot of effects
* Easing functions are reusable outside of Tween

## Installation

### Install the Tweener [https://pub.dev/packages/tweener](https://pub.dev/packages/tweener):

#### You should ensure that you add the following dependency in your Flutter project.
```
dependencies:
  tweener: ^2.2.2
```

#### install packages from the command line:
```
flutter packages get
```

## Useage

#### import class
```
import 'package:tweener/tweener.dart';
```

#### use Tweener
```
Tweener({"x": 0, "y": 0, "alpha": 0, "custom_prop_abc": 123})
    .to({"x": 100, "y": 500, "alpha": 1, "custom_prop_abc": 321}, 2000)
    .easing(Tweener.ease.elastic.easeOut)
    .onUpdate((obj) {
        setState(() {
            _x = obj["x"];
            _y = obj["y"];
            _alpha = obj["alpha"];
            _abc = obj["custom_prop_abc"];
        });
    })
    .onComplete((obj){
        /// 
    })
    .start();
```

```
var tween1 = new Tweener(sprite)
	.to({x: 700, y: 200, rotation: 359}, 2000)
	.delay(1000)
	.easing(Ease.back.easeOut)
	.onUpdate(update);

var tween2 = new Tweener(sprite)
	.to({x: 10, y: 20, rotation: 30}, 2000)
	.onUpdate(update);

tween1.chain(tween2);
tween1.start();
```
## About AnimateCon

To operate widget animations more conveniently, you can utilize the [AnimateCon](https://github.com/flutterkit/AnimateCon) library. This [library](https://github.com/flutterkit/AnimateCon) provides extremely facile implementation methods for animations such as position, scale, and alpha, enabling you to easily create various vivid and interesting animation effects.

## Thanks

Tweener refers to the implementation code of [tween.js](https://github.com/tweenjs/tween.js). They are really great. I want to pay tribute to the original author!
