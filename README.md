# Angular TensorFlow Notepad

Code to experiment with machine learning using [Tensorflow.js](https://www.tensorflow.org/js), starting with recognising numbers. Tutorial code from Fireship (see ref in 'Inspiration') cloned then updated to Angular 8. All dependencies updated with no vulnerabilities. Requires some fixes to work, due to angular updates. The plan is to use this to try new Tensorflow ideas.

*** Note: to open web links in a new window use: _ctrl+click on link_**

## Table of contents

* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## General info

"_TensorFlow.js is an open-source hardware-accelerated JavaScript library for training and deploying machine learning models._"

## Screenshots

![Example screenshot](./img/.png)

## Technologies

* [Angular v8.0.2](https://angular.io/)

* [Tensorflow](https://js.tensorflow.org)

* [@tensorflow/tfjs v1.2.2](https://www.npmjs.com/package/@tensorflow/tfjs).

* [ng2-charts](https://www.npmjs.com/package/ng2-charts)

## Setup

* when fixed: type `ng serve` then navigate to port 4200.

## Code Examples

* tba

```typescript
 async trainNewModel() {
      // Define a model for linear regression.
    this.linearModel = tf.sequential();
    this.linearModel.add(tf.layers.dense({units: 1, inputShape: [1]}));

    // Prepare the model for training: Specify the loss and the optimizer.
    this.linearModel.compile({loss: 'meanSquaredError', optimizer: 'sgd'});


    // Training data, completely random stuff
    const xs = tf.tensor1d([3.2, 4.4, 5.5, 6.71, 6.98, 7.168, 9.779, 6.182, 7.59, 2.16, 7.042, 10.71, 5.313, 7.97, 5.654, 9.7, 3.11]);
    const ys = tf.tensor1d([1.6, 2.7, 2.9, 3.19, 1.684, 2.53, 3.366, 2.596, 2.53, 1.22, 2.87, 3.45, 1.65, 2.904, 2.42, 2.4, 1.31]);


    // Train
    await this.linearModel.fit(xs, ys)

    console.log('model trained')
  }
```

## Features

* to follow

## Status & To-Do List

* Status: not compiling.

* To-Do: Correct: Namespace has no exported member, loadModel does not exist.., fromPixels does not exist.

## Inspiration

* [Fireship, TensorFlow.js Quick Start](https://www.youtube.com/watch?v=Y_XM3Bu-4yc)

* [github repo for the above](https://github.com/AngularFirebase/97-tensorflowjs-quick-start)

## Contact

Repo created by [ABateman](https://www.andrewbateman.org) - feel free to contact me!
