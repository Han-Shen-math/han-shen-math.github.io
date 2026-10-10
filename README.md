# ShenHan · 智能、研究与探索

GitHub Pages 静态研究主页，围绕具身智能与世界模型、大模型、神经科学启发的模型架构展开。

长期愿景：让智能技术释放人类劳动力，让人们拥有更多时间与自由。

网站使用纯 HTML、内联 CSS 和少量 JavaScript，无需安装依赖或执行构建。

## 文件

- `index.html`：网站内容、布局与深浅主题切换。
- `research-notes.html`：从具身经验到世界模型的初步研究设想。
- `.nojekyll`：按静态文件发布。

## 发布

目标仓库：`Han-Shen-math/han-shen-math.github.io`。

在仓库的 Settings → Pages 中选择 Deploy from a branch，使用 `main` 分支的 `/ (root)`，保存后等待 GitHub 部署完成。

预期网站地址：https://han-shen-math.github.io/

## 本地预览

在项目目录运行 `python3 -m http.server 8765 --bind 127.0.0.1`，然后打开 http://127.0.0.1:8765/。

## 后续更新

在 `index.html` 中修改简介、项目和记录入口；研究笔记保存在 `research-notes.html`。提交到 `main` 后会触发自动更新。

当前项目暂时只收录 LeRobot fork 与已提交的 PR #4902。研究设想根据个人讨论整理，明确区分未来研究计划与已验证结果。
