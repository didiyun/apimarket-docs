##一. 请求访问：
<br/></br>
**问. 进行服务调用之前需要做哪些操作和准备？**

答：请按以下流程进行操作：（如有问题，可随时咨询滴滴云线上客服专员获取协助）

（1）注册滴滴云账号，注册地址：https://app.didiyun.com/#/auth/signup?channel=0&return_to=https%3A%2F%2Fwww.didiyun.com%2F

（2）进行实名认证，实名认证地址：https://app.didiyun.com/#/account/personal/info/fillin?type=ENT_V1

（3）获得白名单认证，请联络滴滴云线上客户专员。

（4）进行接口测试之前请参考下列接口文档。


<br/></br>
**问.  认证完成后如何进行接口测试和调用？**

答：具体接口请参考以下接口文档： https://docs.didiyun.com/static/apimarket-docs/services/AI/%E6%9C%BA%E5%99%A8%E7%BF%BB%E8%AF%91/%E6%9C%BA%E5%99%A8%E7%BF%BB%E8%AF%91.html




<br/></br>
**问. 如何鉴权？**

答：测试使用的鉴权方式有两种，请参考滴滴云相关说明文档： https://docs.didiyun.com/static/docs-content/products/%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8/%E9%89%B4%E6%9D%83%E6%96%B9%E5%BC%8F.html ，

使用Appcode鉴权请参考：https://app.didiyun.com/#/ 所有产品-》云市场-》API市场 进入后预定所需的服务，预定成功后可以在“我的服务”中看到每个服务的AppCode，在请求headers里添加AppCode+空格+AppCode值，即可进行访问。


<br/></br>
**问. 使用postman等工具进行测试时提示“参数错误”，是什么原因？**

答：对于自然语言处理基础技术接口，header必须填写Content-Type: application/json




<br/></br>
<br/></br>
<br/></br>

##二. 私有化部署及定制需求：
<br/></br>
**问. 如需对其他类型文本进行识别如何合作？(比如特定场景、自定义字典等)**

答：如有新需求，请联系滴滴云线上客服或与 chentanfang@didiglobal.com 联络，自然语言处理算法定制需提供必要的标注数据集，同时涉及必要的定制周期和定制费用。


<br/></br>
**问. 是否支持私有化部署相关算法服务？私有化部署如何收费？**

答：支持私有化部署并已有相应成功案例。私有化部署的收费采取一单一议线下沟通方式，详情请与 chentanfang@didiglobal.com 联络。


