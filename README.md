[![](https://jitpack.io/v/pao11/WheelView3DRelease.svg)](https://jitpack.io/#pao11/WheelView3DRelease)


# WheelView-3D
### Camera, Matrix 实现WheelView 3D效果

### 效果图

![纵向排列](https://github.com/pao11/WheelView3DRelease/blob/master/imgs/1122.png)

## Gradle 添加引用
```
compile 'com.github.pao11:WheelView3DRelease:v1.0.0' 
```

## 属性介绍

```
<declare-styleable name="WheelView">
        <!-- 中间分割线外的item数量,整个滑动数量就为 wheelItemCount * 2 + 1  -->
        <attr name="wheelItemCount" format="integer"/>
        <!-- 滑轮item高度 -->
        <attr name="wheelItemSize" format="dimension"/>
        <!-- 滑轮字体大小 -->
        <attr name="wheelTextSize" format="dimension"/>
        <!-- 滑轮字体颜色 -->
        <attr name="wheelTextColor" format="color"/>
        <!-- 滑轮中心字体颜色 -->
        <attr name="wheelTextColorCenter" format="color"/>
        <!-- 分割线颜色 -->
        <attr name="dividerColor" format="color"/>
        <!-- 布局方向 -->
        <attr name="wheelOrientation">
            <enum name="vertical" value="1"/>
            <enum name="horizontal" value="2"/>
        </attr>
        <!-- 两根分割线的距离 -->
        <attr name="wheelDividerSize" format="dimension"/>
    </declare-styleable>

```

## Usage  使用

```
<com.pao11.wheelviewlibrary.WheelView
        android:id="@+id/wv_number"
        android:layout_width="wrap_content"
        android:layout_height="60dp"
        android:layout_gravity="center_horizontal"
        app:wheelItemCount="3"
        app:wheelItemSize="35dp"
        app:wheelDividerSize="38dp"
        app:wheelOrientation="horizontal"
        app:wheelTextSize="25sp"/>

wv_number.setAdapter(new WheelView.WheelAdapter() {
            @Override
            protected int getItemCount() {
                return 100;
            }

            @Override
            protected String getItem(int index) {
                return String.valueOf(index);
            }
        });
        wv_number.setOnItemSelectedListener(new WheelView.OnItemSelectedListener() {
            @Override
            public void onItemSelected(int index) {
                tv_number.setText("水平布局"+index);
            }
        });
        wv_number.setCurrentItem(88);

```
## Apk download
![wheelview.apk](https://github.com/pao11/WheelView3DRelease/blob/master/imgs/wheelview.apk)


##更新记录

 **v1.0.0**　`2017.10.11`　发布第一个版本--SDK VERSION 24.2.0
 

## License

```
Copyright 2017 pao11

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```




