本repo fork出来只是修改了滑动返回的阴影效果。修改后的效果为底下的Fragment盖上了透明的灰色，而不是固定的阴影跟随滑动。 
这些修改也没有重新build并上传到maven。若有需要上述效果，请自行进行源码依赖。  

以下为原repo的README

# ParallaxBackLayout
[![Download](https://api.bintray.com/packages/anzewei/maven/com.github.anzewei/images/download.svg)](https://bintray.com/anzewei/maven/com.github.anzewei/_latestVersion)

Finish an Activity with parallax scrolling effect.

[![Watch the video](https://github.com/anzewei/ParallaxBackLayout/blob/master/ext/video.png)](https://youtu.be/6da7UZh8MRk)
# Demo Apk

<a href="https://github.com/anzewei/ParallaxBackLayout/blob/master/ext/demo.apk?raw=true">DOWNLOAD</a>


<a href="https://github.com/anzewei/ParallaxBackLayout/blob/master/README_ZH.md">简体中文</a>

# Usage

## Step 1

- Add these lines to your build.gradle

``` groovy
compile 'com.github.anzewei:parallaxbacklayout:lastversion'
``` 
	
## Step 2

- register ParallaxHelper to application

``` java
  registerActivityLifecycleCallbacks(ParallaxHelper.getInstance());
```
- Add annontion to  the activity you want to parallax back

``` java
@ParallaxBack
public class DetailActivity extends AppCompatActivity {
 。。。
}
```
# Other Usage



``` java
@ParallaxBack
public class DetailActivity extends AppCompatActivity {
     private void disableBack(){
         ParallaxHelper.getInstance().getParallaxBackLayout(this).setEnableGesture(false);
     }
}
```

# Update
- Date 2017.05.16  Version  1.0
    Use annotation 

# License

Copyright 2017 anzewei

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
