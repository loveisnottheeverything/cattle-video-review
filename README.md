# 牧场视频证据台

这是比赛视频素材理解结果的静态展示站点，可直接通过 GitHub Pages 发布。

## 在线展示

**[打开牧场视频证据台](https://loveisnottheeverything.github.io/cattle-video-review/)**

页面支持深色与浅色主题，可在电脑、平板和手机浏览器中直接审阅素材。

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

## GitHub 授权备用方案

Codex 内置 GitHub 插件如果无法加载，可直接使用本机已安装的 GitHub CLI：

```powershell
gh auth login --hostname github.com --git-protocol https --web --clipboard
```

命令会复制一次性设备码。浏览器回调异常时，可在手机或其他已登录 GitHub 的设备访问 <https://github.com/login/device>，粘贴设备码并确认。

如果 GitHub CLI 设备授权不可用，还可以使用 Git for Windows 自带的 Credential Manager：

```powershell
git credential-manager github login --device
```

个人访问令牌只作为最后备选；不要把令牌写入仓库、脚本、远程地址或命令历史。
