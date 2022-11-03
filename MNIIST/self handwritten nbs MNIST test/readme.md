I get my hand-written numbers tested in this work.
Some details are as followed.
* Firstly, I wrote some numbers on the A4 sheet ,then took the phone and pictured these numbers individually.
* Secondly, I imported images by using 'number1 = cv2.imread(r"E:\AI\MNIST\datasets\test\up5.jpg")'
* Thirdly, I resized images into 28X28, which is the same size with MNIST datasets.
> PS: There're some differences between 'reshape' and 'resize',in terms of images.[Opencv学习之：reshape和 resize 的区别](https://blog.csdn.net/qq_42902997/article/details/108339036?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-3-108339036-blog-52945822.pc_relevant_aa2&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-3-108339036-blog-52945822.pc_relevant_aa2&utm_relevant_index=6)
* Fourthly, cvtColor to gray by 'img1 = cv2.cvtColor(number1, cv2.COLOR_BGR2GRAY)'


![image](https://user-images.githubusercontent.com/87826552/199665316-67587c42-ac22-4d2e-9876-1897fc06bb76.png)


* Last but not least, let images normalized by 'x_test = tf.keras.utils.normalize(x_test, axis=1) ' # scales data between 0 and 1
* DO YOUR PREDICTIONS! 'predictions = model.predict(x_test)'
