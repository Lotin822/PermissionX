# PermissionX

PermissionX是一个用于简化Android运行时权限用法的开源库

添加如下配置将PermissionX引入到你的项目中:

```groovy
dependencies {
    ...
    implementation 'io.github.Lotin822:PermissionX:1.0.0'
}
```

然后就可以使用如下语法结构来申请运行时权限了:

```kotlin
PermissionX.request(this, Manifest.permission.CALL_PHONE,
    Manifest.permission.READ_CONTACTS) { allGranted, deniedList ->
    if (allGranted) {
        Toast.makeText(this, "All permissions are granted",
            Toast.LENGTH_SHORT).show()
    } else {
        Toast.makeText(this, "You denied $deniedList",
            Toast.LENGTH_SHORT).show()
    }
}
```