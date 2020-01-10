# Museum的PRD文档（百度API&高德api）

|所有者|杨玉杏|
|---|---|


## 一、产品概述
为方便视障人群参观博物馆，领会更多关于博物馆内部的展区信息，同时方便陪同人员和志愿者所推出的一款智能产品。结合图片识别、文字识别、语音识别、语音合成等技术支持打造一款多用的关于帮助视障人群参观博物馆的智能产品，尽力可能满足视障参观者的困难需求。

## 二、加值宣言
本产品至于通过运用相关的人工智能加值，使视障人事在在博物馆达到便捷的体验效果。**图片识别api**，拍照文物识别文物，得到相应的知识内容；**文字识别api**，用户拍摄文字内容，输出得到的文字内容。**语音合成api**，结合图片识别和颜文字识别得到的内容，调用语音合成api，将文字合成语音，方便视障者详细了解文物背景信息。**语音识别**，方便视障者对产品的操作，拜托打字和手写，需要视力的程序操作。**高德地图室内定位**，多方位定位确定位置，方便定制导览路线

## 三、核心价值
本产品最小可行做到结合图片识别、文字识别和语音合成，做到让视障者能在博物馆内了解到文物的信息，最大体验博物馆的参观。

## 四、核心价值与用户痛点
* **目标用户：来博物馆参观的视力障碍人群和陪同人员或帮忙的志愿者（视障人群可表示视力或视觉有一定障碍的没有办法科学矫正的人，不一定泛指盲人）
* 痛点
1. 视障者想了解文物信息，无法看清标注文字
2. 陪同人员或帮助的志愿者，无法详细或无过多精力去详细解释文物信息时
3. 视障操作产品不便
4. 视障者无法了解博物馆内部各处方位时


## 五、人工智能概率性与用户痛点
* 图片识别api：精准识别超过十万种物体和场景，包含多项高精度的识图能力并提供相应的API服务，充分满足各类个人开发者和企业用户的业务需求
* 文字识别api：基于业界领先的深度学习技术，提供多场景、多语种、高精度的整图文字检测和识别服务，多项ICDAR指标居世界第一
* 语音合成api：基于业界领先的深度神经网络技术，提供高度拟人、流畅自然的语音合成服务，让您的应用、设备开口说话，更具个性
* 语音识别api：存在进场中文普通话识别准确率达98%，同时支持普通话和略带口音的中文识别、个别方言粤语四川话识别和英文识别。
* 高德室内定位SDK：通过基于WIFI、蓝牙以及PDR的室内定位技术，可实现平滑的1-8米的定位效果和精度


语音合成的错误时基于图片识别与文字识别的正确率，能保证图片识别与语音识别的正确，就能保证语音合成的正确。图片识别和语音识别可能会出现的错误是在用户拍照时，照片不够清晰或过于模糊，另外是图片识别，识别的物品与另一物品极其相似而导致的错误。语音识别，只要说话相对清楚音量够大，句子不长问题不大，但反之就会有问题。

## 六、需求列表与人工智能API加值

|场景描述|优先级|api运用|
|---|---|---|
|视障者来到博物馆参观时，没有办法清楚了解文物信息（如无法看清楚博物管标注的文字信息），本人（或他人）可使用产品拍照识别文物或注解文字了解信息，此后视障者可带耳机听取文字转化语音的内容来了解信息|重要|图片识别api、文字识别api、语音合成api|
|视障者可通过语音操作产品|次要|语音识别api|
|视障者不知方位，找不到路线|次要|高德室内SDK|
## 七、原型
### 交互及界面设计
1.首页
- 首页设置两个大控件，方便视障者操作，不因控件小而达不到相应的交互效果。

[首页](https://github.com/YangYuxing12345678900/museum/blob/master/首页.PNG)

2.识别功能(核心)
- 可以点击相机图标的控件，就可对相应信息拍照识别。拍照，的到照片调用【图片识别api】或【文字识别api】实现识别功能，通过识别到的内容，调用【语音合成api】转音频，方便视障者了解内容信息。另外，通过语音输入，也可以指挥做到相应的功能

[识别](https://github.com/YangYuxing12345678900/museum/blob/master/识别.PNG)

### 信息设计

[信息架构图](https://github.com/YangYuxing12345678900/museum/blob/master/信息架构.PNG)

### 原型文档

- [原型文档元件](https://github.com/YangYuxing12345678900/museum/blob/master/原型.rp)--下载

### 口头操作说明
各位好，今天要介绍的是一款关于帮助视障人士游览博物馆的智能产品。进入首页，有两个很大的控件，属于本产品的主要功能。大控件，方便视障者操作，不因控件小而达不到相应的交互效果。可以点击相机图标的控件，就可对相应信息拍照识别。拍照，的到照片调用【图片识别api】或【文字识别api】实现识别功能，通过识别到的内容，调用【语音合成api】转音频，方便视障者了解内容信息。另外，点击语音输入，调用【语音识别api】了解用户下达指令，并通过指令内容，到达下一步操作。同时语音课发出导览指令，调用【室内定位SDK】对用户进行定位，并根据用户指令定制导览路线。以上便是此产品的操作简况，欢迎各位下载并使用此产品，谢谢！
## 八、API测试
### API1.使用水平
1. 百度API的token的获取
```Python
#第一步先是来请求token
# access_token 的有效期为 30 天，切记需要每 30 天进行定期更换，或者每次请求都拉取新 token

# encoding:utf-8
import requests 

# client_id 为官网获取的AK=API Key， client_secret 为官网获取的SK=Secret Key
host = 'https://aip.baidubce.com/oauth/2.0/token?grant_type=client_credentials&client_id=【官网获取的AK】&client_secret=【官网获取的SK】'  # Key 不要用双引号括起来只是部分参数而已
response = requests.get(host)
if response:
    print(response.json())
```
- 请求
  
  ![token请求代码图片](https://github.com/YangYuxing12345678900/API_ML_AI/blob/master/img/token请求.PNG)
- 返回
  ```
  {'refresh_token': '25.9df19889433fc5001cefb8446d531173.315360000.1893261598.282335-18156003', 'expires_in': 2592000, 'session_key': '9mzdDc636/G2MenMoAEPpCB2U+1QBRaRxlevU0dE5+ihGn59l1Bila0O7kHttDT961Q2Vb8SRpgZoKMHM8xoXto9Yw2DEg==', 'access_token': '24.68b90052b6cf2ba4ae6e6e141b26f43b.2592000.1580493598.282335-18156003', 'scope': 'audio_voice_assistant_get brain_enhanced_asr audio_tts_post public brain_all_scope brain_ocr_handwriting picchain_test_picchain_api_scope wise_adapt lebo_resource_base lightservice_public hetu_basic lightcms_map_poi kaidian_kaidian ApsMisTest_Test权限 vis-classify_flower lpq_开放 cop_helloScope ApsMis_fangdi_permission smartapp_snsapi_base iop_autocar oauth_tp_app smartapp_smart_game_openapi oauth_sessionkey smartapp_swanid_verify smartapp_opensource_openapi smartapp_opensource_recapi fake_face_detect_开放Scope vis-ocr_虚拟人物助理 idl-video_虚拟人物助理', 'session_secret': 'd4c94b69fc180262ffe137a01b1ec293'}
  ```
2. 百度文字识别api测试
- 代码
```Python
import requests,json,base64
url = "https://aip.baidubce.com/rest/2.0/ocr/v1/general_basic"
file = open("en.png","rb").read()
png = base64.b64encode(file)
params = {"image":png}#image和url各选一个
token = '24.48afc02361999d06bfdc2b067dc5a560.2592000.1580545631.282335-18160921'
url = url + "?access_token=" + token
headers = {'content-type': 'application/x-www-form-urlencoded'}
response = requests.post(url, data=params, headers=headers)
if response:
    print (response.json())
```
- 返回
```
{'log_id': 8411515331957384194, 'words_result_num': 11, 'words_result': [{'words': 'ACKNOWLEDGEMENTS'}, {'words': 'We would like to thank all the designers and'}, {'words': 'contributors who have been involved in the'}, {'words': 'production of this book; their contributions'}, {'words': 'have been indispensable to its creation. We'}, {'words': 'would also like to express our gratitude to all'}, {'words': 'the producers for their invaluable opinions'}, {'words': 'and assistance throughout this project And to'}, {'words': 'the many others whose names are not credited'}, {'words': 'but have made specific input in this book, we'}, {'words': 'thank you for your continuous support'}]}
```
- 测试详情

|事项|错误码|报错原因|修改调整|备注|
|---|---|---|---|---|
|图片内文字识别（“en.png”）|-|-|-|无报错正常返回结果|

3. 语音识别api测试
- 代码
```Python
import requests,json,uuid,base64
token = '24.68b90052b6cf2ba4ae6e6e141b26f43b.2592000.1580493598.282335-18156003'#token请自行申请
file = open("fa.wav", "rb").read()#音频文件
url = "http://vop.baidu.com/server_api"
mac_address = uuid.UUID(int=uuid.getnode()).hex[-12:]
params = {"format": "wav",
    "lan": "zh",
    "token": token,
    "len": len(file),
    "rate": 16000,
    "speech": base64.b64encode(file).decode("utf-8"),
    "cuid": mac_address,
    "channel": 1}
headers = {"Content-Type": "application/json"}
response = requests.post(url, params=json.dumps(params), headers=headers)
if response:
    print (response.json())
```
- 返回
```
{"corpus_no":"6777113310890319637","err_msg":"success.","err_no":0,"result":["我不知道。"],"sn":"561065703321577919653"}
```
- 测试详情

|事项|错误码|报错原因|修改调整|备注|
|---|---|---|---|---|
|第一次测试|3316|使用音频为m4a格式，错误使用wav格式参数数填写方式|调整参数|-|
|第二次测试|3302|鉴权失败，请求requests_url输入错误，m4a格式音频的语音识别只有语音识别极速版可实现|修改requests_url|-|
|第三次测试（尝试多种音频格式，将m4a转mav）|3310|音频文件过大|修剪音频长度|-|







