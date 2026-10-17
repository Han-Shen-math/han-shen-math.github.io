# ShenHan · 智能、研究与探索

GitHub Pages 静态研究主页，围绕具身智能与世界模型、大模型、神经科学启发的模型架构展开。

长期愿景：让智能技术释放人类劳动力，让人们拥有更多时间与自由。

网站使用纯 HTML、内联 CSS 和少量 JavaScript，无需安装依赖或执行构建。

## 文件

- `index.html`：网站内容、布局与深浅主题切换。
- `research-notes.html`：从具身经验到世界模型的初步研究设想。
- `papers/finite-texts-authorial-intention.html`：作者意图与哲学批判英文初稿的网页全文。
- `assets/papers/finite-texts-authorial-intention-2026-10-17.pdf`：对应的六页英文 PDF 原稿。

## 发布

目标仓库：`Han-Shen-math/han-shen-math.github.io`。

在仓库的 Settings → Pages 中选择 Deploy from a branch，使用 `main` 分支的 `/ (root)`，保存后等待 GitHub 部署完成。

预期网站地址：https://han-shen-math.github.io/

## 本地预览

在项目目录运行 `python3 -m http.server 8765 --bind 127.0.0.1`，然后打开 [本地预览](http://127.0.0.1:8765/)。

## 后续更新

在 `index.html` 中修改简介、项目和记录入口；研究笔记保存在 `research-notes.html`。提交到 `main` 后会触发自动更新。

## 论文与手稿

首页 `#papers` 为论文与手稿区域，顶部导航在电脑与手机端均保留“论文”入口。第一篇为 *Finite Texts, Authorial Intention, and Philosophical Criticism*（2026-10-17，English draft），提供网页全文和 PDF 下载。沿用原稿的草稿状态，不标记为已发表、已录用或在审。新增文章时在该区域添加条目，并在 `papers/` 和 `assets/papers/` 放置对应网页及 PDF；保留明确日期与版本状态。

## 近期公开贡献

状态快照：**2026-10-12 03:48 UTC**。本次列出 10 项已核实贡献：6 个本人 PR、1 项参与他人 PR 的验证、3 条 issue 技术讨论。SpikingJelly #773 已合并，其余 6 个相关 PR 仍未合并。验证数字来自公开 PR、CI 和固定提交报告；本地验证记录不等于托管 CI 通过。本次网站更新核实作者、链接与状态，未重新运行上游项目实验。

| 贡献与源链接 | 角色、状态 | 验证证据与范围 |
| --- | --- | --- |
| [TorchEEG #166：标准 PhaseLockingValue](https://github.com/torcheeg/torcheeg/pull/166) | 本人作者；开放、非草稿、未合并；暂无评论或评审 | 新增标准 PLV EEG transform，说明旧 PhaseLockingCorrelation 行为并保持兼容，关联仍开放的 [issue #105](https://github.com/torcheeg/torcheeg/issues/105)。创建于 2026-10-11 22:45:04 UTC。作者在 PR 中报告 Mac CPU 17 项专项与 65 项相关测试通过，以及旧行为等价检查、聚焦相关 API 的严格文档构建、wheel 安装数值检查；未跑全量套件或真实 EEG 分类 benchmark。[固定提交数学与兼容性说明](https://raw.githubusercontent.com/Han-Shen-math/torcheeg/03a85ec573049bcc09a95d2d49a2d23cb742041c/docs/source/phase_locking_value.rst)。[托管 Tests](https://github.com/torcheeg/torcheeg/actions/runs/38181660684) 为 action_required、零 jobs，未运行。 |
| [MetaBCI #120：未训练 EEG Transformer](https://github.com/TBC-TJU/MetaBCI/pull/120) | 本人作者；开放、草稿、未合并 | trial ID 对齐的辅助特征、small / large 预设与训练/checkpoint 接口；Mac CPU 91 项软件检查通过。未执行拟合或优化器步骤；实际训练/恢复、真实 EEG 准确率与 CUDA 未验证。[固定提交文档](https://raw.githubusercontent.com/Han-Shen-math/MetaBCI/76b82a3f5d68493e989a0608d1849dd15540b33f/docs/source/eeg_transformer.rst)。 |
| [LeRobot #4916：可选 CUDA 图像预处理](https://github.com/huggingface/lerobot/pull/4916) | 本人作者；开放、草稿、未合并 | HIL-SERL 可选 image_device，保留 CPU 默认、状态位置与旧配置；39 passed、3 CUDA skipped。尚无实测加速、训练或 robot rollout。[固定提交文档](https://raw.githubusercontent.com/Han-Shen-math/lerobot/14bb151979ca2f2658c69ba6133e903472cef9e5/docs/source/hilserl.mdx)。s1lent4gnt 于 2026-10-11 18:40:41 UTC 自行认领，尚无评审或批准。 |
| [SpikingJelly #773：可训练 signed ternary IF / LIF](https://github.com/fangwei123456/spikingjelly/pull/773) | 本人作者；维护者整理后已合并；CI 通过 | AllenYolk 于 2026-10-11 08:46:20 UTC 合并，[合并提交 a230b4d](https://github.com/fangwei123456/spikingjelly/commit/a230b4d053a600f4bca4ac679080eda31e8b0ee0)。维护者追加两次整理提交，并给出 [LGTM](https://github.com/fangwei123456/spikingjelly/pull/773#issuecomment-6107263123)。最终 PR 的 Mac 验证为 170 passed、2 skipped、72 项前后等价检查；最新 [CI](https://github.com/fangwei123456/spikingjelly/actions/runs/38125399474) 的 CPU 测试为 1682 passed、1439 skipped，严格文档构建与安装 smoke test 通过，[Changelog](https://github.com/fangwei123456/spikingjelly/actions/runs/38125399528) 通过。CI 检出的临时 PR merge 与最终合并提交的文件树相同。未验证整网准确率、能耗或 CUDA。 |
| [MetaBCI #119：MultiCSP 兼容性修复](https://github.com/TBC-TJU/MetaBCI/pull/119) | 本人作者；开放、非草稿、未合并 | 保留公开三维 EEG 接口与原 CSP 计算；scikit-learn 1.5.2 / 1.6.1 / 1.9.1 各 178 项算法与回归测试通过。每版本 864 个跨日测试试次预测不变；这是兼容性证据，未声称准确率提升、实时或硬件验证。[固定提交的 Mac 报告](https://raw.githubusercontent.com/Han-Shen-math/MetaBCI/42932cf70bc70a9314cc0ce917b0d5add4e4e387/docs/validation/csp-ovo-mac.md)。 |
| [LeRobot #4902：零尺寸数值特征修复](https://github.com/huggingface/lerobot/pull/4902) | 本人作者；开放、非草稿、未合并 | 录制/读取保留 dtype 与完整形状；CPU 345 passed、1 CUDA skipped，另有 9 项流式测试通过。Windows 单项 CUDA normalizer 设备测试通过，仅检查图像设备保持，未建立零尺寸特征的 GPU 覆盖。 |
| [LeRobot #4835：RoPE 验证评论](https://github.com/huggingface/lerobot/pull/4835#issuecomment-6093995249) | 本人参与组件实验与数学诊断；PR 作者 Afloat16；开放、草稿、未合并 | [完整公开报告](https://raw.githubusercontent.com/Han-Shen-math/lerobot/83ff921b9541ffbc425116d0fb1ceea8f45c6cc4/benchmarks/vla_jepa_rope_study/REPORT.md)记录 18 次合成数据 CUDA 实验：单步 MSE 改善、15 步递归 MSE 更差。报告与评论已完成；未验证当前完整 PR、预训练质量或真实机器人性能，自动审计不代表独立人工评审。 |
| [BrainPy issue #718：零曲线分支连通性研究](https://github.com/brainpy/BrainPy/issues/718#issuecomment-6116187018) | 本人独立研究与技术分析；评论已发布、issue 开放；暂无后续回复 | 评论发表于 2026-10-12 01:34:38 UTC，附 [15 页 AI 辅助研究 PDF](https://github.com/user-attachments/files/33317095/smooth_formula_topology.pdf) 与 [复现包](https://github.com/user-attachments/files/33317096/brainpy-718-topology-research.zip)。基于既有不可判定性结果讨论特定完整光滑公式类与允许退化零集时的算法限制，探索解析分支、认证多项式细分与延拓；不排除有理多项式或额外正则性假设下的方法。包内记录 100 项测试通过、87 次追踪实验；21 个配置为 17 已认证、3 未决、1 不支持。本次只读取核对保存结果，未重跑。未集成 BrainPy、未复现原 HH 模型、未正式同行评审，也不是完整集成测试。 |
| [LeRobot issue #2108：变换顺序与边界诊断](https://github.com/huggingface/lerobot/issues/2108#issuecomment-6103122860) | 本人诊断与建议；评论已发布、issue 开放 | 代码审阅、解析反例、domain / codomain 问题与 AffineTransform 建议；未提交此问题的修复，无训练或 GPU 结论。 |
| [LeRobot issue #1871：目标熵澄清](https://github.com/huggingface/lerobot/issues/1871#issuecomment-6103180729) | 本人数学澄清；评论已发布、issue 开放 | 微分熵及温度损失梯度推导；负目标熵本身不证明符号错误。尺度与混合动作目标仍需单独检验，未提交修复或验证训练性能。 |

SpikingJelly #773 的最终 CI 与 Changelog 工作流均为 `completed / success`。其余 6 个相关 PR 的主要上游工作流仍为 `completed / action_required`，且 jobs 为空：等待维护者批准，不能算测试通过或失败。LeRobot #4902 / #4835 各 4 个、#4916 共 5 个，MetaBCI #119 / #120 各 2 个，TorchEEG #166 共 1 个。

发现范围结合 GitHub 作者/参与者搜索、公开活动记录和本地发布报告。搜索存在索引遗漏，公开活动有时间窗口；本页不宣称穷尽历史贡献。PR 比较对象、未发布的评审与研究计划未计入公开贡献。

研究设想根据个人讨论整理，明确区分未来研究计划与已验证结果。
