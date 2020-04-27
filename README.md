# BetterTouchTool-在TouchBar上背单词

## 一、效果

### 1. 背单词

#### 1）第1套

**学习模式——Learning Mode**

![触控栏快照2020-04-2409.45.13](a1.png)

![触控栏快照2020-04-2411.03.01](a2.png)

* **特色**
  * *统计每个单词的不认识次数，并生成以不认识的单词组成的新文档*
  * *认识的单词不再显示*
  * *可调文字大小、字体颜色、背景颜色*

#### 2）第2套

**复习模式——Quick Look Mode**

* 特色
  * *每隔2秒，显示1个单词*
  * *每隔5秒，显示n个单词（n值可自定义，默认n为3）*
  * *可调文字大小、字体颜色、背景颜色*

![背单词复习模式1](b1.png)

![背单词复习模式2](b2.png)

![背单词复习模式3](b3.png)

![背单词复习模式4](b4.png)



## 二、必备工具

* Bettertouchtool
* 我的Bettertouchtool配置-[cyubuchen_learning](cyubuchen_learning.json)
* txt文档—你想看的单词表



## 三、准备工作

### 1.Bettertouchtool的安装、导入配置

[BetterTouchTool](https://folivora.ai/)

[cyubuchen_learning](cyubuchen_learning.json)

### 2.配置说明——背单词

#### 1）必须设置单词表文档所在路径

##### 需要添加路径的配置名

* Touch Bar
  * Learning Mode — 1 word each time
    * 修改文档路径方法
      * 选中Learning Mode — 1 word each time => 点右侧的compile => 修改第2行filePath的文档路径
  * Quick Look Mode
    * 1 word each time
    * 3 words each time
    * 修改文档路径方法同上
* Named & Other Triggers
  * Named Trigger: Word recognised
    * 选中Named Trigger: Word recognised => Run Apple Script =>点compile => 修改第2行filePath的文档路径
  * Named Trigger: Word forgotten
    * 同上

##### Bettertouchtool的触摸反馈（可选）

* BetterTouchTool Settings => Touch Bar => Advanced => Default Haptic Feedback... => On Touch: Very Light Fdeedback

#### 2） 单词文档格式

* 推荐使用UTF-8编码的txt文档
* 每行内容对应一个单词、释义或例句
* 可参考该文档的格式：[GRE 8000 Words](https://github.com/mahavivo/english-wordlists/blob/master/GRE_8000_Words.txt)
  * 常用英语词汇：[mahavivo / english-wordlists](https://github.com/mahavivo/english-wordlists)

#### 3）自定义文字大小、字体颜色、背景颜色

* font_size：字体大小
  * 默认15

* font_color：字体颜色
  * 默认白色：255,255,255,255
* background_color：背景颜色
  * 默认蓝色：0,103,255,255

#### 4）补充

* 文档编码
  * 推荐使用编码为UTF-8的txt文档

* 文档编码转换方法

  * 查看文档编码是否为UTF-8
    * 终端内输入`file your_text_file_path`
    
* 转换文档编码至UTF-8：
    * 终端内输入`iconv -c -f GBK -t UTF-8 /Users/your_username/Desktop/your_text_file_name.txt >> /Users/your_username/Desktop/your_text_file_name-UTF8.txt `

