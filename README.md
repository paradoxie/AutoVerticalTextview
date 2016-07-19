# AutoVerticalTextview
垂直滚动的textview，继承自TextSwitcher，抽出一个依赖库供以后备用


### 使用方法

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