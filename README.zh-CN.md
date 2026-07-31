# 动画表现方式图鉴 Motion Design Field Guide

[繁體中文](README.md) ｜ 简体中文 ｜ [English](README.en.md) ｜ [日本語](README.ja.md) ｜ [한국어](README.ko.md)

[![GitHub stars](https://img.shields.io/github/stars/qpalzm963/animation-gallery?style=social)](https://github.com/qpalzm963/animation-gallery/stargazers)

[![动画表现方式图鉴预览](og.png)](https://qpalzm963.github.io/animation-gallery/)

一份单页交互图鉴，收录 **76 个网页动画技法** —— 从最常见的淡入位移，到 FLIP、View
Transitions、滚动时间轴、液态融合、故障艺术这类比较少见的手法。每一张卡片都是**真的在动**的实现：鼠标移到卡片上或按“重播”可以重看一次，附上什么时候该用、以及可以直接抄走的核心代码。

**单个 HTML 文件、零依赖、全部原生 CSS / Web Animations API / Canvas / SVG。**
示范用的代码片段就是实际注入页面的那份字符串 —— 你看到的就是真的在跑的。

## 在线浏览

**https://qpalzm963.github.io/animation-gallery/?lang=cn**

或打开 [`index.html`](index.html)，不需要建置或安装任何东西：

```bash
open index.html
# 或起个本机服务器（View Transitions 的部分示范需要 http:// 而非 file://）
python3 -m http.server 8991
```

## 画面预览

| 浅色主题 | 深色主题（`?theme=dark`） |
|---|---|
| ![浅色主题](assets/home-light.png) | ![深色主题](assets/home-dark.png) |

界面支持五种语言，网址带 `?lang=` 就能直接分享指定语言，例如[日本语版](https://qpalzm963.github.io/animation-gallery/?lang=ja)：

![日文界面](assets/lang-ja.png)

## 内容

12 个分类、76 个技法：

| 分类 | 收录 |
|---|---|
| 基础变化 | 淡入、淡入上移、缩放弹出、旋转、模糊聚焦、翻转、方向擦除 |
| 节奏与缓动 | 缓动曲线并排对照、弹簧物理、过冲回弹、预备动作、错位延迟、挤压伸展、跟随重叠 |
| 布局过场 | FLIP、共享元素、View Transitions API、列表重排、形状变形、高度自动展开 |
| 滚动驱动 | 卷入显现、视差、滚动进度、钉住场景、原生 `animation-timeline` |
| 文字动画 | 打字机、乱码解码、逐字错位、遮罩上推、数字滚动、跑马灯、可变字体、动态排版 |
| 描绘与遮罩 | 线条描绘、沿路径移动、几何遮罩扩散、打勾绘制、渐层擦除、路径变形 |
| 物理与交互 | 磁吸、拖尾光标、惯性滑行、橡皮筋阻尼、粒子系统、触点波纹 |
| 空间与 3D | 倾斜卡片、翻牌、立方体、鼠标分层视差、透视列表 |
| 光影与材质 | 骨架微光、流动渐层、呼吸光晕、颗粒噪点、玻璃模糊、液态融合 |
| 特殊实验 | 故障艺术、色差、逐格 sprite、波浪网格、幕帘转场、像素溶解、弹性指示器、轨道系统 |
| 现代 CSS 转场 | `@starting-style`、`allow-discrete`、`calc-size()`、`linear()` 纯 CSS 弹簧、`@property`、多轨道 keyframes |
| View Transitions | 自订新旧画面、`::view-transition-group()`、方向感知转场、命名撞名教学、清单→详情、跨文档转场（`vt-a.html` / `vt-b.html`） |

另外收录：

- **动画十二法则 → 界面对照** — 迪士尼十二法则换成界面语汇
- **跨平台对照** — CSS / Web、Flutter、SwiftUI 的概念对照表，以及各平台独有的表现方式（SwiftUI 的 `KeyframeAnimator`、`PhaseAnimator`、Liquid Glass；Flutter 的 `Hero`、`Curves`）
- **时长与曲线速查表**

## Prompt 产生器

每张卡片可以一键复制一段结构化 prompt，贴给任何 AI coding agent 就能产出该技法在目标框架的道地实现。工具列选择目标框架（Flutter / SwiftUI / React + Framer Motion / 纯
CSS），prompt 带的是**视觉规格**而不是要求逐行翻译 CSS，并会附上该框架的惯用写法提醒。

## 功能

- 分类筛选、关键字搜索——支持使用情境与英文同义字（“入场”“loading”“页面转场”“slide”都找得到）
- 每张卡标注渲染成本（Composite／Paint／Layout），滑过标签有说明
- 单卡重播 / 全部重播——暂停动态后按单卡重播，可以只单独播那一张，其余维持静止
- 五种语言界面（繁体中文／简体中文／English／日本语／한국어，右上角切换），选择会记住
- 每张卡片都有深链接（点卡片编号复制 `#t-技法id` 链接），可以直接分享特定技法
- 深色／浅色主题切换（预设浅色），选择会记住
- `prefers-reduced-motion` 侦测，会自动暂停示范动画并提供“还是想看”的选项
- 离屏自动卸载，避免大量示范同时运行拖垮性能

## 授权

[MIT](LICENSE) — 可自由取用、修改与再散布。

---

觉得有帮助的话，麻烦点个右上角的 ⭐ Star，让更多人看到这份图鉴。
