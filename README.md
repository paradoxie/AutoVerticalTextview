# AutoVerticalTextview
垂直滚动的textview，继承自TextSwitcher，抽出一个依赖库供以后备用


### 配置方法

项目*build.gradle*文件内:
````
    allprojects {
    		repositories {
    			...
    			maven { url "https://jitpack.io" }
    		}
    	}

````
module内*build.gradle*添加依赖:
  ````
  dependencies {
    	        compile 'com.github.paradoxie:AutoVerticalTextview:0.1'
    	}

````
### 使用方法

xml文件里:
````
    <com.paradoxie.autoscrolltextview.VerticalTextview
            android:id="@+id/text"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
           />
````

activity里:
````
        TextView.setTextList(titleList);//加入显示内容,集合类型
        TextView.setText(26, 5, Color.RED);//设置属性,具体跟踪源码
        TextView.setTextStillTime(3000);//设置停留时长间隔
        TextView.setAnimTime(300);//设置进入和退出的时间间隔
        //对单条文字的点击监听
        TextView.setOnItemClickListener(new VerticalTextview.OnItemClickListener() {
                    @Override
                    public void onItemClick(int position) {
                    // TO DO
                    }
                });

````
        //开始滚动
        @Override
            protected void onResume() {
                super.onResume();
                TextView.startAutoScroll();
            }
        //停止滚动
        @Override
            protected void onPause() {
                super.onPause();
                TextView.stopAutoScroll();
            }
````