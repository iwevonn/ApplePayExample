[![Build Status](https://travis-ci.org/iwevonn/ApplePayExample.svg?branch=master)](https://travis-ci.org/iwevonn/ApplePayExample)

![](http://upload-images.jianshu.io/upload_images/1511939-63bbdb6559a91a35.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 1 配置证书 [**`Apple Developer`**](https://developer.apple.com/account)

> 1.1) 进入**`Identifiers`** -> **`App IDs`** 的 *`Register iOS App ID`*界面，填写 *Name* 和 *Bundle ID** 
![Register iOS App ID [1]](http://upload-images.jianshu.io/upload_images/1511939-a279f0d95fe8b5ad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 1.2) 勾选*`Apple Pay`*，依次点击**`Continue`** -> **`Submit`** -> **`Done`** 完成注册
![Register iOS App ID [2]](http://upload-images.jianshu.io/upload_images/1511939-437d6383c463f169.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 1.3) 在**`Identifiers`** -> **`App IDs`** 中查找新建的App ID -> 点击 *`Edit`*进行编辑
![Apple Pay当前的状态都是 **Configurable**](http://upload-images.jianshu.io/upload_images/1511939-87400b546fdf51cb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 1.4) 找到*`Apple Pay`*选项 -> 点击 *`Edit`*
![Configurable. Merchant IDs](http://upload-images.jianshu.io/upload_images/1511939-423a0ad1ca3c6e6f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 1.5) 然后  点击 *`Create Merchant ID`* 进入到 *`Registering Merchant ID`*界面
![Merchant ID Assignment](http://upload-images.jianshu.io/upload_images/1511939-ea9377f5b8197173.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 1.6) 填写 *Description* 和 *ID*  然后依次点击 **`Continue`** -> **`Register`** -> **`Done`**
![Registering Merchant ID](http://upload-images.jianshu.io/upload_images/1511939-5915f813b29accb3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 1.7) 完成上面的步骤，*`applepay`*的信息就会显示在 *`Merchant IDs`*的列表中
![](http://upload-images.jianshu.io/upload_images/1511939-f277bec5e2cc53af.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)   
> 1.8) 完成 *`App IDs`* 中未完成的配置，选择相应的   **`Merchant IDs`** ->  **`Continue`** -> **`Assign`**
![](http://upload-images.jianshu.io/upload_images/1511939-532fd6c7c10595e8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
> 1.9) 显示下面的界面，说明成功地更新了 *Merchant IDs* 到 *App ID* 然后点击 *`Done`*结束配置
![](http://upload-images.jianshu.io/upload_images/1511939-506fa4c037bc81ca.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---

- 2 生成证书

> 2.1) 打开”钥匙串访问” 制作 CSR 证书，将下面信息配置好，然后点击`继续`
![从证书颁发机构请求证书...](http://upload-images.jianshu.io/upload_images/1511939-8e10125f836f272f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 2.2)将生成的证书”存储"在桌面  ->  然后”完成”，证书就生成了
![生成.certSigning...文件](http://upload-images.jianshu.io/upload_images/1511939-e1962573a275c695.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 2.3) 进入**`Identifiers`**-> **`Merchant IDs`**  -> *`Edit`*
![](http://upload-images.jianshu.io/upload_images/1511939-7aa9a0b81b3d6e78.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
> 2.4) 询问你是否在美国以外处理您的付款？ 点击*`YES`* -> *`Continue`* ->  *`Continue`*
![](http://upload-images.jianshu.io/upload_images/1511939-5fbaebd1a32f230b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
> 2.5) 点击*`Choose File…`* 然后将生成好的  CSR证书导入进去 然后点击*`Generate`*
![](http://upload-images.jianshu.io/upload_images/1511939-05f94ec4418470de.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
> 2.6) 将制作的好的cer证书*`Download`*然后点击*`Done`*
![](http://upload-images.jianshu.io/upload_images/1511939-b4b6371a0f06189e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
> 2.7) 这时在 **`Identifiers`** -> **`App IDs`** 中 *`Apple Pay`*的选项就会变成*`Enabled`*
![](http://upload-images.jianshu.io/upload_images/1511939-c4c5f34fdca2a1a2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
> 2.8) 将下载的证书导入进钥匙串
![](http://upload-images.jianshu.io/upload_images/1511939-06f6f9875b6d9c38.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
> 2.9) 如果显示证书是由未知颁发机构签名的 [#进入到这个网址下载#](https://www.apple.com/certificateauthority/) 
[WWDR Certificate 证书](https://developer.apple.com/certificationauthority/AppleWWDRCA.cer)
[Worldwide Developer Relations - G2 Certificate 证书](https://www.apple.com/certificateauthority/AppleWWDRCAG2.cer)
>![需要配置的证书](http://upload-images.jianshu.io/upload_images/1511939-de5238b3f764c812.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 2.10)导入上面的证书，现在Merchant ID 证书就显示正常
![显示正常的证书配置](http://upload-images.jianshu.io/upload_images/1511939-7753a07742428298.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---

- 3 Xcode的配置
> 创建一个 iOS项目`所支持的版本 iOS 8.0+`(前提  必须要将你的账号添加进去 **`Xcode`** -> **`Preferences`** -> **`Accounts`**)，在 *`Capabilities`*中 将 *`Apple Pay`* 打开至*`ON`* ，勾选下面的选项， `Steps中有没有错误说明 完成了Apple Pay的环境的搭建`
![Xcode项目中的配置](http://upload-images.jianshu.io/upload_images/1511939-e05a314a1263e6cf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

