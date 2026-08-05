# 小刚资源站

免费软件工具与实用教程的分享门户（GitHub Pages 静态站）。支持多分类、多内容分享。

## 访问方式

部署到 GitHub Pages 后，访问：

```
https://你的用户名.github.io/watermark-tool/
```

## 页面结构

- **首页 `index.html`**：分类导航式分享门户
  - 分类 Tab：全部 / 软件工具 / 文档教程
  - 顶部统计：各分类数量
  - 分享卡片：标题、描述、大小、分类标签、下载按钮
- **`files/`**：所有可下载文件放在此目录

## 当前分享内容

| 分类 | 名称 | 文件 |
|------|------|------|
| 软件工具 | 证件水印工具 | `files/证件水印工具.zip` |
| 文档教程 | 使用说明（待补充） | — |

## 如何添加新的分享内容

所有分享项在 `index.html` 底部的 `shareItems` JS 数组里配置。添加只需两步：

1. **上传文件**：把工具包/文档放到 `files/` 目录
2. **加配置项**：在 `shareItems` 数组里复制一项修改即可，字段包括：

```js
{
  cat: "soft",            // 分类：soft=软件工具 / doc=文档教程
  name: "工具名称",        // 标题
  desc: "功能描述",
  tag: "Windows",         // 小标签
  icon: "shield",         // 图标：shield/tool/file/book/doc
  file: "files/xxx.zip",  // 文件相对路径（files/ 下）
  size: "32 MB",          // 显示大小
  btnText: "下载工具"      // 按钮文字
}
```

> 提示：文件路径务必与 `files/` 下的实际文件名一致，否则下载按钮会 404。

## 技术说明

- 纯静态 HTML + CSS + JS，无需构建
- 深色 OLED 设计系统（基于 ui-ux-pro-max 生成）
- 分类筛选为前端 JS 动态渲染，支持移动端响应式
