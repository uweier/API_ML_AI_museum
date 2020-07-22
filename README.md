<div align="center">
  <h1>智能博物馆APP</h1>
</div>

### Product Requirements
|Target release|2020-1|
|---|---|
|Epic|智能博物馆APP|
|Document status|已完成|
|Document owner、Designer、Developer、QA|黄煜惠|

## PRD 价值主张设计
### 背景
博物馆的使用价值是为了促进社会教育、科学研究等，可是参观博物馆有不同的人群，有的人喜静，有的人喜动。多动症儿童参观博物馆可能会打扰到其他参观者，而行动不便的人士参观博物馆时又不那么方便。这对博物馆的管理者来说是一个急需解决的问题，所以，针对以上两类人群，需要推出一款能够在他们参观时为他们带来便利的博物馆APP。

### 目标
提供博物馆参观者一个好的参观体验。

## 目标用户
博物馆游客

### 加值宣言
基于博物馆的特性与博物馆游客需求的差异，现使用百度的人流量统计API、语音合成API、相同图片搜索API对博物馆APP进行加值。

（主要）
- 人流量统计API基于深度学习的人体识别方案，可以统计图像中的人体个数和流动趋势，以头肩为主要识别目标统计人数，无需正脸、全身照，适合博物馆的人流量监控。通过人流量统计，将数据传递到APP上，部分喜静的参观者、身障者即可了解博物馆各展馆的人流量情况，以此避开人多拥挤的展馆，得到更好的参观体验。

（次要）
- 相同图片搜索API会在博物馆图库中找到与检索图相同的图片。参观者可以使用博物馆APP对文物进行拍照，得到返回的信息就是该文物的相关信息、典故。
- 在线语音合成API基于业界领先的深度神经网络技术，提供高度拟人、流畅自然的语音合成服务，可在手机APP进行语音播报，将文字合成为声音。智能博物馆APP将利用在线语音合成API实现语音导览功能，参观者不再需要借博物馆里的语音导览设备的同时，还能个性化切换“播报人”，自行调整语速等等。
- 相同图片搜索API和在线语音合成API相互结合，形成一个主要的功能，即：拍照-搜索相同图片-返回文物信息-在线语音播报内容。

### 核心价值
实现具有博物馆人流量监控、语音讲解和拍照识别文物功能的APP。

### 核心价值与用户痛点
痛点一：身障者想避开人多的展馆，但是无法知道每个展馆的当前人数，每一次只能随机选取。若不幸到达了人多的展馆，只能小心翼翼地参观。
- 人流量统计API功能将会解决这个用户痛点，用户只需打开智能博物馆APP，就能知道每个展馆的人数，从而避开多人的地方。

痛点二：参观者需要语音导览，但是必须去借博物馆的设备，不太方便的同时，共用耳机也不卫生。
- 智能博物馆APP加入了语音合成功能后，参观者只需使用自己的手机，便能解决以上的需求问题。

痛点三：在展馆人多的时候，部分参观者只能匆匆看两眼文物就离开，来不及看文物介绍。
- 参观者可通过智能博物馆APP，拍下想了解的文物，然后再慢慢浏览APP上的文物介绍。

### 人工智能概率性与用户痛点
人工智能的准确率并不是百分百的，所以API可能出现以下的问题：

- 人流量统计API：因博物馆展馆内光线昏暗，无法准确识别人数。
- 在线语音合成API：若用户手机刚好处于信号不好的时候，语音播报会产生卡顿的情况，影响参观体验。
- 相同图片搜索API：因光线问题，造成图片识别有误的情况。

### 需求列表与人工智能API加值

||优先级|需求|API的使用|
|---|---|---|---|
|1|高|参观者需要了解当前展馆人流量|[人流量统计API](https://ai.baidu.com/tech/body/num)|
|2|中|参观者需要方便的语音导览设备|[在线语音合成API](https://ai.baidu.com/tech/speech/tts)|
|3|低|参观者想对某一件文物有更多的了解|[相同图片搜索API](https://ai.baidu.com/tech/imagesearch/same)|

## 原型
### 信息设计
- 人流量统计功能：使用了人流量统计API，方便参观者提前了解每个展馆的人流量，避开参观高峰。
- 语音导览功能：使用了语音合成API，方便参观者参观。
- 拍照识别馆内文物：使用了相同图片搜索，能够快速地将馆内文物识别，并提供更多关于该文物的介绍，同时介绍可选择通过语音播报的方式。

产品架构图：

![产品架构图](https://github.com/uweier/API_ML_AI_museum/blob/master/API_museum_image/jiagou.png)

产品主要功能使用流程图：

![产品主要功能使用流程图](https://github.com/uweier/API_ML_AI_museum/blob/master/API_museum_image/liucheng.png)

### 交互及界面设计
[**查看交互**](https://nfunm034.gitee.io/api_museum)

人流量统计：

![人流量统计](https://github.com/uweier/API_ML_AI_museum/blob/master/API_museum_image/renliuliang.png)

语音导览：

![语音导览](https://github.com/uweier/API_ML_AI_museum/blob/master/API_museum_image/yuyindaolan.png)

相同图片搜索：

![相同图片搜索](https://github.com/uweier/API_ML_AI_museum/blob/master/API_museum_image/paizhao.png)

![文物介绍](https://github.com/uweier/API_ML_AI_museum/blob/master/API_museum_image/jieshao.png)

### 原型文档
[智能博物馆APP.rp下载](https://github.com/uweier/API_ML_AI_museum/blob/master/%E6%99%BA%E8%83%BD%E5%8D%9A%E7%89%A9%E9%A6%86APP.rp)

[智能博物馆APP文件](https://github.com/uweier/API_ML_AI_museum/tree/master/%E6%99%BA%E8%83%BD%E5%8D%9A%E7%89%A9%E9%A6%86APP)

### 口头操作说明
**一句话版本**

通过人流量统计、语音导览、拍照识别的方式，更好地为参观者介绍博物馆文物，宣扬博物馆文化。

**一分钟版本**

这款智能博物馆APP有三大亮点：首先是，通过使用人流量统计API，为参观者展现各展馆内人流量情况，方便参观者提前得知馆内人数，合理安排参观时间，错峰参观；然后是，通过使用语音合成API，让参观者可以在自己手机上就能随意切换不同展馆的语音导览，无需借博物馆的导览设备；最后，通过使用相同图片搜索API，让参观者可以用手机拍下博物馆内文物，APP智能识别后，输出该文物的相关介绍，并能够通过语音介绍该文物。这三大功能主要是为了喜欢安静、行动不便的参观者而设计的，当然，其余人群也很适合使用。无论是喜欢安静的人群，还是多动症小孩，当他们都戴上耳机听取语音播报时，馆内环境自然就变得安静。
