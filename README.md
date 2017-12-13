# MaterialPlayPauseView
 
A View that can be toggled between play/pause states with Material Design animation.

This an improvement over [OHoussein's fork of PlayPauseView](https://github.com/OHoussein/android-material-play-pause-view).

Fixes from there:
* Fix for button state getting confused with rapid toggle events
* Proper publication mechanism

<div  align="center">    
<img src="./media/demo.gif" alt="demo" align=center />
</div>

**Usage Sample**

For now, add my Bintray repository to your `repositories` block (jcenter coming soon):
```groovy
repositories {
    maven { url 'https://dl.bintray.com/zsmb13/android-material-play-pause-view/' }
}
```

And then the dependency itself:

```groovy
dependencies {
    implementation 'co.zsmb:playpauseview:1.0.4'
}
```

#### layout

```xml
<com.ohoussein.playpause.PlayPauseView
    android:id="@+id/play_pause_view"
    android:layout_width="200dp"
    android:layout_height="200dp"
    android:clickable="true"
    android:foreground="?android:selectableItemBackground"
    app:fill_color="#e1e1e1"
    app:pause_bg="#00a2ed"
    app:play_bg="#001eff" />
```

* pause_bg : the background for the pause status
* play_bg : the background for the play status
* fill_color: the icon's color

#### Java

```java
PlayPauseView view = (PlayPauseView) findViewById(R.id.play_pause_view);
view.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        view.toggle();
    }
});
```

You can use also `PlayPauseView#change(boolean isPlay)` to change play/pause state with animation.

# License

The MIT License (MIT)

Copyright (c) 2017 Márton Braun

Copyright 2016 OHoussein

Copyright (c) 2015 Alex Lockwood

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
