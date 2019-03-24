# helloworldlayout
## 实验一：helloworld及activity生命周期
### 主要代码：
```
public class helloworld extends AppCompatActivity {

    Button bt;
    final String tag="hello world!";

    /**
     * Activity创建时被调用
     * @param savedInstanceState
     */
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_helloworld);
        Log.d(tag,"onCreate is invoke!!!");
        //setContentView(R.layout.linearlayout);//调用线性布局
        //setContentView(R.layout.relativelayout);//调用约束布局
        //setContentView(R.layout.tablelayout);//调用表格布局
        //快捷键注释Ctrl+/
    }

    /**
     *Activity创建或者从后台重新回到前台时被调用
     */
    @Override
    protected void onStart() {
        super.onStart();
        Log.d(tag,"onStart is invoke!!!");
    }

    /**
     *Activity创建或者从被覆盖、后台重新回到前台时被调用
     */
    @Override
    protected void onResume() {
        super.onResume();
        Log.d(tag,"onResume is invoke!!!");
    }

    /**
     *  Activity被覆盖到下面或者锁屏时被调用
     */
    @Override
    protected void onPause() {
        super.onPause();
        Log.d(tag,"onPause is invoke!!!");
    }

    /**
     *退出当前Activity或者跳转到新Activity时被调用
     */
    @Override
    protected void onStop() {
        super.onStop();
        Log.d(tag,"onStop is invoke!!!");
    }

    /**
     *退出当前Activity时被调用,调用之后Activity就结束了
     */
    @Override
    protected void onDestroy() {
        super.onDestroy();
        Log.d(tag,"onDestroy is invoke!!!");
    }

    /**
     * Activity从后台重新回到前台时被调用
     */
    @Override
    protected void onRestart() {
        super.onRestart();
        Log.d(tag,"onRestart is invoke!!!");
    }
}
```
### 结果截图：
![image](https://github.com/Magicpanda-orz/helloworld/blob/master/helloworld.PNG)
##    
![image](https://github.com/Magicpanda-orz/helloworld/blob/master/activity.PNG)

## 实验二：三种布局的设计
### LinearLayout主要代码：
```
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".helloworld"
android:orientation="vertical"
android:background="#000000">

<LinearLayout
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:orientation="horizontal">

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#000000"
        android:layout_marginTop="3dip"
        android:layout_marginLeft="3dip"
        android:textColor="#ffffff"
        tools:text="One,One"/>

    <Button
        android:layout_width="115dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:textColor="#ffffff"
        tools:text="One,Two" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:textColor="#ffffff"
        tools:text="One,Three" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#000000"
        android:layout_marginTop="3dip"
        android:layout_marginLeft="3dip"
        android:textColor="#ffffff"
        tools:text="One,Four"/>

</LinearLayout>

<LinearLayout
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:orientation="horizontal"
    >

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#000000"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:text="Two,One"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="115dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:text="Two,Two"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:text="Two,Three"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#000000"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:textColor="#ffffff"
        android:text="Two,Four"/>

</LinearLayout>
<LinearLayout
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:orientation="horizontal"
    >

    <Button
        android:layout_width="99dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:text="Three,One"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:text="Three,Two"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="103dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:text="Three,Three"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:text="Three,Four"
        android:textColor="#ffffff" />

</LinearLayout>
<LinearLayout
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:orientation="horizontal"
    >

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#000000"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:text="Four,One"
        android:textColor="#ffffff" />

    <Button

        android:layout_width="115dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:background="#000000"
        android:text="Four,Two"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#000000"
        android:layout_marginTop="3dip"
        android:layout_marginLeft="3dip"
        android:textColor="#ffffff"
        android:text="Four,Three"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#000000"
        android:layout_marginLeft="3dip"
        android:layout_marginTop="3dip"
        android:textColor="#ffffff"
        android:text="Four,Four"/>
```
### 结果截图：
![image](https://github.com/Magicpanda-orz/helloworld/blob/master/linearlayout.PNG)
### RelativeLayout主要代码：
```
 <Button
        android:id="@+id/b1"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:background="#ff0000"
        android:textColor="#000000"
        tools:text="Red"
        android:layout_marginLeft="3dp" />

    <Button
        android:id="@+id/b2"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:background="#ff8247"
        android:textColor="#000000"
        tools:text="orange"
        android:layout_marginLeft="152dp" />

    <Button
        android:id="@+id/b3"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:background="#fff000"
        android:textColor="#000000"
        tools:text="yellow"
        android:layout_marginLeft="302dp" />

    <Button
        android:id="@+id/b4"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginTop="100dp"
        android:background="#b3ee3a"
        android:textColor="#000000"
        tools:text="green"
        android:layout_marginLeft="80dp" />

    <Button
        android:id="@+id/b5"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginTop="100dp"
        android:background="#6495ED"
        android:textColor="#000000"
        tools:text="blue"
        android:layout_marginLeft="170dp" />

    <Button
        android:id="@+id/b6"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginTop="100dp"
        android:background="#4b0082"
        android:textColor="#000000"
        tools:text="indigo"
        android:layout_marginLeft="260dp" />

    <Button
        android:id="@+id/b7"
        android:layout_width="match_parent"
        android:layout_height="80dp"
        android:layout_marginTop="200dp"
        android:background="#BA55D3"
        android:textColor="#000000"
        tools:text="violef" />
      
```
### 结果截图：
![image](https://github.com/Magicpanda-orz/helloworld/blob/master/relativelayout.PNG)
### TableLayout主要代码：
```
<TableLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:stretchColumns="1"
    android:background="#000000">

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Open..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-O"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>

    </TableRow>

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Save..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-S"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>
    </TableRow>

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Save As..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-Shift-S"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>
    </TableRow>

    <View
        android:layout_height="2dip"
        android:background="#ffffff"/>
    <TableRow>
        <TextView
            android:text="X"
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Import..."
            android:textColor="#ffffff"
            android:padding="3dip"/>
    </TableRow>
    <TableRow>
        <TextView
            android:text="X"
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Emport..."
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Ctrl-E"
            android:gravity="right"
            android:textColor="#ffffff"
            android:padding="3dip"/>
    </TableRow>
    <View
        android:layout_height="2dip"

        android:background="#ffffff"/>
    <TableRow>
        <TextView
            android:layout_column="1"
            android:textColor="#ffffff"
            android:text="Quit"
            android:padding="3dip"/>
    </TableRow>

</TableLayout>
```
### 结果截图：
![image](https://github.com/Magicpanda-orz/helloworld/blob/master/tablelayout.PNG)
