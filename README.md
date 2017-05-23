# AlphaTabsIndicator
High imitation microblogging at the bottom of the status bar of the lightweight library for most of the bottom status bar application requirements.
## Abstract
Imitation WeChat at the bottom of the tab label, slide the color gradient, increase the angle mark function, the use of extremely simple, only two lines of code.

## Chinese Documents
[查看中文文档](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/READEME_CN.md)

## Gif
![1](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/show.gif)

## Screenshot
![1](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/Screenshot1.png)
![2](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/Screenshot2.png)
![3](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/Screenshot3.png)
![4](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/Screenshot4.png)

## Demo
[Download Demo](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/app-debug.apk)

## Usage
### Step 1
#### Gradle
```
dependencies {
    compile 'com.yinglan.alphatabs:library:1.0.8'
}
```

### Step 2

#### In Layout
```
	        <com.yinglan.alphatabs.AlphaTabsIndicator
                android:id="@+id/alphaIndicator"
                android:layout_width="match_parent"
                android:layout_height="55dp"
                android:orientation="horizontal">

                <com.yinglan.alphatabs.AlphaTabView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:padding="5dp"

                    app:tabIconNormal=""
                    app:tabIconSelected=""
                    app:tabText=""
                    app:tabTextSize=""
                    app:textColorNormal=""
                    app:textColorSelected=""
                    app:badgeBackgroundColor=""
                    app:paddingTexwithIcon=""/>

                <com.yinglan.alphatabs.AlphaTabView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:padding="5dp"

                    app:tabIconNormal=""
                    app:tabIconSelected=""
                    app:tabText=""
                    app:tabTextSize=""
                    app:textColorNormal=""
                    app:textColorSelected=""
                    app:badgeBackgroundColor=""
                    app:paddingTexwithIcon=""/>

                    、、、、
                    、、、、

            </com.yinglan.alphatabs.AlphaTabsIndicator>                                //模式
```
#### Function and parameter definition

<table>
  <tdead>
    <tr>
      <th align="center">Parameters</th>
      <th align="center">Meaning</th>
    </tr>
  </tdead>
  <tbody>
    <tr>
      <td align="center">tabIconNormal</td>
      <td align="center">Unselected icon</td>
    </tr>
    <tr>
      <td align="center">tabIconSelected</td>
      <td align="center">Already selected icon</td>
    </tr>
    <tr>
      <td align="center">tabText</td>
      <td align="center">Tab tag text</td>
    </tr>
    <tr>
      <td align="center">tabTextSize</td>
      <td align="center">Tab The size of the label</td>
    </tr>
    <tr>
      <td align="center">textColorNormal</td>
      <td align="center">Unchecked text color</td>
    </tr>
    <tr>
      <td align="center">textColorSelected</td>
      <td align="center">Selected text color</td>
    </tr>
    <tr>
        <td align="center">badgeBackgroundColor</td>
        <td align="center">Corner background color, default red</td>
     </tr>
     <tr>
        <td align="center">paddingTexwithIcon</td>
        <td align="center">The distance between the icon and text</td>
     </tr>
  </tbody>
</table>


#### In Code

##### AlphaTabView Main Method
```
        mAlphaTabView.showNumber(int i); //Display digital remind
        mAlphaTabView.showPoint();       //Show little red dot
        mAlphaTabView.removeShow();      //Remove the digital remind
```

##### AlphaTabsIndicator Main Method
```
        mAlphaTabsIndicator.setViewPager(ViewPager mViewPger);                     //Set ViewPager
        mAlphaTabsIndicator.setOnTabChangedListner(OnTabChangedListner listner);   //Settings TAB at the bottom click to monitor
        mAlphaTabsIndicator.removeAllBadge();                                      //Remove all remind the TAB
        mAlphaTabsIndicator.setTabCurrenItem(int tabIndex);                        //Settings TAB option
```

#### Instructions
The library is in the permission of the Mr [jeasonlzy](https://github.com/jeasonlzy) permission,on the basis of his [AlphaIndicatorView](https://github.com/jeasonlzy/AlphaIndicatorView) do usability improvements, thank you, now continue to open source.
## The main improvement:
1. Increase the Angle of standard, make it more close to WeChat TAB at the bottom;
1. The diagonal mark size for dynamic control, adaptive according to the height of the TAB;
1. Limit the appropriate to reduce to use requirement, can be used in the case of not binding viewpager;
1. When without binding ViewPager Settings TAB option;
1. The distance between the icon and text can be configured, the default is 5;
1. Increase click on the TAB to monitor the callback;
1. Increase in code mViewPager. SetCurrentItem (i) TAB linkage control condition;
1. Repair is not set in a state of not click Tab.