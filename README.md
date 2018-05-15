# FFDExtension
* UserDefaults+FFExtension的使用

首先 定义俩个要存储的值 不需要设置key 可以设置默认值
```
 var string1: String? {
        get { return FFDUserDefaults.ffd_stringForKey() }
        set { FFDUserDefaults.ffd_setString(newValue) }
    }

 var string2: String? {
        get { return FFDUserDefaults.ffd_stringForKey(defaultValue: "defaultValueString") }
        set { FFDUserDefaults.ffd_setString(newValue) }
    }
```

调用 当值为nil移除该key
```
/// 设置并存储string1, string2的值
    FFDUserDefaults.string1 = "string1"
    FFDUserDefaults.string2 = "string2"
/// 获取string1, string2 的值
    let _ = FFDUserDefaults.string1
    let _ = FFDUserDefaults.string2
```
