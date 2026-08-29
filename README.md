# 智能体重健康分析助手 / Smart Health Analyzer

这是一个轻量级、纯前端、无依赖的单页网页应用。用户只需输入性别、身高、体重、体脂率、肌肉量，即可快速评估当前的体脂重量、标准体重区间、肌肉率，并计算出距离目标体重需要增减的重量以及按计划达标所需的时间。

This is a lightweight, pure front-end, dependency-free single-page web application. Users only need to input gender, height, weight, body fat percentage, and muscle mass to quickly evaluate their current fat mass, ideal weight range, muscle ratio, and calculate the exact weight to lose/gain, along with the estimated time to reach their goal.

---

## ✨ 核心功能 / Core Features

- **精准标准体重计算**：内置男女身高 140cm - 190cm 的标准体重对照数据，自动查找并给出合理的体重区间。
  *Accurate Ideal Weight Calculation*: Built-in standard weight data for heights from 140cm to 190cm for both men and women, automatically providing a healthy weight range.

- **体脂重量计算**：根据输入的体重和体脂率（%），精准计算当前的脂肪重量（kg）。
  *Fat Mass Calculation*: Accurately calculates current fat mass (kg) based on input weight and body fat percentage (%).

- **肌肉率计算**：新增肌肉量（kg）输入，自动计算肌肉量占总体重的百分比（%），更全面地评估身体成分。
  *Muscle Ratio Calculation*: Added muscle mass (kg) input to automatically calculate the percentage of muscle mass in total body weight (%), providing a more comprehensive body composition assessment.

- **智能差值估算**：自动对比当前体重与标准区间，清晰显示你需要**增加**或**减少**多少公斤；若已达标则明确显示无需调整。
  *Smart Weight Gap Estimation*: Automatically compares current weight against the standard range, clearly showing how many kg to *gain* or *lose*; if already within range, it clearly states no changes are needed.

- **目标周期预估**：按照“每 3kg 一个月”的标准，提供达到目标体重所需的预估月份（含小数点向上取整），并附带预估周数。
  *Goal Timeline Estimation*: Based on the "3kg per month" rule, provides an estimated number of months (rounded up to the nearest integer) and weeks to reach the target weight.

- **中英双语一键切换**：页面所有 UI 文本、标签、结果说明均支持中文（华语）与英文无缝切换。
  *One-click Bilingual Switching*: All UI texts, labels, and result messages seamlessly switch between Chinese (Hua Yu) and English.

- **手机深色模式自动适配**：自动检测手机/系统的深浅色模式，动态切换高对比度颜色，暗光环境下字体清晰不刺眼、不融底。
  *Automatic Dark Mode Adaptation*: Automatically detects system dark/light mode, switches to high-contrast colors, ensuring readable fonts in low light without blending into the background.

- **手机键盘防遮挡优化**：针对移动端体验深度优化，输入数字时键盘弹起，页面会自动平滑滚动且保持在合理的视觉位置，绝不会被键盘挡住或强行居中导致错乱。
  *Mobile Keyboard Avoidance Optimization*: Deeply optimized for mobile. When the soft keyboard pops up, the page smoothly scrolls to keep the active input at an optimal position, never blocked or misaligned by the keyboard.

---

## 🛠️ 技术栈 / Tech Stack

- *HTML5 / CSS3*
- *原生 JavaScript (Vanilla JS)*
- **CSS 变量 (CSS Variables)**：用于实现明暗主题的即时切换。 / Used for instant theme switching.
- **Media Query (prefers-color-scheme)**：实现系统深色模式检测。 / Implements system dark mode detection.
- **VisualViewport API**：用于处理移动端软键盘弹起后的视口变化和自动滚动。 / Handles viewport changes and auto-scrolling when the mobile soft keyboard pops up.
- **Meta Tag (interactive-widget=resizes-content)**：解决 iOS/Android 浏览器的软键盘遮挡问题。 / Solves soft keyboard occlusion issues on iOS/Android browsers.

---

## 🚀 使用方法 / How to Use

1. 下载或复制 index.html 文件。
   Download or copy the index.html file.
2. 将文件重命名为 index.html`（或其他你喜欢的 .html` 名字）。
   Rename it to index.html (or any other .html name you prefer).
3. 使用任何现代浏览器（Chrome, Safari, Edge, Firefox 或手机自带浏览器）双击直接打开即可运行。**无需搭建服务器，无需联网。**
   Open it directly with any modern browser (Chrome, Safari, Edge, Firefox, or the mobile default browser). *No server required, no internet needed.*

---

## 📊 输入与输出说明 / Input & Output Specifications

*输入项 / Inputs:*
- 性别 / Gender (Female / Male)
- 身高 / Height (cm) - 仅支持 140 - 190 的整数 / Integers only from 140 to 190
- 当前体重 / Current Weight (kg)
- 体脂率 / Body Fat (%)
- *肌肉量 / Muscle Mass (kg)* - 需小于总重量 / Must be less than total weight

*输出项 / Outputs:*
- *体脂重量 / Fat Mass* (Current fat mass in kg)
- *标准体重区间 / Ideal Weight Range* (Healthy range based on height, e.g., 55.0 kg - 58.9 kg)
- *需要增加/减少的体重 / Weight to Gain/Lose* (Displayed in large font, automatically colored red, blue, or green)
- *达标所需时间 / Time to Reach Goal* (Estimated months and weeks)
- *肌肉率 / Muscle Ratio* (Percentage of muscle mass in total body weight)

---

## 🎨 UI 视觉设计规则 / UI Visual Design Rules

结果区域采用模块化卡片设计，方便快速获取信息：
The results area uses modular card designs for quick access to information:
- *体脂重量 / Fat Mass*: 紫色系卡片 / Purple-themed card
- *标准体重区间 / Ideal Weight Range*: 橙色系卡片（全宽，一行显示）/ Orange-themed card (Full width, single line)
- *需要增减量 / Weight to Change*: 红色（需减）/ 蓝色（需增）/ 绿色（已达标）/ Red (Need to lose) / Blue (Need to gain) / Green (Within range)
- *达标时间 / Time to Goal*: 与增减量主色调同步，采用白底同色字，形成视觉配对。 / Synchronizes with the main color of the weight change card, using white background with same-colored text for visual pairing.
- *肌肉率 / Muscle Ratio*: 青色系卡片（全宽，放在需要增减量下方）/ Cyan-themed card (Full width, placed below the weight change cards)

---

## ⚠️ 注意事项 / Important Notes

本工具的数据基于通用的健康体重/体脂对照表（Ideal Weight vs Height Chart），**仅供参考，不构成任何医疗建议**。
This tool's data is based on general healthy weight/body fat charts (Ideal Weight vs Height Chart) and is *for reference only and does not constitute medical advice*.

人体是一个复杂的系统，标准体重受 *年龄、骨架大小、肌肉量* 等因素影响极大。肌肉密度大于脂肪，经常健身、肌肉发达的人，即使体重超过了标准区间，也绝对非常健康。建议结合专业体脂秤或健身房的体成分分析仪获取更准确的数据。
The human body is a complex system. Standard weight is heavily influenced by *age, bone structure, and muscle mass*. Muscle is denser than fat; therefore, active individuals with high muscle mass may exceed the standard weight range while remaining perfectly healthy. It is recommended to combine this data with professional body fat scales or gym body composition analyzers for more accurate results.

---
项目说明：完全由 HTML/CSS/JS 单文件构建，可直接离线使用。
Project Description: Built entirely as a single HTML/CSS/JS file, usable completely offline.
