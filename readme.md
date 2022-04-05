### elecV2P 脚本/应用

一些适用于 [elecV2P](https://github.com/elecV2/elecV2P) 的脚本。

### 格式结构

单个脚本结构(script_obj)：

``` JSON
{
  "name": "脚本名称",
  "logo": "url/to/logo_180x180.png",
  "note": "一些备注，关于脚本的说明",
  "tags": ["elecV2P", "标签"],
  "author": "elecV2",
  "homepage": "url/to/author",
  "resource": "url/to/file.js",
  "thumbnail": ["url/to/thum1.jpg", "url/to/thum2.jpg"],
  "sponsor_img": "url/to/donation_qr.png",
  "sponsor_txt": "捐赠支持说明/或其他账号信息",
  "content_hash": "auto content md5 hash",
}
```

说明：

- 必填项：name 和 resource，其他为可选项
- 推荐 logo 大小 180x180 或 192x192。建议填写
- thumbnail 应用预览图。（尺寸待定
- sponsor_img/sponsor_txt 填一个就好。建议都填
- 脚本 hash。自动生成（待完成

#### 最小单元

``` JSON
{
  "name": "清空日志",
  "resource": "https://raw.githubusercontent.com/elecV2/elecV2P/master/script/JSFile/deletelog.js",
  "sponsor_img": "https://elecv2.github.io/src/wechat.png",
}
```

- sponsor_img 也可不填。如不填，可能无法进行打赏

推荐提交结构

``` JSON
{
  "name": "清空日志",
  "logo": "https://raw.githubusercontent.com/elecV2/elecV2P-scripts/main/data/res/dlog.png",
  "note": "清空 elecV2P 脚本运行产生的日志",
  "tags": ["elecV2P", "工具"],
  "author": "elecV2",
  "homepage": "https://github.com/elecV2/elecV2P",
  "resource": "https://raw.githubusercontent.com/elecV2/elecV2P/master/script/JSFile/deletelog.js",
  "sponsor_img": "https://elecv2.github.io/src/wechat.png",
  "sponsor_txt": "如果觉得该脚本还不错的话，请作者喝杯饮料",
}
```

### 脚本分类

- 工具应用 tools
- 休闲娱乐 relax
- 日常签到 routine

### 主入口 main.json

``` JSON
{
  "tools": {
    "name": "工具应用",
    "list": [
      "https://raw.githubusercontent.com/elecV2/elecV2P-scripts/main/data/tools_01.json",
    ]
  },
  "relax": {
    "name": "休闲娱乐",
    "list": [
      "https://raw.githubusercontent.com/elecV2/elecV2P-scripts/main/data/relax_01.json"
    ]
  },
  "routine": {
    "name": "日常打卡",
    "list": [
      "https://raw.githubusercontent.com/elecV2/elecV2P-scripts/main/data/routine_01.json",
    ]
  },
}
```

### 分类脚本 category_name.json

``` JSON  category_name_01.json
{
  "name": "分类名称",
  "note": "分类说明",
  "list": [
    "script_obj1", "script_obj2", "script_obj3"
  ]
}
```

### TODO

- [ ] 脚本快速查找
- [ ] logo 自动生成
- [ ] contex_hash 自动生成
- [x] 具体如何分类