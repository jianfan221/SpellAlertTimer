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

## Spell ID Mapping

The spell alert overlay uses its own trigger IDs, which sometimes differ from the buff actually gained on your character when the alert fires. A mapping is therefore needed. Most mappings exist because of **stack-based triggers**: the same buff fires with a different alert ID per stack and may appear at a different position (e.g. 1 stack on the left, 2 stacks on the right), while all of them map to the same actual buff ID. Configure it in the `SPELL_ALIAS` table in `SpellAlertTimer.lua`. Supported mapping forms:

- **Single mapping**: `[alertID] = buffID` — maps one alert ID to the single buff ID gained on your character
- **Multiple candidates**: `[alertID] = { buffID1, buffID2 }` — for specs/variants where the buff ID gained differs (e.g. Evoker Augmentation vs Preservation Essence Burst); the AuraContainer matches whichever buff is actually present
- **Hide / filter**: `[alertID] = false` — completely hide the overlay for this spell

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

## 法术 ID 映射

暴雪提供的法术警报触发 ID 有时与触发警报时自身新增的 buff ID 不一致，因此需要映射。**大部分映射是因为叠层触发**：同一 buff 的不同层数会以不同警报 ID 触发，并显示在图标的不同位置（如 1 层触发在左、2 层触发在右），但对应的实际 buff ID 相同。可在 `SpellAlertTimer.lua` 的 `SPELL_ALIAS` 表中配置，支持三种方式：

- **单个映射**：`[警报ID] = buffID`，将一个警报 ID 映射到触发警报时自身新增的那个 buff ID
- **多候选映射**：`[警报ID] = { buffID1, buffID2 }`，用于不同专精/变体新增的 buff ID 不同的情况（如龙人增辉/奶龙精华迸发），AuraContainer 会自动匹配实际存在的那个
- **隐藏/过滤**：`[警报ID] = false`，完全隐藏该法术的倒计时

## 使用方法

1. 安装插件后输入 `/sat` 打开设置界面
2. 调整倒计时文字尺寸到合适大小
3. 可选调整水平偏移（正值外扩、负值内收）
4. 透明度跟随暴雪原生"法术激活覆盖透明度"设置
5. 触发的法术生效时，图标旁会自动出现倒计时数字

## 作者

**简繁 — 无尽之海 (CN)**

如需反馈问题，可发送邮件至 **32655163@qq.com**
