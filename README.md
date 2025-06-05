# AWEABTestDataPatch

🎯 **用于修改抖音热更新文件的 JSON 数据补丁**

---

## 📌 项目简介

`AWEABTestDataPatch` 是一个用于定制和优化抖音热更新文件的数据补丁。通过修改关键字段，你可以实现定制化的 UI 和交互体验，避免一些默认行为带来的困扰。

---

## ⚙️ 支持的热更新字段说明

以下是目前支持的热更新配置键及其功能说明(基于Patch_A)，你可以根据自己的实际需求进行添加、修改或删除：

| 键名 | 说明 | 默认行为 |
|------|------|----------|
| `share_strengthen_panel_type` | 新版分享面板 | 添加此键即开启 |
| `profile_like_status_shown_on_cover` | 主页点赞红心展示 | `1` 开启 |
| `favorite_list_style` | 收藏列表切换样式按钮 | `1` 开启(仅热更新配置有效) |
| `interaction_element_dd_config` | 自定义图文图标大小失效问题 | **删除此键** 可解决 |
| `feed_related_recommend_stable_entrance` | 文案末尾小箭头 | **删除此键** 不显示 |
| `AWESLIDES_SCALE_EXPERIMENT` | 评论弹出时上移图文内容 | **删除此键** 可禁止 |
| `AWEFeedAlbumShortDescShowExpansion` | 图文文案完整时显示展开按钮 | `false` 不显示 |
| `AWENotesDotProgress` | 部分多图图文新版滑条样式 | `false` 不显示 |
| `AWEDetailCommentInputShow` | 图文展开后显示中部评论条 | `false` 不显示(34.2.0及以下) |
| `feed_desc_lines_count` | 部分图文文案显示的行数 | 官方默认值 `2` |
| `AWEMusicDetailRelatedEnable` | 新版音乐图标 | `enable=false`不显示 |
| `detail_page_panel_config` | 视频文案展开样式控制 | `enable=0` 仅展开文案；`enable=1` 展示相关推荐 |
| `AWEFullPageEnableRelatedRecommend` | 图文文案展开样式控制 | `enable=false` 仅展开文案；`enable=true` 展示相关推荐 |
| `long_press_fast_speed_enabled_scene` | 长按触发2倍速播放 | `true` 开启 |
| `long_press_lock_speed_config` | 长按上/下拉锁定倍速触发距离 | 修改 `distance`，官方默认值 `distance=250` |
| `long_press_play_control_modal_switch` | 新版长按菜单 | `0` 关闭 |
| `long_press_modal_show_hint_label` | 新版长按菜单显示操作提示 | `false` 关闭 |
| `long_press_play_control_modal_quick_items` | 新版长按菜单左右按钮显示的功能 | 设置为特定值开启对应功能 |
| `edge_fast_speed_toast_style` | 长按侧边倍速显示样式跟随新版长按菜单顶部样式 | `false` 关闭 |
| `long_press_panel_speed_optimize` | 自定义长按面板中的倍速选项 | 可自由配置倍速参数 |
| `homepage_remote_ab_config`  `homepage_long_press_setting` | 首页单击/双击/长按行为配置 | 设置为 `false` 关闭相关功能 |
| `c2_recommend_feed_entry_style` | 首页双列按钮 | `enable=0` 关闭 | 
| `double_column_recommend_exp` | 顶部推荐 Tab 样式及刷新机制 | 控制小白条展示行为 | 
| `*` | 更多 | 待发掘 |

---

## 📂 配置文件说明

项目中包含以下 3 个 JSON 补丁文件，可根据实际需要选择使用：
| 文件名                      | 描述                               |
| ------------------------ | -------------------------------- |
| `ABTestDataPatch_A.json` | **稳定版补丁**：仅开启基础优化项，关闭热更新推送的新功能，稳定性优先，适合大多数用户 |
| `ABTestDataPatch_B.json` | **尝鲜版补丁**：开启新功能和交互，适合追求新体验的用户  |
| `ForPrivateUse.json`     | **自定义补丁**：自用版本，有个人偏好配置   |


---

## 🛠 使用方法

- 使用热更新补丁
    1. 选择一个合适的热更新补丁版本，下载补丁文件
    2. 修改补丁文件中的 JSON 键值对以满足个人需求（可选） 
    3. 增强设置-热更新-启用补丁模式（确保禁用下发配置关闭）-本地选择配置
    4. 选择下载的补丁文件，重启 App 即可生效

- 使用热更新配置
    1. 选择一个合适的热更新配置
    2. 修改配置文件中的 JSON 键值对以满足个人需求
    3. 增强设置-热更新-禁用下发配置（确保启用补丁模式关闭）-本地选择配置
    4. 选择配置文件，重启 App 即可生效
---

## 📎 注意事项

* 热更新配置仅在最新版本的客户端中测试
* 配置可能因客户端版本不同而略有差异或失效，请根据实际情况调整

---

## 📝 许可协议

本项目遵循 MIT License，详情见 [LICENSE](./LICENSE)。

---