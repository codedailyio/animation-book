---
title: "Animated.createAnimatedComponent"
lesson: 22
chapter: 4
date: "03/01/2018"
type: "lesson"
---

# createAnimatedComponent

`Animated` ships with 3 default views. `Animated.View`, `Animated.Text`, and `Animated.Image`. However in some cases you may want to turn a component into an `Animated` component so it can take advantage of `Animated.Value` in it's styles or properties.

Example ScrollView

```js
const AnimatedScrollView = Animated.createAnimatedComponent(ScrollView)
```

It will work on any View, even `react-native-svg` views.

```js

import { Path } from "react-native-svg";


const AnimatedPath = Animated.createAnimatedComponent(Path);
```
