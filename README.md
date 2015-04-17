# afiledialog
Overview
aFileDialog is an Android library which implements a simple and easy to use file chooser.

His main features are:

The file chooser can be opened both as a Dialog or as an Activity.
You can filter the files using regular expressions.
Can select files or folders.
Can create files and folders.
aFileDialog is open source, licensed under LGPL 3, and is compatible with Android 2.2+.

Download it here or visit the Downloads section.

You can also install the showcase app, available at Google Play.

			
How to use it
In order to use aFileDialog in your application you must do three steps:

1) Add a reference to the library project. Note that, since aFileDialog is a Android Library project, it can not be compiled into a binary file (such as a JAR file), so your project must reference to the aFileDialog project, instead of reference to a single JAR file.

2) Declare the activity FileChooserActivity in the manifest file. This can be done by adding the following lines inside the tags </application>\</application>:

     <activity android:name="ar.com.daidalos.afiledialog.FileChooserActivity" />
3) Add the permission READ_EXTERNAL_STORAGE to the manifest file, if you want to access the SD card (and if you are using Android 4.1 or superior).

     <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
Then you must only create an instance of FileChooserDialog and call the show() method or start the activity FileChooserActivity.

Documentation
aFileDialog has been designed in order to be easy to use and easy to develop.

In order to known how to use aFileDialog, check the user guide (also available in Spanish and French).

If you want to modify or extend aFileDialog, you can read the software design description (also available in Spanish), although this is not mandatory, since the code is fully commented and you are going to figure out how it works in matters of minutes.

Examples
Samples codes are available in the user guide, but, to summarize, you can open a file chooser (implemented with a Dialog) using the following lines:

 FileChooserDialog dialog = new FileChooserDialog(context);
 dialog.show();
To open a file chooser implemented with an Activity, you can use the following lines:

 Intent intent = new Intent(this, FileChooserActivity.class);
 this.startActivityForResult(intent, 0);
