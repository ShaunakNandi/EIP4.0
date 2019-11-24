# Achieving 0.9940 accuracy on the MNIST dataset within 20 epochs:

  1. Iteration 1: Vanilla - 1x1(to reduce #params) and MP alone
  
  2. Iteration 2: Intro BN and reduce #param count
  
  3. Iteration 3: A touch of Dropout to furthur reduce overfit (99.40% reached)
  
  4. Iteration 4: Adam vs SGD case study and Introducing GAP
  
# Logs

>>Train on 60000 samples, validate on 10000 samples
Epoch 1/20
60000/60000 [==============================] - 29s 477us/step - loss: 0.1722 - acc: 0.9505 - val_loss: 0.0475 - val_acc: 0.9860

Epoch 2/20
60000/60000 [==============================] - 27s 444us/step - loss: 0.0650 - acc: 0.9800 - val_loss: 0.0327 - val_acc: 0.9899

Epoch 3/20
60000/60000 [==============================] - 28s 461us/step - loss: 0.0523 - acc: 0.9838 - val_loss: 0.0314 - val_acc: 0.9899

Epoch 4/20
60000/60000 [==============================] - 28s 462us/step - loss: 0.0467 - acc: 0.9853 - val_loss: 0.0249 - val_acc: 0.9925

Epoch 5/20
60000/60000 [==============================] - 27s 456us/step - loss: 0.0422 - acc: 0.9865 - val_loss: 0.0248 - val_acc: 0.9914

Epoch 6/20
60000/60000 [==============================] - 27s 455us/step - loss: 0.0387 - acc: 0.9880 - val_loss: 0.0232 - val_acc: 0.9917

Epoch 7/20
60000/60000 [==============================] - 27s 456us/step - loss: 0.0361 - acc: 0.9884 - val_loss: 0.0230 - val_acc: 0.9915

Epoch 8/20
60000/60000 [==============================] - 27s 456us/step - loss: 0.0366 - acc: 0.9886 - val_loss: 0.0215 - val_acc: 0.9926

Epoch 9/20
60000/60000 [==============================] - 27s 454us/step - loss: 0.0331 - acc: 0.9896 - val_loss: 0.0225 - val_acc: 0.9919

Epoch 10/20
60000/60000 [==============================] - 27s 456us/step - loss: 0.0328 - acc: 0.9898 - val_loss: 0.0209 - val_acc: 0.9929

Epoch 11/20
60000/60000 [==============================] - 27s 456us/step - loss: 0.0305 - acc: 0.9901 - val_loss: 0.0208 - val_acc: 0.9930

Epoch 12/20
60000/60000 [==============================] - 27s 453us/step - loss: 0.0298 - acc: 0.9906 - val_loss: 0.0227 - val_acc: 0.9934

Epoch 13/20
60000/60000 [==============================] - 27s 455us/step - loss: 0.0283 - acc: 0.9913 - val_loss: 0.0183 - val_acc: 0.9942

Epoch 14/20
60000/60000 [==============================] - 27s 456us/step - loss: 0.0282 - acc: 0.9912 - val_loss: 0.0192 - val_acc: 0.9932

Epoch 15/20
60000/60000 [==============================] - 28s 465us/step - loss: 0.0277 - acc: 0.9917 - val_loss: 0.0198 - val_acc: 0.9936

Epoch 16/20
60000/60000 [==============================] - 27s 454us/step - loss: 0.0278 - acc: 0.9914 - val_loss: 0.0181 - val_acc: 0.9944

Epoch 17/20
60000/60000 [==============================] - 27s 454us/step - loss: 0.0264 - acc: 0.9919 - val_loss: 0.0229 - val_acc: 0.9933

Epoch 18/20
60000/60000 [==============================] - 27s 455us/step - loss: 0.0251 - acc: 0.9920 - val_loss: 0.0200 - val_acc: 0.9936

Epoch 19/20
60000/60000 [==============================] - 27s 454us/step - loss: 0.0240 - acc: 0.9923 - val_loss: 0.0240 - val_acc: 0.9923

Epoch 20/20
60000/60000 [==============================] - 27s 455us/step - loss: 0.0252 - acc: 0.9918 - val_loss: 0.0192 - val_acc: 0.9935


# Test dataset Accuracy

>> [0.019193828565673903, 0.9935]

- - - -

Please click [this link](https://colab.research.google.com/drive/1i4SrgIA-ge-T3n80D9t6u-MP4gbENgMo) if the colab page does not render
