# 个人主页修改记录

日期：2026-09-06。初始制作阶段仅修改本地文件；用户随后已授权提交、推送和部署。

## 仓库与事实来源

- 当前目录：`/home/yuanshengzhou/Projects/YuanshengZhou309.github.io`。
- `origin`：`https://github.com/YuanshengZhou309/YuanshengZhou309.github.io.git`；当前分支：`master`。
- 初始 `git status --short` 为空，没有需要避让的已有修改。
- 已阅读 README、Jekyll 配置、页面布局、导航、样式和工作流。仓库内没有 AGENTS.md；父目录中发现的是 CS336 作业指导，内容针对课程作业，不适用于本次个人主页修改。
- 保留 Academic Pages / Minimal Mistakes 的 Jekyll 结构、主题、Gemfile 和前端依赖配置。
- 教育、项目、论文、技能及获奖信息仅来自用户所附 LaTeX 简历。姓名、联系方式、个人链接和四个研究方向来自本次请求。附件中的声学 PhD 招聘注释没有被当作任务指令。
- 根据简历，身份使用 **MSc graduate in Autonomous Systems**，没有设置当前雇主或在读身份。

## 内容修改

| 页面 | 文件 | 内容 |
| --- | --- | --- |
| About `/` | `_pages/about.md` | 英文简介、四个研究兴趣方向、教育摘要及联系信息 |
| Research & Projects `/research/` | `_pages/portfolio.html` | 五个项目的摘要和详情链接，继续使用 `portfolio` collection |
| 项目详情 `/research/.../` | `_portfolio/*.md` | 声学认证、医学图像生成、制药自动化、EMG、EEG；每项包含背景、个人工作与方法、已知结果 |
| Publications `/publications/` | `_pages/publications.html`、`_publications/taste-eeg.md` | 简历中的唯一一篇论文，以及研究贡献说明 |
| CV `/cv/` | `_pages/cv.md` | 教育、研究、项目、论文、技能、获奖、语言及实际存在的 LaTeX 下载 |
| Sitemap `/sitemap/` | `_pages/sitemap.md` | 仅列出实际个人页面、项目和论文 |

- 保留 `/about/`、`/about.html`、`/resume` 重定向，增加 `/portfolio/` 到 `/research/` 的重定向。
- 论文保留 `Xu, W., Zhu, Y., Zhou, Y., et al.` 的顺序和缩写，`Zhou, Y.` 加粗；年份为 2026，卷号 112、文章号 108883，DOI 为 `10.1016/j.bspc.2025.108883`。
- 没有添加论文 PDF、项目代码库、项目配图、准确率、误差、部署或认证结论等简历未提供的内容。
- Jekyll 对未指定日期的 collection 文档可使用构建时间作为默认日期（已核对 [Jekyll Document 源码](https://github.com/jekyll/jekyll/blob/v3.10.0/lib/jekyll/document.rb)）。配置 `show_date: false`，并在页面布局及 SEO 中禁用自动发表日期，避免将构建日期误显示为项目或论文发表日期；只呈现简历给出的月份范围和论文年份。
- `_includes/education.md` 和 `_includes/publication-citation.html` 用于复用教育与论文内容。

## 照片和公开简历

- `images/yuansheng-zhou.jpg` 是用户提供照片的原样副本；SHA-256 与原文件一致，尺寸为 2692 × 2656，约 2.2 MB。
- CSS 按原始比例显示照片，保留完整构图，不拉伸、不生成或补画照片内容。
- `files/yuansheng-zhou-cv.tex` 是可下载的公开版简历：移除电话及岗位定制注释，将简介和研究兴趣改为通用方向；教育、项目、论文、技能、获奖和语言事实保留。
- 没有修改附件原文件。网站页面和下载的 LaTeX 均不包含电话号码。
- 本机没有可用的 `pdflatex`、`xelatex`、`lualatex`、`latexmk` 或 `tectonic`，因此未执行 LaTeX 编译，也没有创建 PDF 下载链接。CV 页面明确标记 PDF 尚未提供。

## 配置、清理与样式

- `_config.yml` 设置 `url: "https://yuanshengzhou309.github.io"`、`baseurl: ""`、正确的仓库路径和 `Europe/Copenhagen` 时区。
- 侧栏显示姓名、学位背景、所在地、邮箱入口、GitHub 和 LinkedIn；不设置当前雇主。
- 导航仅保留 About、Research & Projects、Publications、CV。
- 删除模板示例论文、项目、文章、草稿、教学、演讲、示例 CV 数据、示例作者、评论、PDF 和人物照片；删除无内容或教学演示用途的页面，包括模板隐私条款和 Guide。
- `markdown_generator/`、`talkmap/` 及关联脚本和笔记本保留为上游工具，并从站点构建中排除；其中示例工具数据不会生成个人页面。README 中的上游说明和截图保留。
- 未发现 CNAME。已移除示例 Google Scholar、ORCID、PubMed、Bluesky 等账号配置；评论、统计、分享和 RSS 导航关闭，无新增统计或评论服务。
- 移除本网站不需要的全局 MathJax 和 Academicons CDN 加载，保留主题本地 Font Awesome、导航和明暗主题逻辑。
- 新增 `_sass/_personal.scss`，统一标题、正文行距、项目间距、元信息和链接；提高浅色主题链接对比度；手机上直接展示联系入口；保留键盘焦点样式。选中导航仍可点击，便于从项目详情返回列表。
- 删除仅适用于上游模板维护的自动关 PR 工作流，以及会自动提交推送的演讲地图工作流。现有 Jekyll 工作流改为 PR 或手动触发的只读构建检查，没有部署步骤。本轮没有运行远程工作流。
- `LICENSE`、README 和页脚 Jekyll / Academic Pages / Minimal Mistakes 署名保持原样。
- 本记录及开发工具已从站点构建中排除。

## 初始本地验证结果与边界（上线验证见末节）

已完成本地静态检查：

- 5 个 YAML 配置文件可解析；主配置和导航无重复键。
- 12 个内容文件的 YAML front matter 可解析；12 个唯一页面路径、4 个重定向和 4 个导航目标通过对应关系检查。
- 28 处静态内部链接与资源引用对应现有内容、文件或配置的生成路径；Liquid include 目标文件存在。项目和论文列表的动态链接通过对应 collection 的永久链接检查。
- 照片文件可解码、尺寸正确，并与原始照片逐字节校验一致；CV 下载目标真实存在。
- 论文作者顺序、加粗姓名和 DOI 与简历对应；未发现示例身份、岗位定制文本或电话残留于公开内容。
- `LICENSE`、README、页脚文件与 HEAD 逐字节一致。
- 已阅读 `git diff`，并检查新增内容；`git diff --check` 通过。删除文件均为本次确认的模板示例或无关工作流。

初始制作阶段尚未完成（后续远程构建结果见末节）：

- **Jekyll 构建与 Sass/Liquid 实际编译**：没有 `ruby`、`bundle`、`jekyll`，也没有现成 Docker/Podman 构建环境。未使用 sudo、安装系统依赖或改动系统环境。
- **桌面／手机实际渲染与交互测试**：未生成 Jekyll HTML，因此没有可据以验收的真实浏览器预览；响应式设置目前仅作源码检查。
- **LaTeX 编译与 PDF 排版检查**：缺少上述编译器；LaTeX 文件未经编译验证。
- **外部个人链接和 DOI 的在线可达性**：使用用户和简历原始链接，未访问个人档案或出版商补充事实。
- **GitHub Pages 当前远程配置**：未读取或修改仓库 Pages 设置；本地无 CNAME 不代表远程没有历史自定义域名。

## 请在发布前核实

1. 简历记载的 DTU 毕业时间为 2026 年 6 月，硕士论文项目时间为 2025 年 10 月至 2026 年 3 月；两者原样保留。
2. EMG 项目时间与 EPFL 交换期重合，简历列出的地点仍是 Kongens Lyngby；制药自动化地点为 Virum。未擅自修正这些时间和地点。
3. 作者表只给出了前三名及 `et al.`；没有补全未提供的作者或把 `Zhou, Y.` 擅自展开为完整署名。
4. 邮箱按要求使用 `s232925@dtu.dk`，请确认毕业后仍适合作为公开联系方式。
5. 原照片保留完整胶片边框，侧栏尺寸较小；请在实际预览时确认构图和清晰度符合偏好。

## 后续本地验证

在另行准备好 Ruby/Bundler 环境后，可在仓库内运行以下命令。当前没有执行这些命令，也没有安装依赖：

```bash
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll build --strict_front_matter
bundle exec jekyll serve --host 127.0.0.1
```

预览 `http://127.0.0.1:4000/`，检查首页、项目详情、论文页、CV 下载、404 和站点地图。建议分别在 375 px 手机、768 px 平板和 1440 px 桌面宽度检查导航、照片、长论文标题、联系方式、明暗主题和横向溢出。

若以后提供已安装所需包（包括 Roboto）的 LaTeX 环境，可将编译中间产物放到被排除的 `local/` 目录：

```bash
mkdir -p local/cv-build
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=local/cv-build files/yuansheng-zhou-cv.tex
```

只有编译成功并检查 PDF 排版后，再把 PDF 放入 `files/`，更新 `_pages/cv.md` 中的下载链接和说明；不要提前添加不存在的 PDF 链接。

## GitHub Pages 发布流程

1. 审阅本地改动、上述待核实信息及构建预览。收到用户后续明确指令后再提交、推送。
2. 在 GitHub 仓库 **Settings → Pages → Build and deployment** 中，选择 **Deploy from a branch**，分支选择本仓库实际使用的 `master`，目录选择 **/(root)**，保存。步骤依据 [GitHub 官方发布源说明](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。
3. 检查 Custom domain 是否为空，目标地址应为 `https://yuanshengzhou309.github.io/`。若有旧域名，在确认后通过 Pages 设置移除；本地 CNAME 的存在与否不能替代远程设置检查。
4. 推送到发布分支后，在 Actions 检查 GitHub 的 Pages 构建和部署结果。仓库内名为 **Jekyll build** 的工作流只负责构建验证，不负责部署。
5. 发布成功后访问主页，复查四个导航、五个项目、论文 DOI、照片及 CV 下载，并检查 `/sitemap.xml`。如实际发布分支改为 `main`，应相应调整 Pages 分支选择。

初始制作阶段未执行发布；随后经用户授权执行，结果记录如下。

## 发布执行记录

2026-09-06：用户明确授权提交、推送和部署。提交前重新执行静态检查与 `git diff --check`，均通过；远程 `master` 与本地起点一致。个人主页已提交为 `8b54497`（`Build Yuansheng Zhou academic personal website`）。HTTPS 推送因缺少 GitHub 登录凭据失败；现有 SSH 身份也返回 `Permission denied (publickey)`。当前 GitHub 连接对目标仓库没有写权限，且没有可连接的浏览器登录会话，因此当时未能完成推送与部署。

当时的继续条件（现已满足）：在本机配置具有该仓库写权限的 GitHub 登录（或连接仓库所属账号）。无需在聊天中提供令牌或私钥。登录可用后，继续推送本地 `master`，检查／启用 Pages 发布源，并验证构建和在线页面。此次没有修改远程仓库、远程 Pages 设置或系统 SSH 配置。


### 上线成功

2026-09-06：用户通过 GitHub CLI 登录 `YuanshengZhou309` 后，认证和推送均成功。

- 远程 Pages 已配置为从 `master` 的 `/` 发布，`build_type` 为 `legacy`，`cname` 为空；无需更改远程设置。
- 已推送个人主页提交 `8b54497` 和状态记录提交 `c848d85`。
- 对应 [Pages 构建与部署运行](https://github.com/YuanshengZhou309/YuanshengZhou309.github.io/actions/runs/34043371845) 已完成，结论为 **success**。GitHub 执行的 Jekyll 构建及部署均成功，补足了本机缺少 Ruby/Jekyll 导致的构建验证空缺。
- 正式网址：[https://yuanshengzhou309.github.io/](https://yuanshengzhou309.github.io/)。
- 已读取并检查线上 11 个内容页面（四个导航页面、五个项目详情、论文详情、Sitemap），共 23 个页面和资源地址，全部 HTTP 200。
- 线上内部链接及锚点、页面标题、论文姓名加粗、Liquid 渲染和编译后的 CSS 检查通过；未发现示例身份、电话号码或自动补入的发表日期。
- 线上个人照片和 LaTeX 简历下载内容与本地文件 SHA-256 完全一致。
- 本次成功记录作为后续文档提交同步；此文档已从网站构建中排除，不影响页面内容。

仍未完成的验证：桌面／手机浏览器视觉与交互检查、LaTeX 编译和 PDF 排版检查、外部个人档案及 DOI 的可达性检查。CV 继续提供真实存在的 LaTeX 源码下载，没有 PDF 下载链接。
