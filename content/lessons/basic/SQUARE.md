---
title: "Moving Square"
lesson: 2
chapter: 7
date: "03/01/2018"
type: "lesson"
---
# Basic Square Animation

#### Live Code [https://rnplay.org/apps/BH9T8Q](https://rnplay.org/apps/BH9T8Q)

![Simple Timing Move](../images/SimpleTimingMove.gif)


```js
import React, { Component } from "react";

import {
  AppRegistry,
  StyleSheet,
  View,
  Animated
} from "react-native";

class SampleApp extends Component {
  componentWillMount() {
    this._animatedValue = new Animated.Value(0);
  }

  componentDidMount () {
    Animated.timing(this._animatedValue, {
        toValue: 300,
        duration: 500
    }).start();
  }

  render() {
    return (
      <View style={styles.container}>
       <Animated.View 
      		style={[styles.box, {transform: [{translateY: this._animatedValue}]}]}
      	/>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1
  },
  box: {
   	backgroundColor: 'red',
    position: 'absolute',
    top: 100,
    left: 100,
    width: 100,
    height: 100
  }
});

AppRegistry.registerComponent('SampleApp', () => SampleApp);

```