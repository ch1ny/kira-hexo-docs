# 自定义样式

`kira-hexo` 为用户提供了自定义样式的配置接口。
先在 `_config.kira.yml` 主题配置文件中新增字段 `customStyles`，其值为字符串数组。例如下面的配置：

```yaml
# 自定义样式
customStyles:
    - style
    - custom
```
之后在博客根目录下的 `source` 文件夹下分别新建 `style.css` 以及 `custom.css` 即可。

::: danger 自定义样式注意

由于 `kira-hexo` 依赖 `hexo-tag-aplayer`，该依赖会强行注入 APlayer script 标签，导致生成的样式文件错误。
如果需要开启自定义样式配置，还需要在 `_config.yml` 下，手动添加如下配置项将自动注入关闭。
```yaml
aplayer:
    asset_inject: false
```
关于这一部分我已向 `hexo-tag-aplayer` 提交相关的 [PR](https://github.com/MoePlayer/hexo-tag-aplayer/pull/119)，待该问题修复后即可免除此配置。
:::
