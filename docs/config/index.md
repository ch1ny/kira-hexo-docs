# 配置详解

## 配置源代码

大部分配置项均已写好对应的注释，开发者可以自行尝试。

```yaml
avatar: https://raw.githubusercontent.com/ch1ny/PictureCDN/master/others/116359b4ccf19917.jpg # 网站 Logo
background: # 既是博客的背景，又是文章默认头图
    path: https://raw.githubusercontent.com/ch1ny/PictureCDN/master/others/f0d5cc34c6e5aa7.jpg
    width: 1280
    height: 720
favicon:
    href: https://raw.githubusercontent.com/ch1ny/PictureCDN/master/others/116359b4ccf19917.jpg # 网站图标
    type: image/png # 图标类型，可能的值有(image/png, image/vnd.microsoft.icon, image/x-icon, image/gif)

# 附加图标库 使用说明：https://hexo.kira.host/config/icon
iconlib: //at.alicdn.com/t/c/font_3299330_2a7ov96q7e3.css

search:
    type: local # 可选engine（用搜索引擎搜索）、swiftype、或local（本地搜索）
    url: https://cn.bing.com/search?q=site:kira.host # 搜索引擎地址，在type为swiftype时无效 e.g:https://www.google.com/search?q={你的博客链接}
    id: <swiftype-id> # swiftype的id，见启用教程。在type为engine时无效

cdn: # 这里可以修改站点使用的库的CDN
    # disqusjs:
    #     css: https://unpkg.com/disqusjs@1.2.5/dist/disqusjs.min.css
    #     js: https://unpkg.com/disqusjs@1.2.5/dist/disqus.min.js
    gitalk:
        css: https://unpkg.com/gitalk@latest/dist/gitalk.css
        js: https://unpkg.com/gitalk@latest/dist/gitalk.min.js
    # valine:
    #     js: https://unpkg.com/valine

menu:
    回到首页:
        - /
        - icon-home
    文章归档: # 使用说明：https://docs.kira.com/article/archive
        - /archive.html
        - icon-container
    关于本人:
        - /about.html
        - icon-user
    我的朋友:
        - /friends.html # 使用说明：https://docs.kira.com/article/py
        - icon-team

widgets:
    - social
    - category
    - tagcloud
# - archive #settings: widgetAchive
# - recent_posts
# - link #settings: widgetLink

maxTagcloud: 0 # 标签云组件显示的标签数量，0 表示不限制

social:
    QQ:
        - tencent://AddContact/?fromId=45&fromSubId=1&subcmd=all&uin=1056317718&website=www.oicqzone.com
        - icon-QQ
        - rgb(49, 174, 255)
        - rgba(49, 174, 255, .1)
    哔哩哔哩:
        - https://space.bilibili.com/27905679
        - icon-bilibili
        - rgb(231, 106, 141)
        - rgba(231, 106, 141, .15)
    GitHub:
        - https://github.com/ch1ny/
        - icon-github
        - rgb(25, 23, 23)
        - rgba(25, 23, 23, .15)
    Gitee:
        - https://gitee.com/ch1ny/
        - icon-gitee
        - rgb(165, 15, 15)
        - rgba(165, 15, 15, .15)

color: # 配色方案，从first到seventh为优先级为1-7的颜色，默认为彩虹配色
    first: # 同时作为主题色
        r: 49
        g: 174
        b: 255
    second:
        r: 255
        g: 78
        b: 106
    third:
        r: 255
        g: 185
        b: 0
    fourth:
        r: 51
        g: 213
        b: 122
    fifth:
        r: 0
        g: 219
        b: 255
    sixth:
        r: 255
        g: 69
        b: 0
    seventh:
        r: 144
        g: 144
        b: 255

# 评论框，目前支持 gitalk,gitment,valine,disqus,disqusjs,changyan,livere,DiscussBot 使用 false 可以关闭
comment: gitalk
gitalk:
    admin: -your github username- # 拥有对该repo进行操作的 GitHub username
    owner: -your github username- # 持有该 repo 的 GitHub username
    repo: -issue repo name- # 存放评论的 issue 所在的 repo
    clientID: -id- # GitHub Client ID
    clientSecret: -key- # GitHub Client Secret
    title: '' # Gitalk Issue Title

copyright: '<strong>版权声明：</strong>本文采用 <a href="https://creativecommons.org/licenses/by-nc-sa/3.0/cn/deed.zh" target="_blank">CC BY-NC-SA 3.0 CN</a> 协议进行许可'
copyTip: "著作权归作者所有。\n商业转载请联系作者获得授权，非商业转载请注明出处。\n来源：%url" # 自定义复制版权文案,使用 %url 代替当前页面URL, 修改为false禁用

# achive widget behavior
widgetAchive: #文章归档组件
    archive_type: 'year' #按月展示还是按年展示
    show_count: true #是否展示数量

widgetLink: #链接组件
    - title: <title>
      img: <img_path>
      link: <url>
    - title: <title>
      img: <img_path>
      link: <url>

# 自定义侧边栏尾部内容
sidebar: ''
```