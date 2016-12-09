# WELCOME YOU TUTORIAL LEARNING ANDROID [![Build Status](https://travis-ci.org/nomensa/jquery.hide-show.svg)](https://travis-ci.org/nomensa/jquery.hide-show.svg?branch=master)

- [Understand definition class or interface in android studio](#understand-definition-class-or-interface-in-android-studio)
  - [Context](#context)
    - [What is the purpose of class context](#what-is-the-purpose-of-class-context)
  - [Intent](#intent)
    - [Starting intent from onclicklistener](#starting-intent-from-onclicklistener)
  - [AndroidManifest](#androidmanifest) 
    - [How to declare activity in manifest](#how-to-declare-activity-in-manifest)

##What is the purpose of class context

<p align="center">
It allows access to application-specific resources and classes, as well as up-calls for application-level operations such as launching activities, broadcasting and receiving intents
</p>

##Starting intent from onclicklistener

    protected void addListenerOnButton(){
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MainActivity.this,Level0Activity.class);
                startActivity(intent);
            }
        });
    }

    protected void addListenerOnButton(){
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(view.getContext(),Level0Activity.class);
                startActivity(intent);
            }
        });
    }

    protected void addListenerOnButton(){
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(context.getApplicationContext(),Level0Activity.class);
                startActivity(intent);
            }
        });
    }

##How to declare activity in manifest

    <activity android:name=".aboutmanifest.Level2Activity"
            android:label="App Football Match">
        </activity>

    Configure: 
 
	@string/app_demo = "App Football Match"

    Details:

    <?xml version="1.0" encoding="utf-8"?>
	<manifest xmlns:android="http://schemas.android.com/apk/res/android"
	    package="com.example.enclaveit.tutorials">

	    <application
		android:allowBackup="true"
		android:icon="@mipmap/ic_launcher"
		android:label="@string/app_name"
		android:supportsRtl="true"
		android:theme="@style/AppTheme">
		<activity android:name=".MainActivity">
		    <intent-filter>
		        <action android:name="android.intent.action.MAIN" />

		        <category android:name="android.intent.category.LAUNCHER" />
		    </intent-filter>
		</activity>

		<activity android:name=".aboutactivity.Level0Activity" />
		<activity android:name=".aboutactivity.Level1Activity" />
		<activity
		    android:name=".aboutmanifest.Level2Activity"
		    android:label="@string/app_demo">
		</activity>

	    </application>

	</manifest>



























