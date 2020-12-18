# dl-comp-vis-final-project

## How to Reproduce the Result Using the Notebooks

Each notebook corresponds to one experiment mentioned in the report.
For example, `Landmark_Classification_ResNet_FineTune.ipynb` is associated
with training a `ResNet18` using `FineTune` method, i.e. unfreezing all layers.

Before running the notebook, prepare the dataset using the following way:

1. Find the cell that contains below command:

`!cp -r "drive/MyDrive/DL for Comp Vis/Final Project/data/landmark" data`

2. If you run the notebook in `Google Colab`, then you can mount your
`Google Drive` and change the path (after the `-r` option) into
your desired data path in drive.

3. If you run it locally, change the path (after the `-r` option) into
your desired local data path. Obviously, you can also place directly
the dataset under the `data` directory and skip/comment the `cp` command.

4. Make sure that `data` directory has the same parent directory to
that of the notebook and is structured like below.

```
data
  landmark
    train
      alma
      lion
      uris
    val
      alma
      lion
      uris
    test
      alma
      lion
      uris
```

## Trying Interactive Demo using Tensorflow.js

You can try an interactive demo of this image classification app by
visiting the below link.

`https://dl-for-comp-vis-final-proj.herokuapp.com`

Alternatively, if the above link doesn't work, you could run it locally by
doing the following steps:

1. Get into the `tfjs_model` directory.

`cd tfjs_model`

2. Run the static web app using Python HTTP Server. Below example is using
port `8282`.

`python3 -m http.server 8282`

3. Visit the app by entering the URL: `localhost:8282` in your browser,
preferably Google Chrome, because that's where I tested the app.
