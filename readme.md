#Bank Card Info

项目根据[zhuzhichao](https://github.com/zhuzhichao/bank-card-info)进行修改补充用于项目


根据银行卡号获取银行信息（银行名称, 信用卡/借记卡, 银行LOGO 等）, 供任何 PHP 框架或者原生代码使用.


```
BankCard::info('6225700000000000');

// 将得到
array (size=6)
  'validated'    => true			// 是否验证成功
  'bank'         => 'CEB',			// 银行标识
  'bankName'     => '中国光大银行' ,	// 银行名称
  'bankImg'      => 'https://apimg.alipay.com/combo.png?d=cashier&t=CEB',  // 银行LOGO
  'cardType'     => 'CC',		// 卡类型
  'cardTypeName' => '信用卡',	// 卡类型名称
```

##特点

1. 不配置和使用数据库，妈妈再也不用担心配置问题了
2. 使用简单，功能专（dān）注（yī）
3. 使用[composer](https://getcomposer.org/)进行安装管理，国际标准，方便快捷，即安即用，随时更新数据库

##Install

`composer require "zhuzhichao/bank-card-info"`。

##Usage


1.安装该插件

2.加载插件

3.然后开始在你的项目里面使用了 `BankCard::info('6225700000000000')` 获取银行卡信息.
```
// 返回结果
array (size=6)
  'validated'    => true
  'bank'         => 'CEB',
  'bankName'     => '中国光大银行' ,
  'bankImg'      => 'https://apimg.alipay.com/combo.png?d=cashier&t=CEB',
  'cardType'     => 'CC',
  'cardTypeName' => '信用卡',
```

4.获取银行列表信息 `BankCard::getBankList()` , 如下
```
array (size=165)
  'SRCB'   =>  '深圳农村商业银行',
  'BGB'    =>  '广西北部湾银行',
  'SHRCB'  =>  '上海农村商业银行',
  'BJBANK' =>  '北京银行',
  'WHCCB'  =>  '威海市商业银行',
  'BOZK'   =>  '周口银行',
  ...
  'LYBANK' =>  '洛阳银行',
  'GDB'    =>  '广东发展银行',
  'ZBCB'   =>  '齐商银行',
  'CBKF'   =>  '开封市商业银行',
```

5.获取银行名称 `BankCard::getBankNameList()` , 如下
```
array (size=165)
  0 => '深圳农村商业银行',
  1 => '广西北部湾银行',
  2 => '上海农村商业银行',
  3 => '北京银行',
  ...
  125 => '广东发展银行',
  126 => '齐商银行',
  127 => '开封市商业银行',
  more elements...
```

6.单独获取银行LOGO `BankCard::getBankImg('ABC')`
```
https://apimg.alipay.com/combo.png?d=cashier&t=ABC
```

##鸣谢
支付宝提供的这么好用的接口 ^_^

##Contributing
有什么新的想法和建议，欢迎提交[issue](https://github.com/zhuzhichao/bank-card-info/issues)或者[Pull Requests](https://github.com/zhuzhichao/bank-card-info/pulls)。


##License
MIT

