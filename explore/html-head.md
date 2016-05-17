# HEAD

A collection of HTML head elements.

## Elements

``` html
<title>Page Title</title>
<base href="https://example.com/page.html">
<style>
  body { color: red; }
</style>
<script src="script.js"></script>
```

## Meta Element

> 标签提供关于HTML文档的元数据。元数据不会显示在页面上，但是对于机器是可读的。它可用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他 web 服务。 —— W3School

``` html
<!-- content-Type(设定网页字符集) -->
<meta http-equiv="content-Type" content="text/html;charset=utf-8">  <!-- 旧的HTML，不推荐 -->
<meta charset="utf-8">
<!-- 优先使用 IE 最新版本和 Chrome -->
<meta http-equiv="x-ua-compatible" content="ie=edge">
<!--
    浏览器内核控制：国内浏览器很多都是双内核（webkit和Trident），
    webkit内核高速浏览，IE内核兼容网页和旧版网站。
    而添加meta标签的网站可以控制浏览器选择何种内核渲染。
-->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
<!--
    viewport：能优化移动浏览器的显示。如果不是响应式网站，不要使用initial-scale或者禁用缩放。
    width：宽度（数值 / device-width）（范围从200 到10,000，默认为980 像素）
    height：高度（数值 / device-height）（范围从223 到10,000）
    initial-scale：初始的缩放比例 （范围从>0 到10）
    minimum-scale：允许用户缩放到的最小比例
    maximum-scale：允许用户缩放到的最大比例
    user-scalable：用户是否可以手动缩 (no,yes)
    minimal-ui：可以在页面加载时最小化上下状态栏。（已弃用）
    注意，很多人使用initial-scale=1到非响应式网站上，这会让网站以100%宽度渲染，
    用户需要手动移动页面或者缩放。如果和initial-scale=1同时使用user-scalable=no或maximum-scale=1，
    则用户将不能放大/缩小网页来看到全部的内容。
 -->
<meta name="viewport" content="width=device-width, initial-scale=1">

<!--
    页面关键词，每个网页应具有描述该网页内容的一组唯一的关键字。
    使用人们可能会搜索，并准确描述网页上所提供信息的描述性和代表性关键字及短语。
    标记内容太短，则搜索引擎可能不会认为这些内容相关。另外标记不应超过 874 个字符。
 -->
<meta name="keywords" content="your,keywords,here,comma,separated,no,spaces">
<!-- 页面描述，每个网页都应有一个不超过 150 个字符且能准确反映网页内容的描述标签 -->
<meta name="description" content="150 chars">
<meta name="subject" content="your website's subject">
<meta name="language" content="en">

<!--
    搜索引擎
    all：文件将被检索，且页面上的链接可以被查询；
    none：文件将不被检索，且页面上的链接不可以被查询；
    index：文件将被检索；
    follow：页面上的链接可以被查询；
    noindex：文件将不被检索；
    nofollow：页面上的链接不可以被查询。
 -->
<meta name="robots" content="index,follow">
<meta name="googlebot" content="index,follow">
<meta name="google" content="nositelinkssearchbox">
<meta name="google-site-verification" content="verification_token">
<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm">
<meta name="abstract" content="">
<meta name="topic" content="">
<meta name="summary" content="">
<meta name="classification" content="business">
<meta name="author" content="name, email@example.com">
<meta name="designer" content="">
<meta name="reply-to" content="email@example.com">
<meta name="owner" content="">
<meta name="url" content="https://example.com/">
<meta name="identifier-URL" content="https://example.com/">
<meta name="directory" content="submission">
<meta name="category" content="">
<meta name="coverage" content="Worldwide">
<meta name="distribution" content="Global">
<meta name="rating" content="General">
<meta name="referrer" content="never">
<meta name="revisit-after" content="7 days">
<!--
    页面重定向和刷新：content内的数字代表时间（秒），既多少时间后刷新。如果加url,则会重定向到指定网页（搜索引擎能够自动检测，也很容易被引擎视作误导而受到惩罚）。
 -->
<meta http-equiv="refresh" content="300;url=https://example.com/">
<meta http-equiv="refresh" content="url=https://example.com/">

<!--
    Cache Control: 指定请求和响应遵循的缓存机制, 指导浏览器如何缓存某个响应以及缓存多长时间.
    no-cache: 先发送请求，与服务器确认该资源是否被更改，如果未被更改，则使用缓存。
    no-store: 不允许缓存，每次都要去服务器上，下载完整的响应。（安全措施）
    public: 缓存所有响应，但并非必须。因为max-age也可以做到相同效果
    private: 只为单个用户缓存，因此不允许任何中继进行缓存。（比如说CDN就不允许缓存private的响应）
    maxage: 表示当前请求开始，该响应在多久内能被缓存和重用，而不去服务器重新请求。
            例如：max-age=60表示响应可以再缓存和重用 60 秒。

 -->
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Cache-Control" content="no-cache">
<!-- 转码申明：用百度打开网页可能会对其进行转码（比如贴广告），避免转码可添加如下meta -->
<meta http-equiv="Cache-Control" content="no-siteapp" />
<!-- expires(网页到期时间):用于设定网页的到期时间，过期后网页必须到服务器上重新传输。 -->
<meta http-equiv="Expires" content="0">
<meta http-equiv="Expires" content="Sunday 26 October 2016 01:00 GMT" />
```

## 移动设备相关
```html
<!-- 针对手持设备优化，主要是针对一些老的不识别viewport的浏览器，比如黑莓 -->
<meta name="HandheldFriendly" content="true">
<!-- 微软的老式浏览器 -->
<meta name="MobileOptimized" content="320">
<!-- uc强制竖屏 -->
<meta name="screen-orientation" content="portrait">
<!-- QQ强制竖屏 -->
<meta name="x5-orientation" content="portrait">
<!-- UC强制全屏 -->
<meta name="full-screen" content="yes">
<!-- QQ强制全屏 -->
<meta name="x5-fullscreen" content="true">
<!-- UC应用模式 -->
<meta name="browsermode" content="application">
<!-- QQ应用模式 -->
<meta name="x5-page-mode" content="app">
<!-- windows phone 点击无高光 -->
<meta name="msapplication-tap-highlight" content="no">
```

## Link Element

``` html
<link rel="copyright" href="copyright.html">
<link rel="stylesheet" href="https://example.com/styles.css">
<link rel="alternate" href="https://feeds.feedburner.com/martini" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">
<link rel="alternate" href="https://es.example.com/" hreflang="es">
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="archives" href="https://example.com/2003/05/" title="May 2003">
<link rel="index" href="https://example.com/" title="DeWitt Clinton">
<link rel="start" href="https://example.com/photos/pattern_recognition_1_about/" title="Pattern Recognition 1">
<link rel="prev" href="https://example.com/opensearch/opensearch-and-openid-a-sure-way-to-get-my-attention/" title="OpenSearch and OpenID? A sure way to get my attention.">
<link rel="search" href="/search.xml" type="application/opensearchdescription+xml" title="Viatropos">
<link rel="self" type="application/atom+xml" href="https://example.com/atomFeed.php?page=3">
<link rel="first" href="https://example.com/atomFeed.php">
<link rel="next" href="https://example.com/atomFeed.php?page=4">
<link rel="previous" href="https://example.com/atomFeed.php?page=2">
<link rel="last" href="https://example.com/atomFeed.php?page=147">
<link rel="shortlink" href="https://example.com/?p=43625">
<link rel="canonical" href="https://example.com/2010/06/9-things-to-do-before-entering-social-media.html">
<link rel="amphtml" href="https://www.example.com/url/to/amp-version.html">
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">
<link rel="pingback" href="https://example.com/xmlrpc.php">
<link rel="webmention" href="https://example.com/webmention">
<link rel="manifest" href="manifest.json">
<link rel="author" href="humans.txt">
<link rel="import" href="component.html">

<!-- Prefetching, preloading, prebrowsing -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="subresource" href="styles.css">
<link rel="preload" href="image.png">
<!-- More info: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
```

### Favicons

``` html
<link rel="icon" href="path/to/favicon-16.png" sizes="16x16" type="image/png">
<link rel="icon" href="path/to/favicon-32.png" sizes="32x32" type="image/png">
<link rel="icon" href="path/to/favicon-48.png" sizes="48x48" type="image/png">
<link rel="icon" href="path/to/favicon-62.png" sizes="62x62" type="image/png">
<!-- More info: https://bitsofco.de/all-about-favicons-and-touch-icons/ -->
```

- [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)



## Browser/Platform


### Apple iOS

``` html
<!-- Smart App Banner -->
<!-- 添加智能 App 广告条 Smart App Banner：告诉浏览器这个网站对应的app，并在页面上显示下载banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Disable automatic detection and formatting of possible phone numbers -->
<!--  忽略数字自动识别为电话号码 -->
<meta name="format-detection" content="telephone=no">
<!-- 忽略识别邮箱 -->
<meta name="format-detection" content="email=no">

<!-- Add to Home Screen -->
<!-- WebApp全屏模式：伪装app，离线应用。-->
<meta name="apple-mobile-web-app-capable" content="yes"> <!-- 启用 WebApp 全屏模式 -->
<!-- 隐藏状态栏/设置状态栏颜色：只有在开启WebApp全屏模式时才生效。content的值为default | black | black-translucent -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<!-- 添加到主屏后的标题 -->
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- Touch Icons -->
<link rel="apple-touch-icon" href="apple-touch-icon.png">
<link rel="apple-touch-icon-precomposed" href="apple-touch-icon-precomposed.png">
<!-- In most cases, one 180×180px touch icon in the head is enough -->
<!-- If you use art-direction and/or want to have different content for each device, you can add more touch icons -->

<!-- Startup Image -->
<link rel="apple-touch-startup-image" href="startup.png">

<!-- More info: https://developer.apple.com/safari/library/documentation/appleapplications/reference/safarihtmlref/articles/metatags.html -->
```

- [Apple Meta Tags](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

### Apple Safari

```html
<!-- Pinned Site -->
<link rel="mask-icon" href="icon.svg" color="red">
```

### Google Android

``` html
<meta name="theme-color" content="#E64545">

<!-- Add to homescreen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->
```

### Google Chrome

``` html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Disable translation prompt -->
<meta name="google" value="notranslate">
```

### Microsoft Internet Explorer

``` html
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta http-equiv="cleartype" content="on">
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Pinned Site -->
<!-- IE 10 / Windows 8 -->
<meta name="msapplication-TileImage" content="pinned-tile-144.png">
<meta name="msapplication-TileColor" content="#009900">
<!-- IE 11 / Windows 9.1 -->
<meta name="msapplication-config" content="ieconfig.xml">
```

### Microsoft Internet Explorer (LEGACY DO NOT USE)

``` html
<!-- Legacy Tags (DO NOT USE) -->
<meta name="mssmarttagspreventparsing" content="true">
<meta http-equiv="page-enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="page-exit" content="revealtrans(duration=3,transition=12)">
```

## App Links

``` html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">
<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">
<!-- Web Fallback -->
<meta property="al:web:url" content="http://applinks.org/documentation">
<!-- More info: http://applinks.org/documentation/ -->
```

## Social

### Facebook / Open Graph

``` html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
<!-- Facebook: https://developers.facebook.com/docs/sharing/webmasters#markup -->
<!-- Open Graph: http://ogp.me/ -->
```

- [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- [Open Graph protocol](http://ogp.me/)

### Twitter

``` html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
<!-- More info: https://dev.twitter.com/cards/getting-started -->
<!-- Validate: https://dev.twitter.com/docs/cards/validation/validator -->
```

- [Twitter Cards: Getting Started Guide](https://dev.twitter.com/cards/getting-started)
- [Twitter Card Validator](https://dev.twitter.com/docs/cards/validation/validator)

### Google+ / Schema.org

``` html
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="https://example.com/image.jpg">
```

- [App Links Docs](http://applinks.org/documentation/)

## 参考资料

- [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)
- [MDN Meta](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta)
- [常用meta整理](https://segmentfault.com/a/1190000002407912)
- [HTML meta标签总结与属性使用介绍](https://segmentfault.com/a/1190000004279791)

## Author

**Josh Buchea**
- <https://github.com/joshbuchea>
- <https://github.com/xiaoyu2er>

## License

[MIT License](LICENSE)
