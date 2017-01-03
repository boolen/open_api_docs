## 查询订单的API

**调用请求**
```
GET /v1/deals?access_token={access_token}
```
**参数说明**

- {access_token}用从“获取身份权限”节拿到的access_token替换
- 除了access_token参数外，该API还支持以下参数来缩小查询结果集:
	- customerId 查询指定客户的订单
	- rows 每页的记录数	- page 第几页	- sidx 排序的字段	- sord 排序的方式, asc是升序，desc是降序

**订单模型**

|参数名|数据类型|说明|
|:---|:---|:---|  
|id|number|订单id|
|type|string|订单类型，属于自定义类型，如双11订单| 
|dateOrder|datetime string|订单日期|
|amountTotal|number|订单金额|
|amountPaid|number|订单支付金额|
|amountTax|number|订单税额|
|amountReturn|number|订单退款金额|
|amountDiscount|number|订单折扣金额|
|currency|string|币种|
|customerId|number|客户id|
|customerName|string|客户姓名|
|paymentTerm|string|支付方式|
|paymentNo|string|支付序列号|
|contactName|string|联系人|
|contactTel|string|联系人电话|
|state|string|支付状态
|invoiceAddress|string|发票地址|
|shippingAddress|string|配送地址|
|shippingMethod|string|配送方式|
|externalId|string|外部系统订单编号|
|externalInvoiceId|string|外部系统发票id|
|externalPickingId|string|外部系统拣货id|
|paymentStatus|string|付款状态|
|deliveryStatus|string|发货状态|
|lines|JSON object array|订单详情|

**订单行模型**

|参数名|数据类型|说明|
|:---|:---|:---|  
|priceUnit|number|单位价格|
|qty|number|货品数量|
|discount|number|货品折扣|
|externalProductId|string|外部系统货品id| 
|productName|string|productName|
