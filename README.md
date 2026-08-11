# 牧场视频证据台

这是比赛视频素材理解结果的静态展示站点，可直接通过 GitHub Pages 发布。

## 公开内容

- 170 条有效素材的结构化理解
- 每条素材的三帧关键帧
- 69 条 Qwen Omni 音视频联合理解记录
- 检索、筛选、时长排序、网格／列表切换和详情弹窗

公开仓库不包含原始视频、Qwen API 密钥、生成脚本或完整分析工作目录。详情页中的素材文件名仅用于课题组内部追溯。

## 更新页面

在上一级工作目录重新生成并同步公开站点：

```powershell
python build_video_review_page.py --export-site
```

然后在本目录提交并推送更新：

```powershell
git add -A
git commit -m "Update video review data"
git push
```

GitHub Pages 会在推送后自动发布新版本。
