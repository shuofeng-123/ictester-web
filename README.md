# 武汉芯测电子科技有限公司 官网

静态单页站点，源码托管于 GitHub，通过 GitHub Actions 自动部署到 GitHub Pages。

## 域名

正式域名：`ictester.cn`（注册商：华为云，DNS：华为云解析）

上线前需完成：
- [ ] 域名注册联系邮箱更换（域名过户）
- [ ] 企业邮箱 `xince@ictester.cn` 开通
- [ ] ICP 备案（备案主体须为武汉芯测电子科技有限公司）
- [ ] DNS 添加 A 记录指向国内服务器

## 文件结构

```
index.html      # 单页站点（含内联 CSS）
favicon.svg     # 站点图标
robots.txt      # 爬虫协议
sitemap.xml     # 站点地图
.github/workflows/deploy.yml  # 自动部署
```

## 部署

推送到 `main` 分支即触发自动部署：

```bash
git add .
git commit -m "update"
git push origin main
```

Pages 来源需设置为 **GitHub Actions**（仓库 Settings → Pages → Source）。

## 绑定自定义域名

备案通过后，在仓库根目录新增 `CNAME` 文件，内容写入 `ictester.cn`，
并在华为云 DNS 将 `ictester.cn` 与 `www.ictester.cn` 指向 GitHub Pages 或国内服务器。
