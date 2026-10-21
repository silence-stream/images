# images

个人图床：存放需要外链（https）引用的图片。

> ⚠️ 本仓库是**公开**的，请勿存放隐私或敏感图片。

## 怎么用

### 1. 把图片放进本地文件夹

把图片文件复制到本地目录 `F:\my code\images`（也可以建子文件夹分类，如 `2026/`）。

> 建议图片名用**英文 + 数字**（避免中文名在某些场景出问题）。

### 2. 推送上去

```bash
cd "F:/my code/images"
git add .
git commit -m "添加图片 xxx"
git push
```

### 3. 拿链接

假设图片是 `photo.png`，有两种链接：

| 方式 | 链接 | 国内访问 |
|---|---|---|
| jsDelivr CDN（推荐） | `https://cdn.jsdelivr.net/gh/silence-stream/images@main/photo.png` | ✅ 一般能直连 |
| GitHub Raw | `https://raw.githubusercontent.com/silence-stream/images/main/photo.png` | ❌ 常被墙，需代理 |

> 国内访问建议用 **jsDelivr** 链接。

### 4. 引用示例

Markdown 里这样写：

```markdown
![图片说明](https://cdn.jsdelivr.net/gh/silence-stream/images@main/photo.png)
```

HTML 里这样写：

```html
<img src="https://cdn.jsdelivr.net/gh/silence-stream/images@main/photo.png" alt="图片说明">
```

## 注意事项

- 单文件大小上限 100MB（图床建议压缩后再传，如用 TinyPNG 等工具）。
- 每次 push 前记得先开代理。
- jsDelivr 缓存有延迟，刚 push 的图片可能要等几分钟才通过 CDN 访问到；着急可用 Raw 链接（需代理）。
