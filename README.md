# Shimmer Effect in Android

### Applications of Shimmer Effect

- Shimmer Effect is mostly used for loading the screen in an attractive form.
- Shimmer Effect gives a good appearance to Images in the Android app.
- Using Shimmer Effect in our app gives an Animated view of the image.


## Step by Step Implementation


### Step 1: Add dependency of Shimmer Effect library in build.gradle file

```
implementation 'com.facebook.shimmer:shimmer:0.5.0'
```

##### now click on *Sync now* it will sync your all files in build.gradle().

### Step 2: Create a new Shimmer Effect in your activity_main.xml file

```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    >

    <!-- Shimmer Effect -->
    <com.facebook.shimmer.ShimmerFrameLayout
        android:id="@+id/shimmer_view_container"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true"
        >

        <LinearLayout
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:gravity="center"
            android:orientation="vertical">

            <!--Image-->
            <ImageView
                android:layout_width="150dp"
                android:layout_height="150dp"
                android:src="@drawable/dashboard" />

            <!--Text given to Image-->
            <TextView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_marginTop="15dp"
                android:text="Dashboard"
                android:textColor="@color/teal_200"
                android:textSize="24dp"
                android:textStyle="bold" />

        </LinearLayout>

    </com.facebook.shimmer.ShimmerFrameLayout>

</RelativeLayout>
```


### Step 3: Working with the MainActivity.java file

```
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import com.facebook.shimmer.ShimmerFrameLayout;

public class MainActivity extends AppCompatActivity {

    
    // Variables created for buttons and Shimmer
    ShimmerFrameLayout textEffect;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Shimmer effect Find
        textEffect = findViewById(R.id.shimmer_view_container);
        
        
        // Start Shimmer Effect
        textEffect.startShimmer();


    }
}
```


##### Now click on the run option it will take some time to build Gradle. After that, you will get output on your device as given below.


_© All Right Reserved by Innovative Programmer ❤️_
