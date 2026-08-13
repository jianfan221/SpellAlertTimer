# SpellAlertTimer (SAT)

Show countdown text next to spell activation overlays

---

## Features

- Displays a countdown number on the spell activation overlay (e.g. proc icons)
- Counts down remaining duration of the relevant buff with high precision
- Precise buff matching via AuraContainer — only shows the intended spell
- Adjustable countdown text size
- Adjustable horizontal offset (positive = spread outward, negative = move inward)
- Overlay opacity follows the Blizzard native setting
- Supports multiple specs / class spell variants via flexible spell ID mapping
- Optional per-spell filtering to hide unwanted overlays
- Clean Blizzard settings panel (`/sat`)
- Lightweight, no unnecessary libraries or dependencies

## Commands

| Command | Description |
|---------|-------------|
| `/sat`  | Open SpellAlertTimer settings panel |

## How to Use

1. Install the addon and type `/sat` to open settings
2. Adjust the countdown text size to your preference
3. Optionally adjust the horizontal offset (positive spreads outward, negative moves inward)
4. The overlay opacity follows the native Blizzard "Spell Alert Opacity" setting
5. When a tracked spell procs, a countdown number appears next to the icon automatically

---

# 中文说明

## 功能特色

- 法术激活（触发图标）时在图标旁显示**倒计时数字**
- 精确倒计时对应增益效果的剩余时间
- 使用 AuraContainer 精确匹配法术，只显示目标法术，避免误显示
- **倒计时文字尺寸可调**
- **水平偏移可调**（正值向两侧外扩、负值向内收拢）
- 透明度跟随暴雪原生"法术激活覆盖"设置
- 支持多专精/职业变体，通过灵活的法术 ID 映射区分（如龙人奶龙/增辉精华迸发）
- 支持按法术过滤，无需显示的可直接隐藏
- 使用暴雪原生设置面板，简洁轻量

## 使用方法

1. 安装插件后输入 `/sat` 打开设置界面
2. 调整倒计时文字尺寸到合适大小
3. 可选调整水平偏移（正值外扩、负值内收）
4. 透明度跟随暴雪原生"法术激活覆盖透明度"设置
5. 触发的法术生效时，图标旁会自动出现倒计时数字

## 作者

**简繁 — 无尽之海 (CN)**

如需反馈问题，可发送邮件至 **32655163@qq.com**
