# AWEABTestDataPatch

## **暂停维护中，接受PR**

> [!NOTE]
>  **说明** | 2025.08.04  
>  下半年事务繁忙，暂缓维护，敬请谅解

🎯 **用于修改抖音热更新文件的 JSON 数据补丁，作用于覆写模式**

---

## 📌 项目简介

`AWEABTestDataPatch` 是一个用于定制和优化抖音热更新文件的JSON覆写补丁。通过修改关键字段，可以实现定制化的 UI 和交互体验，避免一些默认行为带来的困扰。  

---

## 📂 配置文件说明

项目中包含以下 3 个 JSON 覆写文件，可根据实际需要选择使用：
| 文件名                      | 描述                               |
| ------------------------ | -------------------------------- |
| `ABTestDataPatch_A.json` | **稳定版覆写**：仅开启基础优化项，关闭热更新推送的新功能，稳定性优先，适合大多数用户 |
| `ABTestDataPatch_B.json` | **尝鲜版覆写**：开启新功能和交互，适合追求新体验的用户  |
| `ForPrivateUse.json`     | **自定义覆写**：自用版本，有个人偏好配置   |


---

## 🛠 使用方法
- 🌟应用方式使用远程模式（推荐）
    1. 增强设置-热更新-禁止下发配置开启,配置应用方式>远程模式
    2. 远程配置地址根据自身需要选择：
        - `https://github.com/Nathalie-Annis/AWEABTestDataPatch/releases/latest/download/ABTestDataPatch_A.json` （稳定版，插件默认指定无需修改） 
        - `https://github.com/Nathalie-Annis/AWEABTestDataPatch/releases/latest/download/ABTestDataPatch_B.json` （尝鲜版，将A替换为B即可）
        - `https://raw.githubusercontent.com/Nathalie-Annis/AWEABTestDataPatch/refs/heads/main/ForPrivateUse.json` （自用版）
    3. 点击检查配置更新，重启 App 即可生效

- 🌟应用方式使用覆写模式（推荐）
    1. 选择一个合适的热更新覆写版本，下载覆写文件
    2. 修改覆写文件中的 JSON 键值对以满足个人需求（可选） 
    3. 增强设置-热更新-禁止下发配置开启,配置应用方式>覆写模式,导入本地配置
    4. 选择覆写文件，重启 App 即可生效

- 应用方式使用替换模式
    1. 选择一个合适的热更新配置(**🔥通常应为完整的、大小4MB+的热更新文件；不是此处提供的KB级大小的覆写文件**)
    2. 修改配置文件中的 JSON 键值对以满足个人需求
    3. 增强设置-热更新-禁止下发配置开启,配置应用方式>替换模式,导入本地配置
    4. 选择配置文件，重启 App 即可生效
    
---

## ⚙️ 支持的热更新字段说明

以下是目前支持的热更新配置键及其功能说明，你可以根据自己的实际需求进行添加、修改或删除：

| 键名 | 说明 | 默认行为 |
|------|------|----------|
| `AWEAlbumOverallCellLevelShrink` | 图文开启缩略图样式 | `true`/`false` 控制 |
| `AWEDetailCommentInputShow` | 图文展开后的中部评论条 | `true`/`false` 控制(34.2.0及以下) |
| `AWEFeedAlbumShortDescShowExpansion` | 图文文案完整时的展开按钮 | `true`/`false` 控制 |
| `AWEFullPageEnableRelatedRecommend` | 图文文案展开样式控制 | `enable=false` 仅展开文案；`enable=true` 展示相关推荐 |
| `AWEMusicDetailRelatedEnable` | 新版音乐图标 | `enable=false`不显示 |
| `AWENotesDotProgress` | 部分多图图文新版滑条样式 | `true`/`false` 控制 |
| `AWESLIDES_SCALE_EXPERIMENT` | 图文开启缩略图样式 | **删除此键** 以禁止图文缩略图 |
| `background_play_small_window_config` | 官方默认设为`1`开启，会将播放设置中的专注模式后台小窗播放（此时支持图文小窗播放）替换为后台小窗播放。设为`0`禁用后，同时需要确保`官方设置-通用-播放设置-仅从专注模式下退出时生效`开启才会起作用，这样就实现了同时支持后台播放声音（直接退出）和后台小窗播放（专注模式下退出）两种逻辑 | `1`/`0` 控制 |
| `c2_feed_switch_preview_entry` | 单击首页显示单双列切换视图 |  `1`/`0` 控制 |
| `c2_recommend_feed_entry_style` | 首页双列按钮 | `enable=0` 关闭 | 
| `detail_page_panel_config` | 视频文案展开样式控制 | `enable=0` 仅展开文案；`enable=1` 展示相关推荐 |
| `double_column_recommend_exp` | 顶部推荐 Tab 样式及刷新机制 | 控制小白条展示行为 | 
| `edge_fast_speed_toast_style` | 长按侧边倍速显示样式跟随新版长按菜单顶部样式 | `true`/`false` 控制 |
| `familiar_recommend_entrance_lp_panel_pos` | 新版长按菜单的推荐入口显示 | `1`/`0` 控制 |
| `familiar_recommend_icon_when_switch_share_and_recommend` | 加载推荐和取消推荐图标 | 需要填入完整链接 |
| `favorite_list_style` | 收藏列表切换样式按钮 | `1`/`0` 控制 |
| `feed_desc_lines_count` | 部分图文文案显示的行数 | 官方默认值 `2` |
| `feed_related_recommend_stable_entrance` | 文案末尾小箭头 | **删除此键** 不显示 |
| `general_search_layout_type` | 搜索页搜索结果切换双列显示按钮 | `2` 显示 |
| `homepage_long_press_setting` `homepage_remote_ab_config` | 首页单击/双击/长按行为配置 | 设置为 `false` 关闭相关功能 |
| `hp_left_slide_to_user_page_config` | 关注、直播等页面边缘左滑进入用户主页 | `edge_slide_width` 控制边缘触发距离，官方默认值 `76` |
| `im_share_panel_arrangement_strategy` | 新版分享面板失效问题 | **删除此键** 可解决 |
| `im_support_user_bubble` | 聊天支持更换气泡 | `"-1"` 开启 |
| `interaction_element_dd_config` | 自定义图文图标大小失效问题 | **删除此键** 可解决 |
| `long_press_fast_speed_enabled_scene` | 长按触发2倍速播放 | `true`/`false` 控制 |
| `long_press_lock_speed_config` | 长按上/下拉锁定倍速触发距离 | 修改 `distance`，官方默认值 `distance=250` |
| `long_press_modal_show_hint_label` | 新版长按菜单显示操作提示 | `true`/`false` 控制 |
| `long_press_panel_refactor` | 新版长按菜单 | `true`/`false` 控制 |
| `long_press_panel_speed_optimize` | 自定义长按面板中的倍速选项 | 可自由配置倍速参数 |
| `long_press_play_control_modal_quick_items` | 新版长按菜单左右按钮显示的功能 | 设置为特定值开启对应功能 |
| `long_press_play_control_modal_switch` | 新版长按菜单 | `1`/`0` 控制 |
| `pinch_long_press_hot_area_opt` | 清屏状态下等价于长按菜单的按钮 | `1`/`0` 控制 |
| `pinch_to_c2_feed` | 双指缩小画面切换双列视图 | `enable=false` 关闭 |
| `pinch_video_scale_follow_opt` | 清屏状态下双指缩放画面 | `1`/`0` 控制 |
| `profile_like_status_shown_on_cover` | 主页点赞红心展示 | `1`/`0` 控制 |
| `profile_post_hot_sort_exposed` | 主页新版最新最热标签 | 用户主页只有作品时显示, `1`/`0` 控制 |
| `recommend_to_friend_tag_view_refactor` | 推荐给朋友标签右侧编辑按钮 | `true`/`false` 控制 |
| `share_strengthen_panel_type` | 新版分享面板 | `""`开启 |
| **`*`** | **更多功能** | **待发掘，欢迎提出 / PR ！❤️热更新的发现有赖于不同人下发的不同配置❤️** |

---

## 📎 注意事项

* 部分热更新功能会随着版本更新而被固化，这也是热更新的意义所在；这将会导致这些功能不再受热更新控制——切用且珍惜
* 部分热更新键值仅在高客户端版本下有效，客户端版本过低会导致失效，请根据实际情况调整
* 热更新覆写仅在最新版本的客户端中测试

---

## 📝 许可协议

本项目遵循 MIT License，详情见 [LICENSE](./LICENSE)。

---