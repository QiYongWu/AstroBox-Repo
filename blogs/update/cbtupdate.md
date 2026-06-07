---
type: "更新日志"
title: "CBT3 正式发布"
subtitle: "查看本次重大更新说明"
author: "Yulimfish"
date: 2026-05-04
cover: "https://raw.githubusercontent.com/AstralSightStudios/AstroBox-Repo/refs/heads/main/blogs/update/update.png"
---


# 特别提醒

- 因本次功能新增较多，建议卸载旧版本后安装。
- 从本版本开始，我们放开了对大家的截图外传限制。这意味着你可以发布截图到本群以外的位置帮助我们宣传，但是我们依旧要求大家不外传包体、不外借测试账号，若被发现则永久禁止参与先锋测试。
- 欢迎大家通过正常手段在已适配 V2 的资源中多多发布评论，进行评论区压力测试，这有利于我们进行服务器安全与稳定性评估。测试账号及评论区数据将不会在正式版发布时顺延，大家方可放心尝试。
- 测试阶段会员不开放购买，所以会员页面跳转出去无购买途径。
- 测试阶段大陆资源镜像不开放使用。
- i18n 忘记同步了，你们忍一下。

---

# 新功能一览

![绑定米坛账号](https://raw.githubusercontent.com/AstralSightStudios/AstroBox-Repo/refs/heads/main/blogs/update/1.png)

- (米坛深度合作) 支持将 AstroBox 账号与米坛社区账号绑定，并同步登录
- 小米账号的登录状态将被持久化本地存储
- 支持试用来自 AstroBox 官方源的付费表盘资源
- 支持安装来自 AstroBox 官方源的加密资源.目前 AB 娘动态表盘已首发支持付费表盘试用与快捷安装。

::resource{id=979897989798}

- 插件市场支持通过自定义 Provider 接入第三方源

![网络设置页面](https://raw.githubusercontent.com/AstralSightStudios/AstroBox-Repo/refs/heads/main/blogs/update/2.png)

- 设置中新增“网络”页面，可调整官方社区源节点、账号系统节点
- 现在支持使用 DoH 进行域名解析，可在“网络”页面中调整
- 设备页中固件版本卡片新增子页面，并支持通过官方接口检查通过小米账号导入的设备的固件更新

![全新音乐、录音卡片](https://raw.githubusercontent.com/AstralSightStudios/AstroBox-Repo/refs/heads/main/blogs/update/2+.png)

- 设备页中新增“音乐”卡片，不要问有什么用，问就是现在 iOS 用户终于能向手表音乐 APP 导入本地音乐了
- 设备页中新增“录音”卡片，前端新增录音管理页面，支持导出设备上的录音文件。
- 实现了 AstroBox 捐赠计划相关订阅页面
- 探索页加入 Pro 会员专属新背景
- 插件支持自动检查更新并提示
- 资源支持自动检查更新并提示
- (移动端) 新增了三款用于展示设备状态的桌面小组件

![全新灵动岛设计登场](https://raw.githubusercontent.com/AstralSightStudios/AstroBox-Repo/refs/heads/main/blogs/update/3.png)

- (iOS与macOS) 安装资源时的灵动岛现在具有全新的设计
- (iOS) 新增了一款锁屏小组件
- (iOS与macOS) 新增三维震动支持，在设备页中编辑卡片位置时，将为 iPhone 和 MacBook 的Force Touch 触控板提供震感反馈 (可关闭)
- 设置 ⟶ 神笔妙妙工具中新增了设备日志拉取与运行环境信息拉取、发包性能检测的选项
- (移动端) 设置 ⟶ 神笔妙妙工具中新增打包分享日志文件的选项，可直接通过该选项打包近期日志文件并拉起分享
- 实现了 PC 端的 ServerLink 机制，登录不再依赖不稳定的 DeepLink

---

# 插件接口/开发工具相关

在该版本中，插件接口的功能实现已经完全完成。

- 插件接口：调整了 API Level 的定义逻辑，将由Interface 拆分改为由 World 拆分以确保可扩展性
- 插件接口：支持加载自定义 i18n 文件
- 插件接口：支持使用 transport 接口与设备进行 raw 通信
- 插件接口：支持使用 register 接口注册设备页卡片
- 插件接口：新增 UI (API Level 3)，包含更多可用组件和动画元素
- 插件接口：新增 watchface，可管理设备表盘
- 插件接口：支持使用 register 接口添加自定义社区源
- 调试窗口：控制台支持渲染彩色文本
- 新增了一些本地服务接口以供 astrobox-cli 使用，并提供配套 skills 以让 AI Agents 能自动化调用 AstroBox 相关功能

同时，我们新增了一些本地接口以供 astrobox-cli 使用，并提供配套 skills 以让 AI Agents 能自动化调用 AstroBox 相关功能

---

# 体验提升

- (CBT) 移除了所有 UI 内水印与测试标识
- OOBE 流程优化
- 移动端：插件功能页面改为了类似小程序的样式
- PC 端：插件功能页面改为了弹出的独立窗口，可在设置中改为内置页面
- 现在支持在设置中调整设备页的打开方式了
- 优化了插件市场的加载速度
- 新增 URL 转换与流式通用下载接口，提升资源拉取灵活性。
- (macOS) 全新的DMG安装器样式设计
- (iOS与macOS) Liquid Glass 图标样式优化
- 优化了程序打开时的“插件系统正在初始化”页面样式
- (iOS) 优化设备连接流程
- 优化了 iOS 蓝牙的传输逻辑
- 提升了 macOS 的资源传输速度
- 部分 UI 样式优化调整

---

# 问题修复

![AstroBox 又能流畅通过小米账号同步设备了](https://raw.githubusercontent.com/AstralSightStudios/AstroBox-Repo/refs/heads/main/blogs/update/4.png)

- 修复了登录小米账号可能卡 2FA 的问题
- 修复了插件市场部分子仓结构异常时可能导致整个插件市场无法加载的问题
- 修复了从小米账号导入设备时会重复导入已有设备的问题
- 修复了部分页面标签可能闪烁的问题
- 修复了插件加载失败时无法删除插件导致程序无法启动的问题

![](https://raw.githubusercontent.com/AstralSightStudios/AstroBox-Repo/refs/heads/main/blogs/update/5.png)