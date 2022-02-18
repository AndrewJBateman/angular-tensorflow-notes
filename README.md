# :zap: Angular TensorFlow Notepad

* Code to experiment with machine learning using [Tensorflow.js](https://www.tensorflow.org/js), starting with recognising numbers. Tutorial code from Fireship (see ref in 'Inspiration') cloned then updated to Angular 13. All dependencies updated. Requires some fixes to work, due to updates. The plan is to use this to try new Tensorflow ideas.
* **Note:** to open web links in a new window use: _ctrl+click on link_

![GitHub repo size](https://img.shields.io/github/repo-size/AndrewJBateman/angular-tensorflow-notes?style=plastic)
![GitHub pull requests](https://img.shields.io/github/issues-pr/AndrewJBateman/angular-tensorflow-notes?style=plastic)
![GitHub Repo stars](https://img.shields.io/github/stars/AndrewJBateman/angular-tensorflow-notes?style=plastic)
![GitHub last commit](https://img.shields.io/github/last-commit/AndrewJBateman/angular-tensorflow-notes?style=plastic)

## :page_facing_up: Table of contents

* [:zap: Angular TensorFlow Notepad](#zap-angular-tensorflow-notepad)
  * [:page_facing_up: Table of contents](#page_facing_up-table-of-contents)
  * [:books: General info](#books-general-info)
  * [:camera: Screenshots](#camera-screenshots)
  * [:signal_strength: Technologies](#signal_strength-technologies)
  * [:floppy_disk: Setup](#floppy_disk-setup)
  * [:computer: Code Examples](#computer-code-examples)
  * [:cool: Features](#cool-features)
  * [:clipboard: Status & To-Do List](#clipboard-status--to-do-list)
  * [:clap: Inspiration](#clap-inspiration)
  * [:file_folder: License](#file_folder-license)
  * [:envelope: Contact](#envelope-contact)

## :books: General info

* "_TensorFlow.js is an open-source hardware-accelerated JavaScript library for training and deploying machine learning models._"

## :camera: Screenshots

![Example screenshot](./img/.png)

## :signal_strength: Technologies

* [Angular v13](https://angular.io/)
* [@tensorflow/tfjs v3](https://www.npmjs.com/package/@tensorflow/tfjs), javascript version of [Tensorflow](https://js.tensorflow.org)
* [ng2-charts v3](https://www.npmjs.com/package/ng2-charts)

## :floppy_disk: Setup

* `npm i` to install dependenciesy

* `ng serve` then navigate to port 4200.

## :computer: Code Examples

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

## :cool: Features

* to follow

## :clipboard: Status & To-Do List

* Status: not compiling due to errors from tensorflow update to v3
* To-Do: Correct: Namespace has no exported member, loadModel does not exist.., fromPixels does not exist.

## :clap: Inspiration

* [Fireship, TensorFlow.js Quick Start](https://www.youtube.com/watch?v=Y_XM3Bu-4yc)
* [github repo for the above](https://github.com/AngularFirebase/97-tensorflowjs-quick-start)

## :file_folder: License

* This project is licensed under the terms of the MIT license.

## :envelope: Contact

* Repo created by [ABateman](https://github.com/AndrewJBateman), email: gomezbateman@yahoo.com
