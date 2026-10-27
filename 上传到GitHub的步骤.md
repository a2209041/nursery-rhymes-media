# 上传到 GitHub 的步骤（约 10 分钟）

## 第 1 步：建仓库（2 分钟）

1. 打开 https://github.com/new
2. Repository name：`nursery-rhymes-media`（也可以起别的名，记住即可）
3. 选 **Public**（jsDelivr 只加速公开仓库；里面只有儿歌素材，不涉及隐私）
4. 勾选「Add a README file」
5. 点 **Create repository**

## 第 2 步：上传文件（5 分钟）

网页上传一次最多 100 个文件，我们只有 19 个，一次就能传完：

1. 仓库页面点 **Add file → Upload files**
2. 把本目录 `songs` 文件夹里的 **15 个 mp3** 拖进去
3. 点 **Commit changes**
4. 再点 **Add file → Upload files**，把 `videos` 文件夹里的 **4 个 mp4** 拖进去
5. 再点 **Commit changes**
6. 最后把 `README.md`、`mapping.json` 也传上去（可选，不影响使用）

> 注意：单文件超过 25MB GitHub 网页会拒收。我们最大的文件 14.3MB，都在限内。

## 第 3 步：告诉我会变的两个值

上传完成后，把 GitHub **用户名**和**仓库名**发我。例如：

> 用户名 xiaoming，仓库 nursery-rhymes-media

我改一行代码就能切到新源。

## 第 4 步：小程序后台加域名（2 分钟）

1. 打开 https://mp.weixin.qq.com → 开发管理 → 开发设置 → 服务器域名
2. 在 **downloadFile 合法域名** 里添加：`https://cdn.jsdelivr.net`
3. 保存

## 第 5 步：重新编译验证

开发者工具里点编译，点第一首歌，应该能直接出声。

---

## 常见问题

**Q：为什么要 Public 仓库？**
jsDelivr 只缓存公开仓库。仓库里只有儿歌 mp3/mp4 和文件名对照表，没有任何个人信息。

**Q：以后加第 5~10 周素材怎么办？**
同样上传到 songs/ 目录，把文件名按 `w05-1-xxx.mp3` 格式起，然后告诉我，我更新映射表。

**Q：GitHub 会不会被墙？**
我们访问的是 jsDelivr 的 CDN 节点（国内有节点），不是 GitHub 本身。日常使用一般没问题；如果家里网络特殊，以后可以再换源。
