# ampprac2
STRINGS.XML
<resources>
    <string name="app_name">Simarjeet_prac2</string>

        <string name="Heading">Programming Resources</string>
        <string name="Description">
        Android is a mobile operating system developed by Google.It is based on a modified version of the Linux kernel, designed primarily for touch screen mobile devices
 such as smart phones and tablets.
        </string>
</resources>
MAINACTIVITY.JAVA
package com.example.simarjeet_prac2;

import android.graphics.drawable.ColorDrawable;
import android.os.Bundle;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);
        getSupportActionBar().setBackgroundDrawable(new ColorDrawable(getResources().getColor(R.color.purpleColor)));
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });
    }
}

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity">
        <LinearLayout
            android:layout_width="409dp"
            android:layout_height="729dp"
            android:orientation="vertical"
            app:layout_editor_absoluteX="1dp"
            app:layout_editor_absoluteY="1dp">
        <TextView
            android:id="@+id/textView"
            android:layout_width="match_parent"
            android:layout_height="56dp"
            android:text="@string/Heading"
            android:textSize="24SP"
            android:textColor="@color/yellow"
            android:background="@color/red">
        </TextView>
        <TextView
            android:id="@+id/textView2"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/Description"
            android:textSize="24dp"
            android:textColor="@color/white"
            android:background="@color/grey">
        </TextView>
        <TextView android:id="@+id/textView3"
            android:layout_width="match_parent"
            android:layout_height="59dp"
            android:text="TextView"
            android:textSize="22dp"
            android:textColor="@color/white"
            android:background="@color/blue">
        </TextView>
            <TextView android:id="@+id/textView4"
            android:layout_width="match_parent"
            android:layout_height="51dp"
            android:text="TextView"
            android:background="@color/cyan">
            </TextView>
            <ImageView
                android:id="@+id/imageView"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:scaleType="centerInside"
                app:srcCompat="@drawable/forandroid" />
        </LinearLayout>
    </LinearLayout>
ACTIVITY_MAIN.XML
</androidx.constraintlayout.widget.ConstraintLayout>
