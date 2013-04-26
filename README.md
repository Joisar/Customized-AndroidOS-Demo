Demo-App
========

NOTE: the purpose of creating this repo is purely for debugging the app.

Here is the scenario, In the application I was missing Timsort.java file so I needed to import it.I found that file in ICS AOSP and imported it by creating java.util package in my application src directory as shown in below screenshot.
![Alt text](http://thumbnails102.imagebam.com/25099/005a69250989046.jpg "Optional title")


and TimSort.java is not there in android.jar that is why I need to import it from AOSP.

Here is how I came to know that TimSort.java is not included in android.jar

![Alt text](http://thumbnails106.imagebam.com/25099/2b52d9250989643.jpg "Optional title")


Now when I import TimSort.java ,it tries to access some hidden method of Arrays.java class,So I need to import that class also from AOSP and so on to solve errors I need to import 3 more classes as shown in below image,
![Alt text](http://thumbnails106.imagebam.com/25100/eea749250994970.jpg "Optional title")









