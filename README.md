# 1 实验内容
- 安装AndroidStudio4.1+以上版本，后续更好的使用 TensorFlowLite
- 按照教程构建首个Kotlin交互应用
- 上传代码至Github，并撰写详细的Readme文档
  
# 2 实验记录
## 2.1 项目准备与虚拟环境
打开Android Studio。选择File下的new project。

![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554195250-319adbc0-be7a-4377-a8d9-154a3fc735d4.png#averageHue=%23dbbe8c&clientId=ub579683e-d055-4&from=paste&height=217&id=ub91151fd&originHeight=298&originWidth=852&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=57590&status=done&style=none&taskId=u0cc7420b-daf9-409d-82a1-1f9192195bc&title=&width=619.6363636363636)

选择项目的基础交互页面。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554240674-64b28302-3a0b-4a28-917d-e6f0330e8ad0.png#averageHue=%23e9f1f3&clientId=ub579683e-d055-4&from=paste&height=591&id=u0a295cf7&originHeight=813&originWidth=1126&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=129789&status=done&style=none&taskId=u87b5063b-721a-4344-b605-9fbc3da0200&title=&width=818.9090909090909)<br />选择项目路径。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554298708-af303b33-add0-4981-b2c0-23aa70c7ba7b.png#averageHue=%23f2f4f8&clientId=ub579683e-d055-4&from=paste&height=591&id=u3b647909&originHeight=813&originWidth=1126&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=85075&status=done&style=none&taskId=u95b893ca-4130-4042-b520-8fb082a9ae7&title=&width=818.9090909090909)<br />进入项目，等待相关的依赖安装。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554337143-2fddb018-e0a8-47cb-9660-04f5855c8357.png#averageHue=%23edeef1&clientId=ub579683e-d055-4&from=paste&height=749&id=u041966d6&originHeight=1030&originWidth=1920&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=205727&status=done&style=none&taskId=u1cc3b66d-d429-4729-a25b-2bd76b7f573&title=&width=1396.3636363636363)<br />然后，为了能够运行Android的程序，我们可以用安卓的手机进行调试，也可以通过安装虚拟设备的方式，运行。这里我们选择安装虚拟环境。<br />在右边的侧边栏上，点击device manageer。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554571697-f147eed3-0b34-4f23-a8c5-5f8e227bab92.png#averageHue=%23d8dade&clientId=ub579683e-d055-4&from=paste&height=276&id=u7fc2908b&originHeight=380&originWidth=460&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=26469&status=done&style=none&taskId=uc8b408d4-4b77-4db3-9f7a-29eb1ea1b96&title=&width=334.54545454545456)<br />然后点击“+”号，添加虚拟设备。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554620288-57e6ebc9-481b-4f23-9efb-19cf8c016c72.png#averageHue=%23d8dade&clientId=ub579683e-d055-4&from=paste&height=276&id=ua061b88b&originHeight=380&originWidth=460&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=26537&status=done&style=none&taskId=u48fe8d37-088c-4222-90dc-338d741f895&title=&width=334.54545454545456)<br />根据实际情况以及配置选择合适的设备。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554650615-2fa97df5-0cf3-40d3-8c5b-c726187a17be.png#averageHue=%237ea3c2&clientId=ub579683e-d055-4&from=paste&height=628&id=u62777957&originHeight=864&originWidth=1376&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=135931&status=done&style=none&taskId=ue813548d-dd50-421e-9f8f-adbc8901bc6&title=&width=1000.7272727272727)<br />然后对这个设备选择一个虚拟镜像进行配置。这里可能要对镜像进行安装，请确保流畅的网络环境。下载完成之后，选中这个镜像，点击“next"。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554755972-7bf034be-6762-4a2d-8abf-c8dae927998d.png#averageHue=%23b2c4c5&clientId=ub579683e-d055-4&from=paste&height=628&id=ud36877ba&originHeight=864&originWidth=1376&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=175974&status=done&style=none&taskId=u72144c0e-12e8-449b-9927-d160063a5d5&title=&width=1000.7272727272727)<br />之后，确认这个虚拟设备的配置，点击”finish“。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554803203-a5bf7ff7-1c5c-4718-a53d-ffc162c1cac2.png#averageHue=%2396bd9c&clientId=ub579683e-d055-4&from=paste&height=628&id=ue33e991c&originHeight=864&originWidth=1376&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=98194&status=done&style=none&taskId=u9bc93546-2ecf-4524-9ef3-5731db9188e&title=&width=1000.7272727272727)<br />当虚拟设备安装完成之后，右侧边栏的device manager处将会出现所安装的虚拟设备（包括其名称，与其他配置）。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714554919669-dc6e50d2-bfb6-4132-997e-6b26dcbf2ff8.png#averageHue=%23f1f3f7&clientId=ub579683e-d055-4&from=paste&height=175&id=uf51f81d6&originHeight=241&originWidth=445&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=20520&status=done&style=none&taskId=u2881a4b4-6a84-4ce8-ae53-9183c7be8af&title=&width=323.6363636363636)<br />之后可以尝试启动虚拟设备。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714704042704-23f182f3-c764-49e6-97d2-defb5cedc86b.png#averageHue=%234a524b&clientId=u641e9078-6c2e-4&from=paste&height=649&id=u5fc04f9d&originHeight=892&originWidth=823&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=65149&status=done&style=none&taskId=u9cd1caaf-9ffa-4400-a8a8-78a987e573e&title=&width=598.5454545454545)<br />左上角的电源键表示开机
## 2.2 first Fragment的外观设置
basic Activity 有两个fragment组成，分别是first fragment和second fragment。<br />我们需要对这两个fragment的外观进行设置，满足项目的要求。首先是对first Fragment的外观设置。<br />first Fragment的设置信息放在了`res/layout/fragment_first.xml`，并且我们可以通过图片image或者代码code的形式进行修改。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714555226596-9fc47361-aea7-4cdf-a93a-064e6c109d88.png#averageHue=%23fefdfc&clientId=ub579683e-d055-4&from=paste&height=684&id=u7a028e42&originHeight=941&originWidth=1104&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=171079&status=done&style=none&taskId=u0507a0ff-6a8b-4c3a-983d-f52e978b497&title=&width=802.9090909090909)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714658808598-45eecff8-a21d-48c5-b2f2-3c58ee06b148.png#averageHue=%23cddbe1&clientId=u84a0f0a5-5448-4&from=paste&height=591&id=ued76ab9a&originHeight=813&originWidth=1167&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=146294&status=done&style=none&taskId=uc79013a4-e852-4bcd-81aa-9a3cd4dd66b&title=&width=848.7272727272727)<br />查看布局的代码（Code），修改Textview的text属性。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714658861497-f81cff43-fef8-4a1f-aa0e-ff7b827bc9e1.png#averageHue=%23e6f0df&clientId=u84a0f0a5-5448-4&from=paste&height=39&id=ua06492af&originHeight=53&originWidth=1150&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=10029&status=done&style=none&taskId=ub9d86600-4a34-44be-b2cc-f232ca8fdce&title=&width=836.3636363636364)<br />右键该代码，选择Go To > Declaration or Usages，跳转到values/strings.xml，看到高亮文本。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714658944592-2f4edb82-2934-46da-986f-283b123f632f.png#averageHue=%23f3f1ef&clientId=u84a0f0a5-5448-4&from=paste&height=518&id=u8509a21e&originHeight=712&originWidth=1469&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=156430&status=done&style=none&taskId=u89692b8a-ad74-4be2-9688-57735ee9eb0&title=&width=1068.3636363636363)<br />修改字符串属性值为“Hello Kotlin!”。随后，对应的text的值也就随之改变。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714659021695-1da5d659-da74-4260-8553-7579e7f9e336.png#averageHue=%23f5f1fa&clientId=u84a0f0a5-5448-4&from=paste&height=196&id=u50d9713f&originHeight=270&originWidth=526&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=8900&status=done&style=none&taskId=ub0f18080-108f-49c9-a672-d1d16460bd8&title=&width=382.54545454545456)<br />更进一步，修改字体显示属性，在Design视图中选择textview_first文本组件，在Common Attributes属性下的textAppearance域，设置相关的文字显示属性，修改了如下红标地方的属性设置。<br />当然也可以通过添加如下的XML代码，添加新的属性。<br />查看布局的XML代码，可以看到新属性被应用。
```python
android:fontFamily="sans-serif-condensed"
android:text="@string/hello_first_fragment"
android:textColor="@android:color/darker_gray"
android:textSize="30sp"
android:textStyle="bold"
```

---

然后，我们要对项目的颜色做出一些规定。<br />首先，我们要为背景和按钮定义一些新的颜色，而alues>colors.xml定义了一些应用程序可以使用的颜色。我们添加如下的颜色。
```python
<color name="screenBackground">#2196F3</color>
<color name="buttonBackground">#BBDEFB</color>
```
然后，将fragment_first.xml的属性面板中设置屏幕背景色为：
```python
android:background="@color/screenBackground"
```
设置每个按钮的背景色为buttonBackground：
```python
android:background="@color/buttonBackground"
```
移除TextView的背景颜色，设置TextView的文本颜色为#ffffff，并增大字体大小至64sp。
```python
android:textColor="#ffffff"
android:textSize="64sp"
```

---

其次，我们要添加first Fragment中的必要的组件。<br />在fragment_first.xml的图像界面的左边，通过点击Button，并拖动，添加两个Button。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714659936458-0b144ce0-5665-4fbe-bc1b-c1c5ab2839ea.png#averageHue=%23cedae1&clientId=u84a0f0a5-5448-4&from=paste&height=449&id=ucf3a3f64&originHeight=618&originWidth=1240&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=96765&status=done&style=none&taskId=u9fdc0f7f-f1b0-4c22-b0c5-68bfd170adf&title=&width=901.8181818181819)<br />添加了Button之后，可以回到code界面，找到刚才添加的两个Button。将其id分别改成toast_button和count_button。并且将自带的button的id改成random_button。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660317092-6f21fc30-ff06-4838-8918-87d40238e5c1.png#averageHue=%23fefefc&clientId=u84a0f0a5-5448-4&from=paste&height=49&id=u9a2e0076&originHeight=67&originWidth=575&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=7007&status=done&style=none&taskId=u49ca2cdc-7982-43c2-83c9-0682694e69a&title=&width=418.1818181818182)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660327367-d0c9ec99-e772-4bd9-8837-c12ce0470ffd.png#averageHue=%23fefefd&clientId=u84a0f0a5-5448-4&from=paste&height=46&id=u9a20ae48&originHeight=63&originWidth=525&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=6498&status=done&style=none&taskId=u99f2ae82-7491-4d92-83d1-dbebe65fb8d&title=&width=381.8181818181818)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660341801-64312c77-e05c-4dd3-8faa-7531def92e36.png#averageHue=%23fdfdfb&clientId=u84a0f0a5-5448-4&from=paste&height=38&id=ub4e6345d&originHeight=52&originWidth=489&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=5850&status=done&style=none&taskId=u44d3e53a-3c25-4b33-acbc-ef2be70e127&title=&width=355.6363636363636)<br />对于random_button，找到对应的text属性，按住crtl，然后点击引号内容，跳转到对应的string上。将其修改成Random。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660611524-68a01037-0c1d-477f-a172-f12b2d105df2.png#averageHue=%232c965b&clientId=u84a0f0a5-5448-4&from=paste&height=46&id=u571de1f5&originHeight=63&originWidth=453&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=8375&status=done&style=none&taskId=uf9286977-1d97-41dd-bd49-c2327c1eddc&title=&width=329.45454545454544)		<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660631389-3511f1fa-5693-4d07-a975-f6002cc68303.png#averageHue=%2382cdc3&clientId=u84a0f0a5-5448-4&from=paste&height=38&id=u302dc410&originHeight=55&originWidth=586&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=8083&status=done&style=none&taskId=u4bd92e6d-60ed-47c5-9c68-13589e9c49c&title=&width=407.18182373046875)<br />对于toast_button和count_button，在xml的对应位置，将鼠标放到text的位置，然后点击提示块的“extract string resource”，动态创建对应Button的文本内容。<br />然后在values处，修改对应的值为Toast和Count。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660106627-498bf900-4dd1-4ef7-999c-3a44f495a6ee.png#averageHue=%23fdfaf8&clientId=u84a0f0a5-5448-4&from=paste&height=269&id=u91be1b7d&originHeight=370&originWidth=1089&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=66323&status=done&style=none&taskId=u147ace17-e337-4add-9fcc-d086c6d7458&title=&width=792)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660731645-2257a9e2-8f47-49ad-b5fb-efca826a007a.png#averageHue=%23fcfbfa&clientId=u84a0f0a5-5448-4&from=paste&height=73&id=u0fcc7a1e&originHeight=101&originWidth=809&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=16338&status=done&style=none&taskId=uc68e3a26-380f-4a69-91a4-b6b49da5d7c&title=&width=588.3636363636364)<br />同时，将textview的文本内容改成0。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660811812-a3076d10-bc7a-47ff-8022-e3878f5eb56a.png#averageHue=%235b9f47&clientId=u84a0f0a5-5448-4&from=paste&height=64&id=ufdadaa4b&originHeight=88&originWidth=769&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=14891&status=done&style=none&taskId=ufd062efd-c8e9-45aa-bf0a-304ac8344b5&title=&width=559.2727272727273)<br />之后，回到fragment_first.xml，查看情况。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660878252-4fe61175-731f-4e90-a4a3-83a2c44b227d.png#averageHue=%2341a4f3&clientId=u84a0f0a5-5448-4&from=paste&height=515&id=ud174062e&originHeight=708&originWidth=402&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=12350&status=done&style=none&taskId=u4b55f24c-dfcc-46ed-a58c-bdeb60064e5&title=&width=292.3636363636364)

---

之后，我们对这几个组件进行布局。<br />在fragment_first.xml，查看TextView组件的约束属性：<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714659370422-f4fe92d0-0139-408c-ba06-131a0d57dd68.png#averageHue=%23fefefd&clientId=u84a0f0a5-5448-4&from=paste&height=140&id=u3bab5408&originHeight=192&originWidth=912&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=36426&status=done&style=none&taskId=u07fc118a-e510-469e-83b2-128f332756c&title=&width=663.2727272727273)<br />在约束布局中，每个组件至少需要一个水平方向和一个垂直方向的约束。<br />添加约束的方式有三种，一种是可以通过xml的code上添加对应的属性实现，<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714660993607-1f07c9b5-6fac-49bf-8e55-dee122037d95.png#averageHue=%23fefefd&clientId=u84a0f0a5-5448-4&from=paste&height=101&id=u4d8f6cef&originHeight=139&originWidth=707&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=21704&status=done&style=none&taskId=u19686dc4-0aac-4de7-ac85-b310ad6524c&title=&width=514.1818181818181)<br />也可以通过image处，点击空间的边框的点，建立与其他位置的约束。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661054919-246a2004-2f75-4551-83e0-33cbffc48590.png#averageHue=%233d798c&clientId=u84a0f0a5-5448-4&from=paste&height=231&id=ue1f8b4ad&originHeight=317&originWidth=337&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=8198&status=done&style=none&taskId=uff7f14b1-bdc4-4ecf-826d-4e8499da0d3&title=&width=245.0909090909091)<br />最后是根据组件的attribution栏目，进行建立。当点击每个黑点的时候可以选择建立约束，或者是删除约束<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661093205-95895ea7-b0b3-4ebf-a116-cd57f2407d98.png#averageHue=%23ebeff3&clientId=u84a0f0a5-5448-4&from=paste&height=235&id=ud68550bb&originHeight=323&originWidth=349&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=19114&status=done&style=none&taskId=u44cc9ec6-e371-44d4-bd56-3d6302f151b&title=&width=253.8181818181818)![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661146588-3c28cb3f-288c-41a2-8669-c1e93e22a0b7.png#averageHue=%23dde0e3&clientId=u84a0f0a5-5448-4&from=paste&height=204&id=uf7fb1f25&originHeight=281&originWidth=367&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=16743&status=done&style=none&taskId=uc9bc09bf-0606-4144-b861-1248340f093&title=&width=266.90909090909093)<br />然后，根据效果图，分别为每个组件构建如下约束。<br />![textview的约束](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661160615-82489ab5-9bec-4c55-a54f-162d5a7826e6.png#averageHue=%236192a2&clientId=u84a0f0a5-5448-4&from=paste&height=401&id=u56874718&originHeight=552&originWidth=442&originalType=binary&ratio=1.375&rotation=0&showTitle=true&size=19277&status=done&style=none&taskId=u77e495b0-048a-40f9-a804-2ac720719ed&title=textview%E7%9A%84%E7%BA%A6%E6%9D%9F&width=321.45454545454544 "textview的约束")![Toast_button的约束](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661217998-1f9a4130-e691-46ca-bc08-e8e90f8ad603.png#averageHue=%23447e91&clientId=u84a0f0a5-5448-4&from=paste&height=383&id=ua09cdcb4&originHeight=508&originWidth=440&originalType=binary&ratio=1.375&rotation=0&showTitle=true&size=19799&status=done&style=none&taskId=u268b4242-f778-4d9e-926b-f318b888e05&title=Toast_button%E7%9A%84%E7%BA%A6%E6%9D%9F&width=332 "Toast_button的约束")<br />![Count_button的约束](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661254711-f39b2596-6927-46d9-8f4f-c65cb8b0dc07.png#averageHue=%236198aa&clientId=u84a0f0a5-5448-4&from=paste&height=294&id=u6fecd899&originHeight=534&originWidth=573&originalType=binary&ratio=1.375&rotation=0&showTitle=true&size=27337&status=done&style=none&taskId=uddb4e689-2e24-48da-989a-497795b506b&title=Count_button%E7%9A%84%E7%BA%A6%E6%9D%9F&width=315 "Count_button的约束")![Random_button的约束](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661297244-5a0ab153-6ff0-4dc2-837e-b831ff71de7b.png#averageHue=%23437d90&clientId=u84a0f0a5-5448-4&from=paste&height=314&id=u927e7fa2&originHeight=493&originWidth=488&originalType=binary&ratio=1.375&rotation=0&showTitle=true&size=19357&status=done&style=none&taskId=u0abe09f8-79ac-47f0-a277-6b62cce71c1&title=Random_button%E7%9A%84%E7%BA%A6%E6%9D%9F&width=310.9091033935547 "Random_button的约束")

---

最后，整体的呈现效果如下：<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661358415-9016fcf6-e9d4-4b64-8c86-23130dcfe195.png#averageHue=%233ea2f3&clientId=u84a0f0a5-5448-4&from=paste&height=541&id=u00f8d17d&originHeight=744&originWidth=499&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=18591&status=done&style=none&taskId=uc3a90429-1217-4ac6-9f16-ab4e6ad9b91&title=&width=362.90909090909093)<br />下面的fragment_first.xml的完整代码：
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.core.widget.NestedScrollView xmlns:android="http://schemas.android.com/apk/res/android"
  xmlns:app="http://schemas.android.com/apk/res-auto"
  xmlns:tools="http://schemas.android.com/tools"
  android:layout_width="match_parent"
  android:layout_height="match_parent"
  tools:context=".FirstFragment"
  android:background="@color/screenBackground">

  <androidx.constraintlayout.widget.ConstraintLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="15dp">

    <Button
      android:id="@+id/random_button"
      android:layout_width="wrap_content"
      android:layout_height="wrap_content"

      android:layout_marginEnd="24dp"
      android:background="@color/buttonBackground"
      android:text="@string/next"
      app:layout_constraintBottom_toBottomOf="parent"
      app:layout_constraintEnd_toEndOf="parent"
      app:layout_constraintTop_toBottomOf="@+id/textview_first"
      app:layout_constraintVertical_bias="1.0" />

    <TextView
      android:id="@+id/textview_first"
      android:layout_width="239dp"
      android:layout_height="82dp"
      android:fontFamily="sans-serif-condensed"
      android:gravity="center"
      android:text="@string/hello_first_fragment"
      android:textColor="#ffffff"
      android:textSize="64sp"
      android:textStyle="bold"
      app:layout_constraintBottom_toBottomOf="parent"

      app:layout_constraintEnd_toEndOf="parent"
      app:layout_constraintStart_toStartOf="parent"
      app:layout_constraintTop_toTopOf="parent"
      app:layout_constraintVertical_bias="0.3" />

    <Button
      android:id="@+id/toast_button"
      android:layout_width="wrap_content"
      android:layout_height="wrap_content"
      android:layout_marginStart="24dp"
      android:layout_marginTop="252dp"
      android:background="@color/buttonBackground"
      android:text="@string/toast_button_test"
      app:layout_constraintBottom_toBottomOf="parent"
      app:layout_constraintStart_toStartOf="parent"
      app:layout_constraintTop_toBottomOf="@+id/textview_first"
      app:layout_constraintVertical_bias="1.0" />

    <Button
      android:id="@+id/count_button"
      android:layout_width="wrap_content"
      android:layout_height="wrap_content"
      android:layout_marginTop="252dp"
      android:text="@string/count_button"
      app:layout_constraintBottom_toBottomOf="parent"
      app:layout_constraintEnd_toStartOf="@+id/random_button"
      app:layout_constraintHorizontal_bias="0.606"
      app:layout_constraintStart_toEndOf="@+id/toast_button"
      app:layout_constraintTop_toBottomOf="@+id/textview_first"
      android:background="@color/buttonBackground" />
  </androidx.constraintlayout.widget.ConstraintLayout>
</androidx.core.widget.NestedScrollView>
```
## 2.3 second Fragment的外观设置
这个部分将对second Fragment的页面进行外观的设计。<br />首先是对second Fragment的背景进行更换。<br />在color中，添加如下的颜色以及名称，作为这个界面的背景色。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662003570-e99d5205-c0f4-441f-a49e-9ccf4ff08604.png#averageHue=%2366bba6&clientId=u84a0f0a5-5448-4&from=paste&height=40&id=ub4599cd0&originHeight=55&originWidth=755&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=12089&status=done&style=none&taskId=u7aec146c-a75f-47fe-a690-c5cb550325e&title=&width=549.0909090909091)<br />在fragment_second.xml的code处，将其背景颜色改为上述的颜色。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662074193-2b692de5-13b1-446c-98d8-42091dfc0466.png#averageHue=%23138230&clientId=u84a0f0a5-5448-4&from=paste&height=48&id=ue75c237d&originHeight=66&originWidth=738&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=12411&status=done&style=none&taskId=u0b41856e-d463-4608-9664-ef7a6336a42&title=&width=536.7272727272727)

---

然后，根据2.2的方法加入一个在fragment_second.xml的左边点击textview并拖动到页面，添加一个viewtext。<br />然后，回到code处。修改这个textview的id为textview_header。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661686936-67cef4ee-c126-484d-896e-b4d7de26f26f.png#averageHue=%23fefefc&clientId=u84a0f0a5-5448-4&from=paste&height=46&id=ub2a3af50&originHeight=63&originWidth=541&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=7474&status=done&style=none&taskId=u9b2646c2-d718-4cc8-91be-d7751f356ec&title=&width=393.45454545454544)<br />同样通过"extract string.."的方式绑定对应的文本内容。这里的文本内容设置为"Here is a random number between 0 and %d"<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661761698-06f8d1ad-9107-456b-a467-1b639f43c42f.png#averageHue=%2354ad7d&clientId=u84a0f0a5-5448-4&from=paste&height=49&id=u62d6ecf7&originHeight=67&originWidth=611&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=9599&status=done&style=none&taskId=ub4af8038-bfe5-4672-a1ef-390712972ef&title=&width=444.3636363636364)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661742333-a06dbcbe-f7a7-42a5-b282-3404253df7ca.png#averageHue=%233f943d&clientId=u84a0f0a5-5448-4&from=paste&height=63&id=u4abd3762&originHeight=86&originWidth=1271&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=25314&status=done&style=none&taskId=u101e5d88-f928-420a-b4b3-41e95f5c815&title=&width=924.3636363636364)<br />设置layout_width为272dp，layout_height为94dp。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661857208-2395dd56-2ffd-419f-b837-9cad365de7f7.png#averageHue=%2332903d&clientId=u84a0f0a5-5448-4&from=paste&height=61&id=u1ee834aa&originHeight=84&originWidth=462&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=13821&status=done&style=none&taskId=uc9c5e181-7d62-4a99-b933-49618af0f43&title=&width=336)<br />向colors.xml添加颜色colorPrimaryDark，并将TextView颜色设置为@color/colorPrimaryDar k，字体大小为24sp。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661927175-629c56b3-f74f-4331-bcb4-1e7d844de05e.png#averageHue=%231c8630&clientId=u84a0f0a5-5448-4&from=paste&height=51&id=u671c22c6&originHeight=70&originWidth=787&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=15553&status=done&style=none&taskId=u9c06433b-b064-4424-b31e-b92cddb885a&title=&width=572.3636363636364)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714661938994-48707be4-9d0d-4ca6-a088-93e477554193.png#averageHue=%2324862b&clientId=u84a0f0a5-5448-4&from=paste&height=63&id=u8786cf61&originHeight=86&originWidth=786&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=15500&status=done&style=none&taskId=u4cdb1de9-aa8e-46a5-9e7a-2ac3642295d&title=&width=571.6363636363636)

---

接着，将second fragment自带的textview的id更名为textview_random。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662206785-8ed62a3e-f206-4703-8070-f7322e12506a.png#averageHue=%2340a380&clientId=u84a0f0a5-5448-4&from=paste&height=39&id=u3a74b1d3&originHeight=54&originWidth=528&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=8414&status=done&style=none&taskId=u08caa888-8c12-4a90-a599-bc50a1d3cb2&title=&width=384)<br />设置TextView的字体颜色textColor属性为#ffffff，textSize为72sp，textStyle为bold。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662234489-25c0893f-cd2e-4e8d-818b-925acf7dd941.png#averageHue=%23fefefd&clientId=u84a0f0a5-5448-4&from=paste&height=92&id=uffdaac95&originHeight=126&originWidth=476&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=16983&status=done&style=none&taskId=u1066b521-eb3e-41f8-82fd-5e34a63adc5&title=&width=346.1818181818182)<br />设置TextView的显示文字为“R”。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662282518-5e5343b6-0cdc-47aa-b7a8-5389dfe48de4.png#averageHue=%23238930&clientId=u84a0f0a5-5448-4&from=paste&height=55&id=u04715513&originHeight=75&originWidth=624&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=14093&status=done&style=none&taskId=uc2411011-9b68-4082-8cbb-aed6d91e2cc&title=&width=453.8181818181818)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662296034-77693e08-ee7a-43bf-a61f-d1ef2a5669ca.png#averageHue=%23fcfcfa&clientId=u84a0f0a5-5448-4&from=paste&height=47&id=u65c30744&originHeight=65&originWidth=662&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=11907&status=done&style=none&taskId=u11f8c862-6369-4c96-be6a-6826f6ccb7c&title=&width=481.45454545454544)

---

最后，根据如下关系，处理这三个组件之间的约束。<br />![textview_random的约束](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662375379-d2bab954-605b-4ce4-8e6a-19188e4af41c.png#averageHue=%236394a4&clientId=u84a0f0a5-5448-4&from=paste&height=316&id=ue57b30e7&originHeight=434&originWidth=461&originalType=binary&ratio=1.375&rotation=0&showTitle=true&size=11640&status=done&style=none&taskId=u26dfe690-a445-4584-aefd-6ec53db9215&title=textview_random%E7%9A%84%E7%BA%A6%E6%9D%9F&width=335.27272727272725 "textview_random的约束")<br />![previous_button的约束](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662405815-d108b6d0-4075-42a9-b405-3a8cc553654a.png#averageHue=%2379a8b7&clientId=u84a0f0a5-5448-4&from=paste&height=204&id=uf2f18d7a&originHeight=280&originWidth=474&originalType=binary&ratio=1.375&rotation=0&showTitle=true&size=9885&status=done&style=none&taskId=uf8c5a44d-cb65-4ef9-8fea-bd57aa1e7c6&title=previous_button%E7%9A%84%E7%BA%A6%E6%9D%9F&width=344.72727272727275 "previous_button的约束")<br />![textview_header的约束](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662437869-cf3a3d29-addd-4456-a66a-0a2f2cbeb9ed.png#averageHue=%2394bcc9&clientId=u84a0f0a5-5448-4&from=paste&height=181&id=u30e15446&originHeight=249&originWidth=483&originalType=binary&ratio=1.375&rotation=0&showTitle=true&size=11580&status=done&style=none&taskId=u4606a26e-ea6a-4aeb-ba35-60aaf567ea2&title=textview_header%E7%9A%84%E7%BA%A6%E6%9D%9F&width=351.27272727272725 "textview_header的约束")<br />同时，textview_random的水平偏移量为0.<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662596059-62d3fa40-82f3-46dc-9cef-def47bbfa221.png#averageHue=%23dfecfa&clientId=u84a0f0a5-5448-4&from=paste&height=40&id=ue2410731&originHeight=55&originWidth=658&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=6890&status=done&style=none&taskId=u63a9f661-5877-466e-8a92-42802be2ef0&title=&width=478.54545454545456)<br />textview_header的垂直偏移量为0.141，水平偏移量为0.<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662656935-55ae80f1-fdb5-44e2-9cde-c059f71b3b56.png#averageHue=%23fefefd&clientId=u84a0f0a5-5448-4&from=paste&height=32&id=u7c5a0856&originHeight=44&originWidth=650&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=7518&status=done&style=none&taskId=u44a77c87-0109-482e-918d-fb412e47c0b&title=&width=472.72727272727275)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662669149-5cc9bdfd-a7ad-49ac-bb96-3123f60229ab.png#averageHue=%2367b6ce&clientId=u84a0f0a5-5448-4&from=paste&height=33&id=u234961c0&originHeight=46&originWidth=647&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=6719&status=done&style=none&taskId=u7ce535b6-1637-4276-a19e-86426f8d658&title=&width=470.54545454545456)

---

最后整体的second_fragment的效果如下。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714662489765-cdc24253-b2a0-4391-b816-e9d12c73a353.png#averageHue=%2342cbdd&clientId=u84a0f0a5-5448-4&from=paste&height=494&id=ud189e5e6&originHeight=679&originWidth=414&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=15746&status=done&style=none&taskId=u866c2813-2cf4-415b-8069-3ff86449ce8&title=&width=301.09090909090907)<br />下面的fragment_second.xml的完整代码：
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.core.widget.NestedScrollView xmlns:android="http://schemas.android.com/apk/res/android"
  xmlns:app="http://schemas.android.com/apk/res-auto"
  xmlns:tools="http://schemas.android.com/tools"
  android:layout_width="match_parent"
  android:layout_height="match_parent"
  tools:context=".SecondFragment"
  android:background="@color/screenBackground2">

  <androidx.constraintlayout.widget.ConstraintLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="16dp">

    <Button
      android:id="@+id/button_second"
      android:layout_width="wrap_content"
      android:layout_height="wrap_content"
      android:layout_marginBottom="150dp"
      android:text="@string/previous"
      app:layout_constraintBottom_toBottomOf="parent"
      app:layout_constraintEnd_toEndOf="parent"
      app:layout_constraintHorizontal_bias="0.498"
      app:layout_constraintStart_toStartOf="parent" />

    <TextView
      android:id="@+id/textview_random"
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:layout_marginBottom="228dp"
      android:gravity="center"
      android:text="@string/textview_random"
      android:textColor="#ffffff"
      android:textSize="72sp"
      android:textStyle="bold"
      app:layout_constraintBottom_toTopOf="@+id/button_second"
      app:layout_constraintEnd_toEndOf="parent"
      app:layout_constraintHorizontal_bias="0.0"
      app:layout_constraintStart_toStartOf="parent" />

    <TextView
      android:id="@+id/textview_header"
      android:layout_width="272dp"
      android:layout_height="94dp"
      android:layout_marginBottom="70dp"
      android:text="@string/random_heading"
      android:textColor="@color/colorPrimaryDark"
      android:textSize="24sp"
      app:layout_constraintBottom_toTopOf="@+id/textview_random"
      app:layout_constraintEnd_toEndOf="parent"
      app:layout_constraintHorizontal_bias="0.0"
      app:layout_constraintStart_toStartOf="parent"
      app:layout_constraintTop_toTopOf="parent"
      app:layout_constraintVertical_bias="0.171" />
  </androidx.constraintlayout.widget.ConstraintLayout>
</androidx.core.widget.NestedScrollView>
```
## 2.4 页面切换
在这个部分，我们将完成交互的代码，以及页面切换的部分。<br />打开FirstFragment.kt文件，有三个方法：onCreateView，onViewCreated和onDestroyView，在onViewCreated方法中使用绑定机制设置按钮的响应事件（创建应用程序时自带的按钮）。
```python
binding.randomButton.setOnClickListener {
    findNavController().navigate(R.id.action_FirstFragment_to_SecondFragment)
}
```
接下来，为TOAST按钮添加事件，使用findViewById()查找按钮id，代码如下。
```
view.findViewById<Button>(R.id.toast_button).setOnClickListener {
    // create a Toast with some text, to appear for a short time
    val myToast = Toast.makeText(context, "Hello Toast!", Toast.LENGTH_LONG)
    // show the Toast
    myToast.show()
}
```
	在FirstFragment.kt文件，为count_buttion按钮添加事件。
```python
view.findViewById<Button>(R.id.count_button).setOnClickListener {
    countMe(view)
}
```
countMe()为自定义方法，以View为参数，每次点击增加数字1，具体代码为：
```kotlin
private fun countMe(view: View){
    val showCountTextView = view.findViewById<TextView>(R.id.textview_first)
    val countString = showCountTextView.text.toString()

    var cnt = countString.toInt()
    cnt++

    showCountTextView.text = cnt.toString()
}
```

---

然后，检查两个页面的导航图。<br />打开nav_graph.xml文件（res>navigation>nav_graph.xml），形如：<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714663018877-9f8e8fd8-3e19-4f7d-b470-0a72a9cc0dd7.png#averageHue=%23a5daf1&clientId=u84a0f0a5-5448-4&from=paste&height=523&id=ufeb51932&originHeight=719&originWidth=909&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=30914&status=done&style=none&taskId=uaec207a3-d503-450e-b932-98cc60ea8cf&title=&width=661.0909090909091)<br />接着，创建导航动作的参数。<br />在导航视图，点击FirstFragment，查看其属性。点击Arguments处的+，创建一个名为myArg的Integer类型的参数。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714663483255-cca4ab1f-052a-4e39-b7f1-205c0f4b39db.png#averageHue=%23dcedf3&clientId=u84a0f0a5-5448-4&from=paste&height=309&id=uabd774ca&originHeight=425&originWidth=532&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=26579&status=done&style=none&taskId=ude3f7371-39e6-4513-bb04-2a38b1ee428&title=&width=386.90909090909093)<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714663493400-6c029f36-640d-4ae2-bb97-c5d69ef193e2.png#averageHue=%23f1f4f7&clientId=u84a0f0a5-5448-4&from=paste&height=321&id=ud476cbab&originHeight=442&originWidth=660&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=41868&status=done&style=none&taskId=u30a8ada0-aebe-4a36-a5a9-e2d5004a56b&title=&width=480)<br />同理，我们也对second fragment创建相同名称，相同的数据类型的参数。

---

接着，是安装SafeArgs插件，它可以帮助您在导航图中输入需要传递的数据信息，作用类似于Activity之间传递数据的Bundle。<br />因为是用的是Android Studio Iguana | 2023.2.1，因此在安装SafeArgs时有所不一样。<br />首先打开 Gradle Scripts > build.gradle (Project: MyKotlinApplication)中的最顶部添加如下代码：
```kotlin
buildscript {
    repositories {
        google()
    }
    dependencies {
        val nav_version = "2.7.7"
        classpath("androidx.navigation:navigation-safe-args-gradle-plugin:$nav_version")
    }
}
```
**添加，上述代码之后，执行sync now，否则后续的找包会找不到。**<br />结束之后，接着打开 Gradle Scripts > build.gradle (Module: app)，apply plugin开头的代码下添加一行；
```kotlin
id("androidx.navigation.safeargs")
```
最后，Android Studio开始同步依赖库，重新生成工程Build > Make Project。

---

接着，在first fragment添加代码，向second fragment发送数据。<br />初始应用中，点击FirstFragment的Next/Random按钮将跳转到第二个页面，但没有传递数据。在本步骤中将获取当前TextView中显示的数字并传输至SecondFragment。<br />打开FirstFragment.kt源代码文件；<br />找到onViewCreated()方法，该方法在onCreateView方法之后被调用，可以实现组件的初始化。找到Random按钮的响应代码，注释掉原先的事件处理代码；<br />实例化TextView，获取TextView中文本并转换为整数值；
```kotlin
val showCountTextView = view.findViewById<TextView>(R.id.textview_first)
    val currentCount = showCountTextView.text.toString().toInt()
```
将currentCount作为参数传递给actionFirstFragmentToSecondFragment()；
```kotlin
val action = FirstFragmentDirections.actionFirstFragmentToSecondFragment(currentCount)
```
添加导航事件代码。
```kotlin
findNavController().navigate(action)
```
如下是上面步骤的完整代码。
```kotlin
binding.randomButton.setOnClickListener {
    //findNavController().navigate(R.id.action_FirstFragment_to_SecondFragment)
    val showCountTextView = view.findViewById<TextView>(R.id.textview_first)
    val currentCount = showCountTextView.text.toString().toInt()
    val action = FirstFragmentDirections.actionFirstFragmentToSecondFragment(currentCount)

    findNavController().navigate(action)
}
```
运行代码，点击FirstFragment的Count按钮，然后点击Random按钮，可以看到second fragment在头部的TextView已经显示正确的数字，但是屏幕中间还未出现随机数显示。

---

最后，将更新SecondFragment.kt的代码，接受传递过来的整型参数并进行处理。<br />导入navArgs包。
```kotlin
import androidx.navigation.fragment.navArgs
```
onViewCreated()代码之前添加一行。
```kotlin
val args: SecondFragmentArgs by navArgs()
```
onViewCreated()中获取传递过来的参数列表，提取count数值，并在textview_header中显示。
```kotlin
val count = args.myArg
val countText = getString(R.string.random_heading, count)
view.findViewById<TextView>(R.id.textview_header).text = countText
```
根据count值生成随机数。
```kotlin
val random = java.util.Random()
var randomNumber = 0
if (count > 0) {
   randomNumber = random.nextInt(count + 1)
}
```
textview_random中显示count值。
```kotlin
view.findViewById<TextView>(R.id.textview_random).text = randomNumber.toString()
```
如下，是上述步骤的完整代码。
```kotlin
val args: SecondFragmentArgs by navArgs()
    override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
        super.onViewCreated(view, savedInstanceState)


        binding.buttonSecond.setOnClickListener {

        }
        view.findViewById<Button>(R.id.button_second).setOnClickListener {
            findNavController().navigate(R.id.action_SecondFragment_to_FirstFragment)

        }
        val count = args.myArg
        val countText = getString(R.string.random_heading, count)
        view.findViewById<TextView>(R.id.textview_header).text = countText
        val random = java.util.Random()
        var randomNumber = 0
        if (count > 0) {
            randomNumber = random.nextInt(count + 1)
        }
        view.findViewById<TextView>(R.id.textview_random).text = randomNumber.toString()
    }
```
# 3 实验结果
完成代码之后，选择2.1的虚拟设备，运行程序。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714703876617-ea80636d-8ee3-4a0b-ad0e-3b08e5a1bfaf.png#averageHue=%237cad93&clientId=u641e9078-6c2e-4&from=paste&height=84&id=u25fa91d8&originHeight=116&originWidth=765&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=20200&status=done&style=none&taskId=u9131f11d-67e2-40c3-ab5f-66b805697cb&title=&width=556.3636363636364)<br />然后开启设备。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714704320717-0a61b8f8-1431-481f-9bde-2417685b5186.png#averageHue=%23add5f6&clientId=u641e9078-6c2e-4&from=paste&height=665&id=ub13e1775&originHeight=915&originWidth=805&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=80631&status=done&style=none&taskId=ufbf87309-b651-41d6-b2a9-5bea00d6984&title=&width=585.4545454545455)<br />点击toast。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714704333877-6779628b-9fd5-4148-bcf2-f414be27b5a0.png#averageHue=%2360b1f2&clientId=u641e9078-6c2e-4&from=paste&height=604&id=uc8f29e37&originHeight=831&originWidth=482&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=65575&status=done&style=none&taskId=uc83c8c3a-cd5b-4fcd-a79c-263964fbb24&title=&width=350.54545454545456)<br />点击四下count。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714704360349-9ebb7968-2670-4e70-9e03-985e168473df.png#averageHue=%235eb0f2&clientId=u641e9078-6c2e-4&from=paste&height=616&id=u30375be8&originHeight=847&originWidth=476&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=63157&status=done&style=none&taskId=ub88825bd-6abb-4dac-83d1-b7d31af6795&title=&width=346.1818181818182)<br />点击random，跳转到second fragment。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714704373270-bd48ce0d-8468-4b00-ad57-4fa6be54b7a2.png#averageHue=%2350cedf&clientId=u641e9078-6c2e-4&from=paste&height=606&id=u54bd9108&originHeight=833&originWidth=447&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=69105&status=done&style=none&taskId=u001259cf-c257-4954-8b42-71f504fa00d&title=&width=325.09090909090907)<br />点击previous，回到first fragment。<br />![image.png](https://cdn.nlark.com/yuque/0/2024/png/38674938/1714704423455-96e742f9-d0b1-45fe-8156-63a0b86f112c.png#averageHue=%233ea2f1&clientId=u641e9078-6c2e-4&from=paste&height=589&id=u39307ce5&originHeight=810&originWidth=430&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=57574&status=done&style=none&taskId=ub841edd5-c3af-49a3-9abc-1955930b43d&title=&width=312.72727272727275)<br />实现效果与要求一致。
