### elecV2P 脚本/应用

[elecV2P](https://github.com/elecV2/elecV2P) 脚本库。收集一些适用于 elecV2P 的脚本，方便用户进行查找。

### 脚本分类

- 工具应用 tools
- 休闲娱乐 relax
- 日常打卡 routine

### 主入口 data/main.json

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

### 分类脚本 data/category_name.json

``` JSON  category_name_01.json
{
  "name": "分类名称",
  "note": "分类说明",
  "list": [
    "script_obj1", "script_obj2", "script_obj3"
  ]
}
```

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

#### 最小结构

``` JSON
{
  "name": "清空日志",
  "resource": "https://raw.githubusercontent.com/elecV2/elecV2P/master/script/JSFile/deletelog.js",
  "sponsor_img": "https://elecv2.github.io/src/wechat.png",
}
```

- sponsor_img 为接受打赏的二维码，也可不填

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

### 脚本提交流程

1. 首先在 https://github.com/elecV2/elecV2P 点击 Fork
2. 然后拉取 Fork 后的仓库到本地
  - git clone https://github.com/{{owner}}/elecV2P
3. 然后在本地添加要提交的脚本
  - 确定脚本分类，在 **data** 目录下找到对应的 json 文件
  - 按照脚本提交结构在 list 中添加相应内容
4. 检查提交内容
  - git status
  - git diff -z
5. 确认无误后，进行正式 PR 提交
  - 首先将修改后的内容 git push 到自己的仓库
  - 然后在仓库页面点击 Compare & pull request 进行正式提交

注意事项：

- 尽量一次只提交一个脚本，如有多少脚本请分开提交
- 如果对 PR 流程不熟悉，搜索 **github PR 流程**。多尝试几次就熟了
- **请放心大胆地提交 PR，反正要简单审核才能通过，不用担心对仓库有什么影响**

### TODO

- [ ] 脚本快速查找
- [ ] logo 自动生成
- [ ] contex_hash 自动生成
- [ ] script_store.efh 应用中心
- [x] 具体如何分类