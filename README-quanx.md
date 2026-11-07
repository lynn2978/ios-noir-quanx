# iOS-NOIR Privacy Shield for Quantumult X（圈X）

基于 Arnold @arnoldchow117 的 iOS-NOIR 取证报告，把它的分流规则转成圈X能用的格式。

来源：https://github.com/arnold117/iOS-NOIR

## 文件

| 文件 | 说明 |
|---|---|
| `ios-noir-shield-quanx.list` | 圈X分流规则（75 条），从原 `ios_noir_shield.conf` 与 `ios_noir_shield.module` 转换而来（两份原文件内容相同） |

## 拦截内容

- 三大运营商免密取号网关：cmpassport.com、wostore.cn、id6.me 等（防绕过 Wi-Fi 偷传手机号）
- 数字联盟跨 App 设备指纹：shuzilm.cn
- JSPatch 热更新后门：jspatch.com
- 行为生物探针：online-metrix.net（ThreatMetrix）
- 秒针 / 国双 / AdMaster 等广告监测
- 字节穿山甲、腾讯广点通、阿里友盟、美团 / 拼多多 / 小红书 / B 站遥测、极光 / 个推等

不影响微信聊天与日常扫码支付。

## 在圈X里使用

1. 打开圈X → 设置 → 分流 → 引用（分流）→ 右上角 + 添加
2. 粘贴本文件的 Raw 链接：`https://raw.githubusercontent.com/lynn2978/ios-noir-quanx/main/ios-noir-shield-quanx.list`
3. 保存后开启即可

## 转换说明

原规则是 Surge/Clash 格式：`DOMAIN-SUFFIX,xxx,REJECT`
圈X格式：`host-suffix, xxx, reject`

## 注意

如果某个 App 必须用本机号码一键登录时卡住，可临时在圈X里停用本规则。
