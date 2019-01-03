# FlycoTabLayoutZ
在FlycoTabLayout的基础上，扩展出SlidingScaleTabLayout，实现滑动可以改变tab字体的大小的切换效果

首先感谢FlycoTabLayout原作者的开源精神，关于FlycoTabLayout原本的具体用法请移步：
<br /> 
https://github.com/H07000223/FlycoTabLayout
  
## 新增SlidingScaleTabLayout
SlidingScaleTabLayout继承SlidingTabLayout，支持SlidingScaleTabLayout的全部特性。
<br />
<img src="https://img-blog.csdnimg.cn/20190103170923648.gif" />

使用说明：

<br />

1、添加gradle配置：

<br />

    compile 'com.lzp:FlycoTabLayoutZ:1.0.2'
    
    
2、新增设置tab被选中以及未被选中的文字大小，大小的变化会在ViewPager滑动的时候自动变化：
<br />

    <attr name="tl_textSelectSize" />
    <attr name="tl_textUnSelectSize" />
    
3、标题默认默认是文字居中，可以修改gravity和margin属性，设置在tab中的位置：
<br />

    <attr name="tl_tab_marginTop" />
    <attr name="tl_tab_marginBottom" />
    <attr name="tl_tab_gravity" />
    
## 示例

xml:
<br />

    <com.flyco.tablayout.SlidingScaleTabLayout
        android:id="@+id/tablayout"
        android:layout_width="match_parent"
        android:layout_height="50dp"
        app:tl_indicator_color="@color/colorAccent"
        app:tl_indicator_corner_radius="3dp"
        app:tl_indicator_gravity="BOTTOM"
        app:tl_indicator_height="2dp"
        app:tl_indicator_width="7dp"
        app:tl_textBold="SELECT"
        app:tl_tab_gravity="Bottom"
        app:tl_tab_marginBottom="8dp"
        app:tl_tab_padding="15dp"
        app:tl_textSelectColor="@color/colorPrimary"
        app:tl_textSelectSize="20sp"
        app:tl_textUnSelectColor="@color/colorPrimaryDark"
        app:tl_textUnSelectSize="14sp" />
        
Java:
<br />

    SlidingScaleTabLayout tabLayout = findViewById(R.id.tablayout);
    ViewPager viewPager = findViewById(R.id.viewpager);
    viewPager.setAdapter(new MyViewPagerAdapter());
    viewPager.setOffscreenPageLimit(4);
    tabLayout.setViewPager(viewPager);
    
更多使用示例，请参考demo。
<br/>
如果您觉得不错，感谢打赏一个猪蹄：

<img width=400 height=400 src="https://camo.githubusercontent.com/9a9587578e25bb3bc917c25cd772ab3ae554e4c7/68747470733a2f2f696d672d626c6f672e6373646e2e6e65742f323031383036313931383539343333343f77617465726d61726b2f322f746578742f6148523063484d364c7939696247396e4c6d4e7a5a473475626d56304c3355774d54457a4d5455354e6a413d2f666f6e742f3561364c354c32542f666f6e7473697a652f3430302f66696c6c2f49304a42516b46434d413d3d2f646973736f6c76652f3730"/>

如果在使用过程中遇到问题或者有更好的建议，欢迎发送邮件到：</br>

lzp-541@163.com
