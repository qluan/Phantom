# 一些限制

## 构建工具链

- 目前使用 `Gradle 3.3` + `Android Gradle Plugin 2.3.3`。对 `Gradle 4.x` + `Android Gradle Plugin 3.x` 的支持正在进行中

## 四大组件

- 不支持 `ContentProvider`
- 不支持使用 `overridePendingTransition` 设置 `Activity` 切换动画
- 在插件 `AndroidManifest.xml` 配置 `Activity` 旋转属性 `screenOrientation` 无效
- 使用 `Application#registerActivityLifecycleCallbacks` 注册回调无效

## 通知

- 不支持插件中使用自定义 layout 的通知。若插件需要展示自定义 layout 的通知，则需要把 layout 资源文件放到宿主中。

## 第三方库

- 若插件 `compile` 依赖了 `com.android.support:support-v4` ，则需要在 `phantomPluginConfig` 配置 `excludeLib` 剔除