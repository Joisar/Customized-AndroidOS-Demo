Demo-App
========

NOTE: the purpose of creating this repo is purely for debugging the app.
I have posted the question on stackoverflow which you can find at http://stackoverflow.com/questions/16142877/ui-modification-of-individual-application-phone-contacts-in-ics-aosp

Here is the example scenario, In the application I was missing many classes and one of them is Timsort.java file so I needed to import it.I found that file in ICS AOSP and imported it by creating java.util package in my application src directory as shown in below screenshot.

![Alt text](http://thumbnails102.imagebam.com/25100/16445b250997206.jpg "")


and TimSort.java is not there in android.jar that is why I need to import it from AOSP.

Here is how I came to know that TimSort.java is not included in android.jar

![Alt text](http://thumbnails106.imagebam.com/25099/2b52d9250989643.jpg "")


Now when I import TimSort.java ,it tries to access some hidden method of Arrays.java class,So I need to import that class also from AOSP and so on to solve errors I need to import 3 more classes as shown in below image,

![Alt text](http://thumbnails105.imagebam.com/25100/0ba594250995720.jpg "")

![Alt text](http://thumbnails106.imagebam.com/25100/eea749250994970.jpg "")


And at the end when I run application,I face error of "Ill-advised or mistaken usage of a core class (java.* or javax.*)
when not building a core library" (It might get conflicts because of Arrays.java already exists in android.jar)

So I think I should go another way to use TimSort.java without facing such mess is to get library files as mentioned at https://code.google.com/p/android-source-browsing/source/browse/Android.mk?repo=platform--packages--apps--contacts&name=android-4.0.1_r1.2.



NOTE: My machine has Windows 7 and I am trying to modify/run the individual application of ICS AOSP.I am not having whole source tree of ICS AOSP in my eclipse.








