# cordova-plugin-http-legacy
`cordova plugin add cordova-plugin-http-legacy --save`

If you are targeting Android 9 and up and using AdMob you will start seeing crashes like:
```
**java.lang.NoClassDefFoundError**:
at gn.b (com.google.android.gms.dynamite_adsdynamite@17455079@17.4.55 (100306-248795830):3)
at gk.a (com.google.android.gms.dynamite_adsdynamite@17455079@17.4.55 (100306-248795830):3)
at gm.a (com.google.android.gms.dynamite_adsdynamite@17455079@17.4.55 (100306-248795830):18)
at com.google.android.gms.ads.internal.util.ap.a (com.google.android.gms.dynamite_adsdynamite@17455079@17.4.55 (100306-248795830):5)
at fr.a (com.google.android.gms.dynamite_adsdynamite@17455079@17.4.55 (100306-248795830):19)
at fr.run (com.google.android.gms.dynamite_adsdynamite@17455079@17.4.55 (100306-248795830):8)
Caused by: **java.lang.ClassNotFoundException**:
at dalvik.system.BaseDexClassLoader.findClass (BaseDexClassLoader.java:134)
at java.lang.ClassLoader.loadClass (ClassLoader.java:379)
at ab.loadClass (com.google.android.gms.dynamite_dynamiteloader@17455079@17.4.55 (100306-248795830):4)
at java.lang.ClassLoader.loadClass (ClassLoader.java:312)
```

Even after updating the AdMob SDK to `17.2.1` doesn't seem to solve the problem. This plugin should solve it.
[more info here](https://developer.android.com/about/versions/pie/android-9.0-changes-28)
