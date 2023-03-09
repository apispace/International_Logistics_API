# APISpace 介绍
**本 API 服务由 [APISpace（apispace.com）](https://www.apispace.com/?utm_source=github&utm_term=guojiwuliu) 提供。**

APISpace 是 Eolink 旗下专业的 API 开放与交易平台，为广大企业以及个人开发者提供多维度、全方位的API接口，覆盖短信验证、天气查询、快递物流、OCR文字识别等海量 API 服务，帮助用户快速获取数据，降低获取数据的成本和难度，提升开发效率。

APISpace 提供15种开发语言的代码示例，分别是：
- Java(OK HTTP)
- HTTP
- cURL
- 微信小程序
- PHP(pecl_http)、PHP(cURL)
- Python(http.client)、Python(Requests)
- JavaScript(Jquery AJAX)、JavaScript(XHR)
- NodeJS(Native)、NodeJS(Request)
- Ruby(Net:Http)
- Shell(Httpie)、Shell(cUrl)

# 跨境国际快递物流查询
支持900+物流商，提供实时查询和单号订阅API接口。稳定高效，为跨境电商平台、独立站、软件服务商提供优质服务。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/internationallogistics/introduction](https://www.apispace.com/eolink/api/internationallogistics/introduction?utm_source=github&utm_term=guojiwuliu) 申请API服务**

本文档末尾提供了 Python(Requests) 的调用代码示例，可以前往文档末尾查看。

更多代码示例：[https://www.apispace.com/eolink/api/internationallogistics/guidence/](https://www.apispace.com/eolink/api/internationallogistics/guidence/?utm_source=github&utm_term=guojiwuliu)

**该产品拥有以下APIs：**
1. 国际物流订阅
2. 国际物流查询

### 功能亮点

1.  跨境国际快递物流查询服务，支持900+国际物流商。
1.  支持物流订阅服务，订阅后如有包裹状态更新会自动推送。
1.  接入跨境电商、独立站、软件服务商的系统，有效减少客服工作量，提升客户满意度。

### 使用须知

第一步：先调用 **订阅** API；

第二步：再调用 **查询** API。

### 应用场景

#### 1. 跨境电商平台

跨境电商平台需要将卖家的商品发往不同国家的买家，可以通过跨境快递物流进行商品的快速配送，确保买家收到商品的时间和质量。

#### 2. B2B贸易

企业需要将自己的产品运往海外市场进行销售，可以选择跨境快递物流公司进行物流配送，提高运输速度和效率，降低运输成本，促进企业的海外销售。

#### 3. 跨境仓储配送

仓库需要将货物快速配送至海外客户，可以通过跨境快递物流进行仓储配送服务，提供客户定制化的仓储物流解决方案，实现客户对物流的全流程管控。

#### 4. 国际医疗物流

医疗机构需要将医疗设备和药品配送至海外客户，可以通过跨境快递物流公司进行医疗物流服务，确保医疗物品的安全和准时配送，满足客户的需求。

### 相关附件

-   [国际快递公司编码表](https://easy-open-link.feishu.cn/wiki/wikcnBNtlAoPpvw97v8Bk0Xyo5c)

### 服务保障
![image](https://user-images.githubusercontent.com/36323798/223955159-e7592b3a-3d55-439d-86ac-e7d43cf45f09.png)

### Python(Requests) 调用代码示例
这里以 国际物流订阅API 为例
```
import requests

url = "https://eolink.o.apispace.com/internationallogistics/subscribe"

payload = {"cpCode":"","mailNo":""}

headers = {
    "X-APISpace-Token":"",
    "Authorization-Type":"apikey",
    "Content-Type":""
}

response=requests.request("POST", url, data=json.dumps(payload), headers=headers)

print(response.text)

```
