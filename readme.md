### elecV2P 脚本/应用

一些适用于 [elecV2P](https://github.com/elecV2/elecV2P) 的脚本。

### 格式结构

单个脚本结构(script_obj)：

``` JSON
{
  "name": "name.js",
  "logo": "url/to/logo_180x180.png",           // 应用图标。可省略，建议填写
  "note": "一些备注，关于脚本的说明",
  "tags": ["elecV2P", "标签"],
  "author": "elecV2",
  "homepage": "url/to/author",
  "resource": "url/to/file.js",
  "thumbnail": ["url/to/thum1.jpg", "url/to/thum2.jpg"],   // 应用预览图。可选
  "sponsor_img": "url/to/qr.png",
  "sponsor_txt": "捐赠支持说明/或其他账号信息",
  "content_hash": "auto content md5 hash",     // 脚本 hash。可不填，
}
```

说明：

- 必填项：name 和 resource，其他为可选项
- 推荐 logo 大小 180x180 或 192x192

主入口：main.json

``` JSON
{
  "category": [
    "url1/to/category.json",
    "url2/to/category.json",
    "url3/to/category.json",
  ]
}
```

分类脚本列表：category_name.json

``` JSON
{
  "name": "分类名称",
  "note": "分类说明",
  "scripts": [
    "script_obj1", "script_obj2", "script_obj3"
  ]
}
```

### 具体类别

- 日常签到
- 工具应用

### 待解决问题

[ ] 具体如何分类
[ ] 脚本快速查找

[x] contex_hash 及 date 自动生成(git commit)