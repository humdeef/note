# note
1.登入 简单的用户名和密码登录  用户名和秘密+时间戳 生成token，以token为key,User为value放到redis里面，用string类型的就可以了。如果没有找到就去数据库里面查找，返回token无效，如果当用户再次登入的时候，输入的正确的用户名和密码，就生成一个新的token放到redis里面。有效期暂定两个小时。
2.聊天 建表  一天为分区。  借助融云
3.银行卡信息对接  


付款页面：
注：隐藏本次活动，意味着别人这次在酒吧伙伴中搜索不到
你，也不能发起拼桌活动？酒吧伙伴？

购物车：
转发？

后台如何给前台推送数据？
方案：融云
聊天系统？
方案：融云

待使用的订单？

app如何附近的人？
方案：用户打开app，上传经纬度，通过经纬度+-2，这样就可以大致获取附近的人。

支付宝支付
用户打开app，然后ios或Android调用支付宝client，支付成功，（同步通知不管）会有一个异步通知给到后台服务器，后台服务器在这个接口检查是否支付成功的状态，更改订单状态，最后out.print("success")输出"success"，支付宝服务器确认通知成功！

