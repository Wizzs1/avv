# Rosé
	
```activity fragment```

		<?xml version="1.0" encoding="utf-8"?>
		<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
		    xmlns:app="http://schemas.android.com/apk/res-auto"
		    xmlns:tools="http://schemas.android.com/tools"
		    android:layout_width="match_parent"
		    android:layout_height="match_parent"
		    android:background="@drawable/background"
		    android:orientation="vertical"
		    tools:context=".activity.FragmentActivity">
		
		    <com.google.android.material.tabs.TabLayout
		        android:id="@+id/tablayout"
		        android:layout_width="match_parent"
		        android:layout_height="wrap_content"
		        android:background="@color/Pastel_Pink"
		        app:tabTextColor="@color/white"
		        app:tabIndicatorColor="@color/white"
		        app:tabSelectedTextColor="@color/white" >
		        
		        <com.google.android.material.tabs.TabItem
		            android:id="@+id/tab1"
		            android:layout_width="wrap_content"
		            android:layout_height="wrap_content"
		            android:text="EYELINER" />
		
		        <com.google.android.material.tabs.TabItem
		            android:id="@+id/tab2"
		            android:layout_width="wrap_content"
		            android:layout_height="wrap_content"
		            android:text="LIPCREAM" />
		
		        <com.google.android.material.tabs.TabItem
		            android:id="@+id/tab3"
		            android:layout_width="wrap_content"
		            android:layout_height="wrap_content"
		            android:text="EYEBROW" />
		        
		    </com.google.android.material.tabs.TabLayout>
		
		    <FrameLayout
		        android:id="@+id/framelayout"
		        android:layout_width="match_parent"
		        android:layout_height="match_parent" />
		</LinearLayout>


```activity homepage```

	<GridLayout
	    xmlns:android="http://schemas.android.com/apk/res/android"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    android:columnCount="3"
	    android:background="@color/white"
	    android:rowCount="2"
	    android:alignmentMode="alignBounds"
	    android:useDefaultMargins="true" >
	
	
	    <ImageView
	        android:id="@+id/btnHello"
	        android:layout_width="120dp"
	        android:layout_height="120dp"
	        android:layout_marginStart="10dp"
	        android:layout_marginEnd="15dp"
	        android:src="@drawable/hello" />
	
	    <ImageView
	        android:id="@+id/btnCount"
	        android:layout_width="120dp"
	        android:layout_height="120dp"
	        android:layout_marginEnd="15dp"
	        android:src="@drawable/count" />
	
	    <ImageView
	        android:id="@+id/btnScrollice"
	        android:layout_width="120dp"
	        android:layout_height="120dp"
	        android:layout_marginEnd="10dp"
	        android:src="@drawable/scrollice" />
	
	    <ImageView
	        android:id="@+id/btnTwoActivity"
	        android:layout_width="120dp"
	        android:layout_height="120dp"
	        android:layout_marginEnd="10dp"
	        android:src="@drawable/twoactivity" />
	
	    <ImageView
	        android:id="@+id/btnAlarm"
	        android:layout_width="120dp"
	        android:layout_height="120dp"
	        android:layout_marginEnd="10dp"
	        android:src="@drawable/alarm" />
	
	    <ImageView
	        android:id="@+id/btnMaps"
	        android:layout_width="120dp"
	        android:layout_height="120dp"
	        android:layout_marginEnd="10dp"
	        android:src="@drawable/maps" />
	
	    <ImageView
	        android:id="@+id/btnMovies"
	        android:layout_width="120dp"
	        android:layout_height="120dp"
	        android:layout_marginEnd="10dp"
	        android:src="@drawable/fragment" />
	</GridLayout>

```activity main```

	<?xml version="1.0" encoding="utf-8"?>
	<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    xmlns:tools="http://schemas.android.com/tools"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    android:background="@color/white"
	    tools:context=".activity.MainActivity">
	
	    <TextView
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:text="@string/text"
	        android:textColor="@color/black"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintEnd_toEndOf="parent"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toTopOf="parent" />
	
	</androidx.constraintlayout.widget.ConstraintLayout>

 ```activity scrollice```

	 <?xml version="1.0" encoding="utf-8"?>
	<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:tools="http://schemas.android.com/tools"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    tools:context="com.helloworld.activity.ScrollingActivity">
	
	    <TextView
	        android:id="@+id/article_heading"
	        android:layout_width="match_parent"
	        android:layout_height="wrap_content"
	        android:background="@color/Pastel_Pink"
	        android:padding="@dimen/padding_regular"
	        android:text="@string/article_title"
	        android:textAppearance="@android:style/TextAppearance.DeviceDefault.Large"
	        android:textColor="@android:color/white"
	        android:textStyle="bold"
	        />
	
	    <ScrollView
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_below="@id/article_heading"
	        android:background="@color/white">
	
	        <LinearLayout
	            android:layout_width="match_parent"
	            android:layout_height="wrap_content"
	            android:orientation="vertical">
	
	            <TextView
	                android:id="@+id/article_subheading"
	                android:layout_width="match_parent"
	                android:layout_height="wrap_content"
	                android:padding="@dimen/padding_regular"
	                android:text="@string/article_subtitle"
	                android:textAppearance="@android:style/TextAppearance.DeviceDefault"
	                android:textColor="@color/black"/>
	
	            <TextView
	                android:id="@+id/article"
	                android:layout_width="wrap_content"
	                android:layout_height="wrap_content"
	                android:autoLink="web"
	                android:lineSpacingExtra="@dimen/line_spacing"
	                android:padding="@dimen/padding_regular"
	                android:text="@string/article_text"
	                android:textColor="@color/black"/>
	        </LinearLayout>
	    </ScrollView>
	
	</RelativeLayout>

 ```activity splashscreen```

	 <?xml version="1.0" encoding="utf-8"?>
	<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:tools="http://schemas.android.com/tools"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    android:background="@color/black"
	    tools:context=".SplashScreen">
	
	    <LinearLayout
	        android:layout_width="match_parent"
	        android:layout_height="wrap_content"
	        android:layout_centerInParent="true"
	        android:gravity="center"
	        android:orientation="vertical">
	
	        <ImageView
	            android:id="@+id/logo"
	            android:layout_width="300dp"
	            android:layout_height="wrap_content"
	            android:adjustViewBounds="true"
	            android:src="@drawable/downloaded" />
	    </LinearLayout>
	
	</RelativeLayout>

 ```activity toast```

	 <?xml version="1.0" encoding="utf-8"?>
	<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    xmlns:tools="http://schemas.android.com/tools"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    tools:context="com.helloworld.activity.CountActivity">
	
	    <Button
	        android:id="@+id/button_toast"
	        android:layout_width="183dp"
	        android:layout_height="44dp"
	        android:layout_marginStart="8dp"
	        android:layout_marginTop="4dp"
	        android:layout_marginEnd="8dp"
	        android:background="@color/blue"
	        android:onClick="showToast"
	        android:text="@string/button_label_toast"
	        android:textColor="@android:color/white"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toTopOf="parent" />
	
	    <Button
	        android:id="@+id/button_count"
	        android:layout_width="190dp"
	        android:layout_height="50dp"
	        android:layout_marginStart="12dp"
	        android:layout_marginBottom="12dp"
	        android:background="@color/blue"
	        android:onClick="countUp"
	        android:text="@string/button_label_count"
	        android:textColor="@android:color/white"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintStart_toStartOf="parent" />
	
	    <Button
	        android:id="@+id/button_back"
	        android:layout_width="190dp"
	        android:layout_height="50dp"
	        android:layout_marginEnd="16dp"
	        android:layout_marginBottom="12dp"
	        android:background="@color/blue"
	        android:onClick="countDown"
	        android:text="@string/button_label_back"
	        android:textColor="@android:color/white"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintEnd_toEndOf="parent" />
	
	    <TextView
	        android:id="@+id/show_count"
	        android:layout_width="0dp"
	        android:layout_height="0dp"
	        android:layout_marginBottom="8dp"
	        android:layout_marginEnd="8dp"
	        android:layout_marginStart="8dp"
	        android:layout_marginTop="8dp"
	        android:background="@color/yellow"
	        android:textAlignment="center"
	        android:gravity="center_vertical"
	        android:text="@string/count_initial_value"
	        android:textColor="@color/blue"
	        android:textSize="160sp"
	        android:textStyle="bold"
	        app:layout_constraintBottom_toTopOf="@+id/button_count"
	        app:layout_constraintEnd_toEndOf="parent"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toBottomOf="@id/button_toast"
	        />
	
	    <EditText
	        android:id="@+id/editText_fib"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginStart="192dp"
	        android:layout_marginTop="4dp"
	        android:ems="10"
	        android:inputType="text"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toTopOf="parent" />
	
	
	</androidx.constraintlayout.widget.ConstraintLayout>

 ```activity one```

	 <?xml version="1.0" encoding="utf-8"?>
	<androidx.constraintlayout.widget.ConstraintLayout
	    xmlns:android="http://schemas.android.com/apk/res/android"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    xmlns:tools="http://schemas.android.com/tools"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    tools:context=".activity.CountActivity">
	
	    <TextView
	        android:id="@+id/text_header_reply"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginStart="8dp"
	        android:layout_marginLeft="8dp"
	        android:layout_marginTop="16dp"
	        android:text="@string/textHeader_reply"
	        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
	        android:textStyle="bold"
	        android:visibility="invisible"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toTopOf="parent" />
	
	    <TextView
	        android:id="@+id/text_message_reply"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginStart="8dp"
	        android:layout_marginLeft="8dp"
	        android:layout_marginTop="8dp"
	        android:visibility="invisible"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toBottomOf="@id/text_header_reply" />
	
	    <Button
	        android:id="@+id/button_main"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginBottom="16dp"
	        android:layout_marginRight="16dp"
	        android:backgroundTint="@color/Pastel_Pink"
	        android:text="@string/button_main"
	        android:onClick="launchSecondActivity"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintRight_toRightOf="parent"/>
	
	    <EditText
	        android:id="@+id/editText_main"
	        android:layout_width="0dp"
	        android:layout_height="wrap_content"
	        android:layout_marginBottom="16dp"
	        android:layout_marginEnd="8dp"
	        android:layout_marginStart="8dp"
	        android:ems="10"
	        android:hint="@string/editText_main"
	        android:inputType="textLongMessage"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintEnd_toStartOf="@+id/button_main"
	        app:layout_constraintStart_toStartOf="parent"/>
	
	</androidx.constraintlayout.widget.ConstraintLayout>

 ```activity two```

	 <?xml version="1.0" encoding="utf-8"?>
	<androidx.constraintlayout.widget.ConstraintLayout
	    xmlns:android="http://schemas.android.com/apk/res/android"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    xmlns:tools="http://schemas.android.com/tools"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    tools:context=".activity.CountActivity">
	
	    <TextView
	        android:id="@+id/text_header"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginStart="8dp"
	        android:layout_marginLeft="8dp"
	        android:layout_marginTop="16dp"
	        android:text="@string/text_header"
	        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
	        android:textStyle="bold"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toTopOf="parent" />
	
	    <TextView
	        android:id="@+id/text_message"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginStart="8dp"
	        android:layout_marginLeft="8dp"
	        android:layout_marginTop="8dp"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toBottomOf="@+id/text_header" />
	
	    <Button
	        android:id="@+id/button_second"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginBottom="16dp"
	        android:layout_marginRight="16dp"
	        android:backgroundTint="@color/Pastel_Pink"
	        android:text="@string/button_second"
	        android:onClick="returnReply"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintRight_toRightOf="parent" />
	
	    <EditText
	        android:id="@+id/editText_second"
	        android:layout_width="0dp"
	        android:layout_height="wrap_content"
	        android:layout_marginBottom="16dp"
	        android:layout_marginEnd="8dp"
	        android:layout_marginStart="8dp"
	        android:ems="10"
	        android:hint="@string/editText_second"
	        android:inputType="textLongMessage"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintEnd_toStartOf="@+id/button_second"
	        app:layout_constraintStart_toStartOf="parent" />
	</androidx.constraintlayout.widget.ConstraintLayout>

 ```activity video```

	 <?xml version="1.0" encoding="utf-8"?>
	<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent">
	
	    <VideoView
	        android:id="@+id/trailer"
	        android:layout_width="match_parent"
	        android:layout_height="match_parent"/>
	
	</androidx.constraintlayout.widget.ConstraintLayout>

 ```activity alarm```

	 <?xml version="1.0" encoding="utf-8"?>
	<LinearLayout
	    xmlns:android="http://schemas.android.com/apk/res/android"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    android:orientation="vertical">
	
	    <!--Added Time picker just to pick the alarm time-->
	    <!--gravity is aligned to center-->
	    <TimePicker
	        android:id="@+id/timePicker"
	        android:layout_width="wrap_content"
	        android:headerBackground="@color/Pastel_Pink"
	        android:layout_height="wrap_content"
	        android:layout_gravity="center"
	        android:numbersBackgroundColor="@color/Pastel_Pink"
	        android:numbersTextColor="@color/black"
	        android:numbersSelectorColor="@color/white"
	        android:amPmBackgroundColor="@color/pink"/>
	
	    <!--Added Toggle Button to set the alarm on or off-->
	    <!--ByDefault toggleButton is set to false-->
	    <ToggleButton
	        android:id="@+id/toggleButton"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_gravity="center"
	        android:layout_margin="20dp"
	        android:checked="false"
	        android:onClick="OnToggleClicked"
	        android:backgroundTint="@color/Pastel_Pink"/>
	
	    <!--"OnToggleClicked" method will be implemented in MainActivity.java -->
	
	</LinearLayout>

 ```fragment first```

	 <?xml version="1.0" encoding="utf-8"?>
	<RelativeLayout
	    xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:tools="http://schemas.android.com/tools"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    android:padding="30dp"
	    android:background="@drawable/background"
	    tools:context=".fragment.FirstFragment">
	
	    <TextView
	        android:id="@+id/titleText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:text="EYELINER"
	        android:textStyle="bold"
	        android:textSize="20sp"
	        android:fontFamily="@font/helium"
	        android:layout_centerHorizontal="true"
	        android:textColor="@color/black"
	        android:layout_marginTop="8dp"
	        android:layout_marginBottom="10dp"/>
	
	    <ImageView
	        android:id="@+id/myImage"
	        android:layout_width="250dp"
	        android:layout_height="300dp"
	        android:clickable="true"
	        android:focusable="true"
	        android:layout_alignParentTop="true"
	        android:layout_centerHorizontal="true"
	        android:layout_marginTop="50dp"
	        android:layout_marginBottom="8dp"
	        android:src="@drawable/eyeliner" />
	
	    <TextView
	        android:id="@+id/synopsisText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:text="BPOM NO: NA11211300164"
	        android:fontFamily="@font/helium"
	        android:textSize="19sp"
	        android:textColor="@color/black"
	        android:layout_below="@id/myImage"
	        android:layout_centerHorizontal="true"
	        android:layout_marginTop="8dp"/>
	
	    <TextView
	        android:id="@+id/myText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_below="@id/synopsisText"
	        android:layout_marginTop="10dp"
	        android:textColor="@color/black"
	        android:gravity="center"
	        android:text="@string/eyeliner"
	        android:lineSpacingExtra="3sp"
	        android:textSize="14sp"
	        android:fontFamily="@font/helium"/>
	
	</RelativeLayout>

 ```fragment second```

	 <?xml version="1.0" encoding="utf-8"?>
	<RelativeLayout
	    xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:tools="http://schemas.android.com/tools"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    android:background="@drawable/background"
	    android:padding="30dp"
	    tools:context=".fragment.SecondFragment">
	
	    <TextView
	        android:id="@+id/titleText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:text="LIPCREAM"
	        android:fontFamily="@font/helium"
	        android:textSize="20sp"
	        android:layout_centerHorizontal="true"
	        android:layout_marginTop="8dp"
	        android:layout_marginBottom="10dp"
	        android:textColor="@color/black"/>
	
	    <ImageView
	        android:id="@+id/myImage"
	        android:layout_width="250dp"
	        android:clickable="true"
	        android:focusable="true"
	        android:layout_height="300dp"
	        android:layout_alignParentTop="true"
	        android:layout_centerHorizontal="true"
	        android:layout_marginTop="50dp"
	        android:layout_marginBottom="8dp"
	        android:src="@drawable/lipcream" />
	
	    <TextView
	        android:id="@+id/synopsisText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:text="BPOM NO: NA11211300164"
	        android:fontFamily="@font/helium"
	        android:textSize="19sp"
	        android:textColor="@color/black"
	        android:layout_below="@id/myImage"
	        android:layout_centerHorizontal="true"
	        android:layout_marginTop="8dp" />
	
	    <TextView
	        android:id="@+id/myText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_below="@id/synopsisText"
	        android:layout_marginTop="10dp"
	        android:gravity="center"
	        android:text="@string/lipcream"
	        android:lineSpacingExtra="3sp"
	        android:textSize="14sp"
	        android:fontFamily="@font/helium"
	        android:textColor="@color/black"/>
	
	
	</RelativeLayout>

 ```fragment third```

	 <?xml version="1.0" encoding="utf-8"?>
	<RelativeLayout
	    xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:tools="http://schemas.android.com/tools"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    android:padding="30dp"
	    android:background="@drawable/background"
	    tools:context=".fragment.ThirdFragment">
	
	    <TextView
	        android:id="@+id/titleText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:text="EYEBROW"
	        android:textSize="20sp"
	        android:fontFamily="@font/helium"
	        android:layout_centerHorizontal="true"
	        android:textColor="@color/black"
	        android:layout_marginTop="8dp"
	        android:layout_marginBottom="10dp"/>
	
	    <ImageView
	        android:id="@+id/myImage"
	        android:layout_width="250dp"
	        android:layout_height="300dp"
	        android:clickable="true"
	        android:focusable="true"
	        android:layout_alignParentTop="true"
	        android:layout_centerHorizontal="true"
	        android:layout_marginTop="50dp"
	        android:layout_marginBottom="8dp"
	        android:src="@drawable/eyebrow" />
	
	    <TextView
	        android:id="@+id/synopsisText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:text="BPOM NO: NA11211200461"
	        android:fontFamily="@font/helium"
	        android:textSize="19sp"
	        android:textColor="@color/black"
	        android:layout_below="@id/myImage"
	        android:layout_centerHorizontal="true"
	        android:layout_marginTop="8dp"/>
	
	    <TextView
	        android:id="@+id/myText"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_below="@id/synopsisText"
	        android:layout_marginTop="10dp"
	        android:textColor="@color/black"
	        android:gravity="center"
	        android:text="@string/eyebrow"
	        android:lineSpacingExtra="3sp"
	        android:textSize="14sp"
	        android:fontFamily="@font/helium"
	        android:textStyle="bold"/>
	</RelativeLayout>
