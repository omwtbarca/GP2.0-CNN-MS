# CNN

[toc]

![](2022-10-04-00-09-39.png)
![](2022-10-04-00-10-22.png)


我们知道卷积层可以提取不同的特征。对CNN的训练，重点就是训练出来各种各样的卷积核来提取特征。初学者在学习CNN时，往往会面临一个问题，知道CNN的输出是如何计算的，也知道如何利用基于链式求导法则的反向传播算法去训练网络，却不知道为什么CNN能够提取图片特征，卷积核里面的那几个数字背后的意义和原理。

# MNIST

```Python
import tensorflow as tf
mnist=tf.keras.datasets.mnist
(x_train, y_train), (x_test, y_test) = mnist.load_data()
x_train=tf.keras.utils.normalize(x_train,axis=1)
x_test=tf.keras.utils.normalize(x_test,axis=1)

model=tf.keras.models.Sequential()
model.add(tf.keras.layers.Flatten())
model.add(tf.keras.layers.Dense(128,activation=tf.nn.relu))  #must activation =tf.nn.relu  不能直接act=“relu"
model.add(tf.keras.layers.Dense(128,activation=tf.nn.relu)) 
model.add(tf.keras.layers.Dense(10,activation=tf.nn.softmax)) 

model.compile(optimizer= 'adam', loss="binary_crossentropy", metrics=['accuracy'])
  # always try to minimize the loss, not maxmize the accuracy
 # or loss='sparse_catagorical_crossentropy' 交叉熵损失
model.fit(x_train,y_train,epochs=3)
val_loss, val_acc = model.evaluate(x_test, y_test)  # evaluate the out of sample data with model
print(val_loss)  # model's loss (error)
print(val_acc)  # model's accuracy

model.save('epic_num_reader.model')
new_model = tf.keras.models.load_model('epic_num_reader.model')
predictions = new_model.predict(x_test)
import numpy as np

print(np.argmax(predictions[0]))
plt.imshow(x_test[0],cmap=plt.cm.binary)
plt.show()
```
```python
# self-made hand-written numbers
number1 = cv2.imread(r"E:\AI\MNIST\datasets\test\up5.jpg")
img_RGB = cv2.cvtColor(number4, cv2.COLOR_BGR2GRAY)
img_RGB=cv2.resize(img_RGB,[28,28])
plt.imshow(img_RGB,cmap='binary')
# x_test = images
x_test = tf.keras.utils.normalize(x_test, axis=1)  # scales data between 0 and 1

# predictions
```

book Python skleran
