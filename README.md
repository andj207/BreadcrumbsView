# BreadcrumbsView

[![](https://jitpack.io/v/HamidrezaAmz/BreadcrumbsView.svg)](https://jitpack.io/#HamidrezaAmz/BreadcrumbsView)
[![API](https://img.shields.io/badge/API-17%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=17)

## New Futures
Custom Font Added

Custom Text Size Added

Custom Text Color ( Selected,UnSelected ) Added

Min API **17**

Migrated To **AndroidX**

<img src="./.readme/breadcrumbsview.png" width="30%"/>

Material Design Breadcrumbs Navigation Widget on Android

<img src="./.readme/screenshot-demo.png" width="50%"/>

## How to use

### Import (Gradle)

First, add it in your root build.gradle at the end of repositories:

```gradle
allprojects {
	repositories {
		maven { url 'https://jitpack.io' }
	}
}
```

Add the dependency to your app modules:

```gradle
dependencies {
    	implementation 'com.github.HamidrezaAmz:BreadcrumbsView:0.2.3'
}
```

### XML

Place a `BreadcrumbsView` to where you want in your layout xml.

For example:

```xml
<moe.feng.common.view.breadcrumbs.BreadcrumbsView
	android:id="@+id/breadcrumbs_view"
	android:layout_width="match_parent"
	android:layout_height="?attr/actionBarSize"
	app:popupTheme="@style/AppTheme.PopupOverlay"
	app:textColorSelected="@color/colorSelected"
        app:textColorUnSelected="@color/colorUnSelected"
        app:textSizeCustom="12sp" />
```

### Add/Remove `BreadcrumbItem`

When your interface navigates to next step, create a new `BreadcrumbItem` and add it to `BreadcrumbsView`. (After 0.2.0, you can implement your own `IBreadcrumbItem` to use.)

Use `removeItemAfter(int)` or `removeLastItem` to remove items or last item.

### Listen events

You can set a callback for `BreadcrumbsView` to receive item click/changed events.

To simplify events, I recommend to use `DefaultBreadcrumbsCallback` :

```java
new DefaultBreadcrumbsCallback<BreadcrumbItem>() {
	@Override
	public void onNavigateBack(BreadcrumbItem item, int position) {
		// ...
	}

	@Override
	public void onNavigateNewLocation(BreadcrumbItem newItem, int changedPosition) {
		// ...
	}
}
```

## License

```
MIT License

Copyright (c) 2017-2018 Fung Go (fython)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
