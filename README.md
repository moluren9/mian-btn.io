# 眠按钮 /  Nemu按钮 / Nemu Button

##### 项目地址: https://hiiro.club/

### 相关链接：
- [佐久间眠的直播间(已毕业)](https://space.bilibili.com/476903292/)

### 参与完善本项目

  - 若是请求添加新语音，请使用指定的**issues模板**，不熟悉github的用法也可以到[QQ](1799507119)和我联系

- 如果您可以进行开发，那么请**Fork**本项目进行修改，完成修改后在本项目中发起一个**Pull Request**，详细说明请查看以下条目

### 添加或修改音频/完善翻译

音频文件推荐使用**mp3**格式，请先音量标准化，然后放入`public/voices/`目录

所有的音频信息都存储在`src/setting/translate/voices.json`中，**添加或修改音频信息**、**完善翻译**，你同样需要修改这个文件中对应的内容

- 添加`usePicture`字段可以添加鼠标悬浮时显示的图片(请放到`public/voices/img`目录)

- 添加`mark`字段可以添加音频出处信息

- `voices.json`可以使用[button-tool](https://github.com/blacktunes/button-tool)(https://button-tool.vercel.app)进行编辑(功能尚未完善)

`voices.json`结构示例如下：
```
{
  // 语音分类列表
  "category": [
    {
      // 分类命名
      "name": "你妈的",
      "translate": {
        // 分类中文翻译
        "zh-CN": "草你○的",
        // 分类英文翻译
          "en-US": "草你○的~"
      }
    }
  ],
  // 语音列表
  "voices": [
   {
      "name": "○的",
      "path": "○的.wav",
      "date": "2020-12-20",
      "translate": {
        "zh-CN": "○的",
        "en-US": "○的"
      },
      "category": "你妈的"
    }
  ]
}
```

### 参与网页开发

本项目使用`Vue3.0`进行开发，使用`yarn`进行包管理
要部署本地开发环境，请先安装较新版的`Node`

1. **Fork**并**Clone**代码到本地
2. 进入代码目录，运行`yarn`以安装依赖项目
3. 开启本地开发服务器，运行`yarn serve`，这将会在`localhost:8080`启动，在代码修改过程中，本地开发服务器可以即时反映修改的结果
4. 要编译可供部署的文件，请运行`yarn build`，这将会在`dist`目录下生成可以直接部署到静态网站托管(GitHub Pages等)或服务器的文件

### 使用模板

若想使用网站模板开发新的语音按钮，可以选择以下两种方式:
- 修改`public`和`scr/setting`目录下的文件以及`package.json`
- 使用[voices-button-cli](https://github.com/blacktunes/voices-button-cli)命令行工具(开发中)

### 计划中功能
- 表情包搜索
- 直播通知
- 动态展示
