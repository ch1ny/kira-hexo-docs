# Bilibili 播放器

## 使用 biliplayer 标签
Kira-Hexo 为用户提供了 `{% biliplayer %}` 标签用以在文章当中快速创建**哔哩哔哩** iframe 播放器。

### 用法
```markdown
{% biliplayer 33053034 11 1 %}
```
![预览](/assets/img/biliplayer.png)

### 标签参数
| 选项 | 默认值 | 描述 |
| --- | --- | --- |
| av | 必须值 | 视频av号 |
| page | 1 | 视频分P |
| danmaku | 1 | 开启/关闭弹幕 |