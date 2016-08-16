

# Lolly
A new way to observe android app log in real time.

![](http://7xprgn.com1.z0.glb.clouddn.com/Screenshot_20160815-135828.png)

![](http://7xprgn.com1.z0.glb.clouddn.com/2016-08-15%2013_53_35.gif)
# How to include  

Add the library to your module **build.gradle**:

```gradle
dependencies {
    compile 'com.zql.android:lolly:1.1'
}
```

# Usage

AndroidManifest.xml

```xml
        <service
            android:name="com.zqlite.android.lolly.Lolly"
            android:enabled="true"
            android:exported="false"
            android:process=":remote" />

        <activity android:name="com.zqlite.android.lolly.LollyViewer">
            <intent-filter>
                <category android:name="android.intent.category.DEFAULT" />

                <action android:name="android.intent.action.VIEW" />

                <data android:scheme="file" />
                <data android:scheme="content" />
                <data android:mimeType="text/plain" />
            </intent-filter>
        </activity>
```

permissions

```xml
    <uses-permission android:name="android.permission.SYSTEM_ALERT_WINDOW" />
    <uses-permission android:name="android.permission.READ_LOGS" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```

java api

```java
public static void showLolly(android.app.Activity activity,
                             java.lang.String[] tags)

public static void hideLolly(@NotNull android.app.Activity activity)

public static void saveLog(@NotNull android.app.Activity activity)
```
#License

     Copyright 2016 zhangqinglian

  	Licensed under the Apache License, Version 2.0 (the "License");
  	you may not use this file except in compliance with the License.
  	You may obtain a copy of the License at

	     http://www.apache.org/licenses/LICENSE-2.0

  	Unless required by applicable law or agreed to in writing, software
	  distributed under the License is distributed on an "AS IS" BASIS,
	  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	  See the License for the specific language governing permissions and
	  limitations under the License.


