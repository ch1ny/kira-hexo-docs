# 音频播放

## 使用 APlayer
Kira-Hexo 自带了 `hexo-tag-aplayer` 依赖，用户可以使用它在文章中插入音乐。

关于 aplayer 的用法可以查阅[官方文档](https://github.com/MoePlayer/hexo-tag-aplayer/blob/master/docs/README-zh_cn.md#%E4%BD%BF%E7%94%A8)

你也可以在 `_config.yml` 当中添加下面的配置来开启 APlayer 对 MetingJS 的支持：
```yaml
aplayer:
    meting: true
    asset_inject: false
```
这样一来就可以通过 `{% meting ...%}` 在文章中使用 MetingJS 播放器了：
```markdown
<!-- 简单示例 (id, server, type)  -->
{% meting "60198" "netease" "playlist" %}

<!-- 进阶示例 -->
{% meting "60198" "netease" "playlist" "autoplay" "mutex:false" "listmaxheight:340px" "preload:none" "theme:#ad7a86"%}
```
下面是 meting 标签的参数列表：
| 选项 | 默认值 | 描述 |
| --- | --- | --- |
| id | 必须值 | 歌曲 id / 播放列表 id / 相册 id / 搜索关键字 |
| server | 必须值 | 音乐平台: netease, tencent, kugou, xiami, baidu |
| type | 必须值 | song, playlist, album, search, artist |
| fixed | false | 开启固定模式 |
| mini | false | 开启迷你模式 |
| loop | all | 列表循环模式：all, one,none |
| order | list | 列表播放模式： list, random |
| volume | 0.7 | 播放器音量 |
| lrctype | 0 | 歌词格式类型 |
| listfolded | false | 指定音乐播放列表是否折叠 |
| storagename | metingjs | LocalStorage 中存储播放器设定的键名 |
| autoplay | true | 自动播放，移动端浏览器暂时不支持此功能 |
| mutex | true | 该选项开启时，如果同页面有其他 aplayer 播放，该播放器会暂停 |
| listmaxheight | 340px | 播放列表的最大长度 |
| preload | auto | 音乐文件预载入模式，可选项： none, metadata, auto |
| theme | #ad7a86 | 播放器风格色彩设置 |